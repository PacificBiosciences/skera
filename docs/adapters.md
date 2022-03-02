---
layout: default
title: Adapters
nav_order: 3
description: "Description of Adapters."
---

<p align="center">
  <img src="img/segmented-read.png" alt="skera logo" width="700px"/>
</p>

***

## Adapters

Adapters must be in FASTA format `<adapters>.fasta` and ordered in the expected 
order of adapters in the reads. There should be one entry per adapter (forward 
or reverse-complement orientation) with no overlapping adapter sequences. 
Duplicate names or sequences are not allowed.

```
>A
AGCTTACTTGTGAAGA
>B
ACTTGTAAGCTGTCTA
>C
ACTCTGTCAGGTCCGA
>D
ACCTCCTCCTCCAGAA
>E
AACCGGACACACTTAG
```