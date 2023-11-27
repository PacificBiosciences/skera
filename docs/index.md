---
layout: default
title: Skera Home
nav_order: 1
description: "PacBio deconcatenation tool."
permalink: /
---

<p align="center">
  <img src="img/skera-header.png" alt="skera logo" width="600px"/>
</p>



_Skera_ splits [MAS-Seq](https://www.pacb.com/products-and-services/applications/rna-sequencing/single-cell-rna-sequencing/) PacBio HiFi reads at adapter positions generating segmented reads 
([S-reads](/read-segments)). For each input/parent read (e.g. HiFi)
_skera_ will create multiple bam records, one for each S-read. A parent read
can contain many S-reads. _Skera_ has two major functions, split and undo.
_Skera_ undo reconstitutes the original parent read from input S-reads.

## Availability
The latest version can be installed via bioconda package `pbskera`.

Please refer to our [official pbbioconda
page](https://github.com/PacificBiosciences/pbbioconda) for information on
Installation, Support, License, Copyright, and Disclaimer.

## Versions
Version **1.2.0**: [Full changelog here](/changelog)

## Input
### HiFi Reads
HiFi reads in PacBio BAM format.

### Adapters
[Adapters](/adapters) in FASTA format. 

## Execution
Skera split run on HiFi reads in PacBio BAM format:

    skera split <movie>.hifi_reads.bam adapters.fasta <movie>.skera.bam

Skera undo:

    skera undo <movie>.skera.bam <movie>.undo.bam 