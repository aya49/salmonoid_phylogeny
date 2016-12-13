# Samonoid Species Phylogeny Analysis

The code in this repository builds a pipeline that takes align.txt (original nexus alignment) & talign.txt (the assumptions CHARSET portion of align.txt) and does the following:

## 1. Prepare Alignments
  1. [align.py](./align.py): organize, seperate, combine alignments from different genes. Does the same with muscel alignments for comparison1

## 2. Build Phylogeny using RAxML and BEAST2
  1. [raxml.py](./raxml.py) creates raxml phylogeny from alignments made from previous step.
  2. [raxml_lh.py](./raxml_lh.py) extracts likelihood and substitution rates from each raxml tree made by raxml.py.

Note: beast takes (.xml) files as input; these should be made using (.nexus) alignments on the beast GUI application BEAUti.

Note: [raxml_template.sh](./raxml_template.sh) and [beast_template.sh](./beast_template.sh) are templates for the bash versions (.sh) of running raxml and beast commandline programs. They may also be embedded into (.pbs) files for submission as jobs on a cluster.

Note: we recommend running beast on a commandline, as working directories cannot be defined directly.

## 

## [Report] (./report.pdf)
+ [Appendix: saturation] (./nucleotide_substitution) - BEAST2 subsitution parameters

## [Brief Presentation] (https://docs.google.com/presentation/d/1G3MzjjyX8WvfTMy2YDwjYd3TpV961PJmhzPmpEeLEzQ/edit?usp=sharing)
