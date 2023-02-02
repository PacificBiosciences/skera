---
layout: default
title: Examples
nav_order: 4
description: "Skera examples"
---

## CLI example

Data generated using the [MAS-Seq for single-cell IsoSeq kit](https://www.pacb.com/products-and-services/applications/rna-sequencing/single-cell-rna-sequencing/) on either Sequel IIe or Revio can be downloaded [here](https://downloads.pacbcloud.com/public/dataset/MAS-Seq/).

```
# download HiFi reads for MAS-Seq PBMCs run on Sequel IIe
wget https://downloads.pacbcloud.com/public/dataset/MAS-Seq/DATA-SQ2-PBMC_5kcells/0-CCS/m64476e_220618_014917.hifi_reads.bam

# download MAS adapter fasta
wget https://downloads.pacbcloud.com/public/dataset/MAS-Seq/REF-MAS_adapters/MAS-Seq_Adapter_v1/mas16_primers.fasta

# run skera split to generate segmented reads
skera split m64476e_220618_014917.hifi_reads.bam mas16_primers.fasta segmented.bam
```

An example of the `segmented.bam` output can be found [here](https://downloads.pacbcloud.com/public/dataset/MAS-Seq/DATA-SQ2-PBMC_5kcells/1-Sreads/)
