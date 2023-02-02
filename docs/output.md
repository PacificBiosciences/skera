---
layout: default
title: Output Files
nav_order: 4
description: "Skera Output Files"
---

## Output Files

### Segmented BAM files

* `segmented.bam`

  _Skera_ outputs a BAM file containing all [segmented reads](/read-segments) that have sequential leading and trailing adapters based on the order of [adapters](/adapters) in the input fasta. 

* `segmented.non_passing.bam`

  The `non_passing.bam` file contains the bam records that have adapters found in non-sequential order. This file is necessary for `skera undo`. 

### Reports

* `summary.csv`

  The `summary.csv` contains general summary statistics for read segmentation. 
  
* `ligations.csv`

  The `ligations.csv` file contains the counts of all leading and trailing adapter combinations found in all passing and non-passing segments.

* `read_lengths.csv`

    The `read_lengths.csv` file contains the parent HiFi and s-read lengths for all passing segments.
