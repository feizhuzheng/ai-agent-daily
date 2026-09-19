---
title: "每次你按回车前，ZCode 已经把整个 .git 传到阿里云了"
date: 2026-09-18
lang: zh
source: https://clauday.com/zh/article/9cede4bf-110d-4122-bc7f-b6f1fd3ac0ce
tags: [Agents, Coding, Infrastructure]
---

# 每次你按回车前，ZCode 已经把整个 .git 传到阿里云了

> 来源 / Source: https://clauday.com/zh/article/9cede4bf-110d-4122-bc7f-b6f1fd3ac0ce

Z.ai 的 ZCode 桌面端会给你的工作区打快照，然后传到阿里云对象存储。不是崩溃时传，不是你点了才传，而是挂在一个叫 captureBeforePrompt 的钩子上，你每输入一次提示词之前触发一次。有人一个会话里跑出了 62 次捕获。

包里装的东西跟你想的不一样。一个商业项目的归档解压前 345MB、加密后 313MB、42411 个文件，其中 86.6% 是 .git 目录：提交历史、松散对象、reflog、LFS 缓存。源码只占 13.4%。还活在 git 对象里的已删除内容占 29.6%。所以被带走的根本不是你给 agent 看的那些代码，是团队里每个人提交过又试图删掉的每个文件的每个版本，外加某次 force push 覆盖之前留在 reflog 里的所有密钥。

加密这一段是最该终结争论的地方。归档用 AES-256-CTR，对称密钥用 RSA-OAEP-SHA256 包一层，听着挺唬人，直到你发现那个 RSA 公钥是服务端在打快照的时候现发给客户端的，私钥从头到尾没离开过云端。一把只有服务端能用的钥匙，用途只有一个。你解不开自己的快照，厂商想什么时候解就什么时候解。上传是从你的机器直连阿里云 OSS 节点，再回调到 z.ai 后端登记对象，这也是为什么盯着 z.ai 域名流量的人什么都没看见。

两位研究者在一天之内各自独立挖到同一件事，路子都是拆 Electron 包里的 app.asar 读打包清单，其中一位顺手记下了 564 次失败的上传重试。没有任何开关能关掉它。目前唯一的缓解手段是在文件系统层面把 checkpoints 目录设成不可写，代价是 checkpoint 回滚也一起废了。Z.ai 官方号至今没吭声，一个跟 ZCode 有关联的账号发了句"hey I am sorry to let you find it"，这不叫否认。

两篇拆解在 https://tokenstead.ai/guides/zcode-silent-git-history-upload 和 https://blog.ferstar.org/en/posts/zcode-silent-workspace-snapshot-upload/。让人不舒服的推论是：checkpoint 和回滚现在是编码 agent 的标配，而所有实现这个功能的方式都是把你的工作树复制到某个地方去。大部分会告诉你复制到哪。去查一下你装了哪些，因为让 agent 敢跑的那个功能，和让它成为完美外泄通道的，是同一个功能。

相关阅读：Opus 5 写出 exploit 那篇 https://clauday.com/zh/article/702bdae7-ca67-46ad-9c10-4c3297adcf98
