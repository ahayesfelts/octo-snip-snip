# Octo-Snip-Snip

## Synopsis
Our contribution addresses the ability of read-manipulation programs to remove parts of a sequence upstream or downstream from an adaptor, without removing the adaptor itself. Our addition enables the end-user to specify the amount of base pairs to remove and, furthermore, if the adaptor should be removed.

## Arguments
      -flags

      -a                             Adaptor sequence specification (e.g.
                                     AACCGGTT, AAGGTTCC)

      -o                             Output path (e.g. /path/to/file.fasta)

      -g                             Remove the adaptor

      -c                             Remove this many base pairs before the
                                     adaptor (e.g. 100, 25, 5)

      -b                             Remove this many base pairs after the
                                     adaptor (e.g. 40, 59, 12)

## Example Usage


## Constraints
octo-snip-snip, currently, only accepts input files of type:
* .fast
- .fa
+ .fna
- .csfasta
+ .cfs
* .fastq
+ .q

## Motivation
Gaining accurate data from DNA sequences at each stage of the analysis is an essential part of genomic, transcriptomic, and proteomic studies; one of the foundational steps for these analyses is the accurate, and timely, location and removal of adaptors, primers, poly-A tails, and other wanted sequences from high throughput sequencing reads. A primary motivation behind our contribution is to improve the ability of existing read-manipulation programs that remove a sequence portion upstream or downstream from an adaptor, without removing the adaptor itself.


# COPYRIGHT

octo-snip-snip is released into the public domain by the copyright holders.

This README file was originally written by [Anaïs Hayes](https://github.com/ahayesfelts) and is likewise released into the public domain.
