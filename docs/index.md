---
layout: default
title: Skera Home
nav_order: 1
description: "PacBio deconcatenation tool."
permalink: /
---


<p align="center">
  <img src="img/skera-card.png" alt="skera logo" width="600px"/>
</p>

***

_Skera_ is currently an alpha release. The output(s), formats, and functionality is not finalized. Expect changes.

***

_Skera_ splits arrayed PacBio reads at adapter positions generating
([read-segments](/read-segments)). For each input/parent read (e.g. HiFi)
_skera_ will create multiple bam records, one for each fragment. A parent read
can contain many fragments. _Skera_ has two major functions, split and undo.
_Skera_ undo reconstitutes the original parent read from input fragments;
_Skera_ undo is not yet implemented.

## Availability
The latest version of `skera` is distributed through
[BioConda](https://github.com/PacificBiosciences/pbbioconda).

## Versions
Version **0.0.100**: [Full changelog here](/change-log)
