---
layout: default
title: Segmented reads
nav_order: 2
description: "Description of S-reads."
---


<p align="center">
  <img src="img/segmented-read.png" alt="skera logo" width="600px"/>
</p>

***

## Segmented Reads

A segmented read (S-read) is comprised of multiple fragments. The figure above shows an S-read with four fragments (Seq 1..4).

## Segmented read names

For segmented reads, the base ``QNAME`` follows the CCS read conventions, while
also appending the 0-based coordinate interval ``[qStart, qEnd)`` that
represents its span within the CCS read. If the CCS read is split by strand

```
  default:
  {movieName}/{holeNumber}/ccs/{qStart}_{qEnd}

  stranded:
  {movieName}/{holeNumber}/ccs/fwd/{qStart}_{qEnd}
  {movieName}/{holeNumber}/ccs/rev/{qStart}_{qEnd}
```

| BAM tag | type |               Description                |       Example       |
| ------- | ---- | ---------------------------------------- | ------------------- |
| di      | i    | 0-based index of read segment            | di:i:0              |
| qs      | i    | 0-based qStart of segment in parent read | qs:i:16             |
| qe      | i    | 0-based qEnd of segment in parent read   | qe:i:450            |
| dl      | i    | 0-based leading adapter index            | dl:i:0              |
| dr      | i    | 0-based trailing adapter index           | dr:i:1              |
| ds      | b    | binary json                              | ds:b:10,21,23,50,10 |

Notes:
 - `qs` and `qe` are 0-based left open, right closed
 - `dl` and `dr` match the ordering of adapter sequences in the user input fasta
 - `ds` contains a number of fields used for supporting _skera_ undo, not
   intended for general use
