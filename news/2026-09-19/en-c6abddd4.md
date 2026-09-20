---
title: "Astra Read a Cipher Nobody Had Read in 108 Years"
date: 2026-09-19
lang: en
source: https://clauday.com/article/c6abddd4-a331-4b3b-b36b-9ccd7404bbad
tags: [Research, Agents]
---

# Astra Read a Cipher Nobody Had Read in 108 Years

> 来源 / Source: https://clauday.com/article/c6abddd4-a331-4b3b-b36b-9ccd7404bbad

On November 27, 1918, a German operator sent a radio message encrypted with ADFGVX. It ran 170 ciphertext characters. It sat on the scienceblogs.de list of the top fifty unsolved ciphers, one of about twenty WWI German radio messages there, for 108 years. This week GPT-6 Astra read it.

The plaintext, once you clean it up, says an English cruiser arrived at Sevastopol on the twenty-fourth, and an allied squadron follows on the twenty-sixth. Modest content. A routine fleet-movement report. That is what most intelligence actually looks like.

The decipherment is not the impressive part. The impressive part is what Astra did next. It went and checked. HMS Canterbury, an English cruiser, logged its arrival at Sevastopol on November 24, 1918, and the arrival of an allied squadron on November 26. The model produced a falsifiable claim and then went into the archives and tried to falsify it. That is the whole difference between a plausible-sounding decrypt and a solved cipher, and for a century the reason nobody could close messages like this one was that the plausible-sounding candidates outnumbered the checkable ones.

Astra's account of why everyone else failed is the part worth keeping. The keyword TRUPPENVERSCHIEBUNG was believed to have only been in use as a key starting December 9, 1918. This message predates that by twelve days, so nobody tried it. One wrong dating assumption, held by the whole small community of people who care about these things, and the message stays closed for a century. The model was not smarter about ADFGVX than the cryptographers were. It was just unencumbered by their shared prior.

Tom's Hardware picked it up and it hit 341 points on Hacker News. The original writeup is at prinzai.com. Worth being clear about what this is and is not: it is not a cryptographic breakthrough, ADFGVX has been broken since 1918. It is a search problem with a large key space and a verification step, and that combination is now the most reliable place to point a model at. Anything where the answer is expensive to find and cheap to check is on the table.
