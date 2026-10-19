---
layout: default
title: Examples
nav_order: 4
description: "Skera examples"
---

## CLI example

Data generated using the [Kinnex kits](https://www.pacb.com/technology/kinnex/) can be downloaded [here](https://www.pacb.com/connect/datasets/#RNA-datasets). Different Kinnex kits offer different concatenation factors: 16-fold for Kinnex single-cell RNA kit, 12-fold for Kinnex 16S rRNA kit, 8-fold for Kinnex full-length RNA kit. Choose the appropriate [MAS/Kinnex adapter set](https://downloads.pacbcloud.com/public/dataset/MAS-Seq/REF-MAS_adapters/) accordingly.

```
# download HiFi reads 
wget https://downloads.pacbcloud.com/public/dataset/MAS-Seq/DATA-Revio-Kinnex-HG002-10x5p/0-CCS/m84039_240124_190648_s3.hifi_reads.bcM0002.bam

# download MAS/Kinnex adapter fasta for the Kinnex single-cell RNA kit (which uses a 16-fold concatenation)
wget https://downloads.pacbcloud.com/public/dataset/MAS-Seq/REF-MAS_adapters/MAS-Seq_Adapter_v1/mas16_primers.fasta

# run skera split to generate segmented reads
skera split m84039_240124_190648_s3.hifi_reads.bcM0002.bam mas16_primers.fasta segmented.bam
```

An example of the `segmented.bam` output can be found [here](https://downloads.pacbcloud.com/public/dataset/MAS-Seq/DATA-Revio-Kinnex-HG002-10x5p/1-Sreads/). 
