# Octo-Snip-Snip

## Synopsis
Our contribution addresses the ability of read-manipulation programs to remove parts of a sequence upstream or downstream from an adapter, without removing the adapter itself. Our addition enables the end-user to specify the amount of base pairs to remove and, furthermore, if the adapter should be removed.

## Arguments
      -flags

      -a                             Adapter sequence specification (e.g.
                                     AACCGGTT, AAGGTTCC)

      -o                             Output path (e.g. /path/to/file.fasta)

      -g                             Remove the adapter

      -c                             Remove this many base pairs before the
                                     adapter (e.g. 100, 25, 5)

      -b                             Remove this many base pairs after the
                                     adapter (e.g. 40, 59, 12)

## Example Usage 

# To remove the adaptor only:
octosnipsnip -a ADAPTER -g -o outputseq.fasta input.fasta

This will remove either 5' or 3' adapters, or a combination of the two; it is especially useful when your adapter is ligated 
to the 5' end for some reads and to the 3' end in other reads, if your adapter is within the read.



# To remove X base pairs upstream from an adapter:
octosnipsnip -a ADAPTER SEQUENCE -c NUMBER OF BASE PAIRS -o output.fastq input.fastq

This will remove only the base pairs upstream from a 3' adapter, without removing the adaptor itself.



# To remove X base pairs downstream from an adapter:
octosnipsnip -a ADAPTER SEQUENCE -b NUMBER OF BASE PAIRS -o output.fastq input.fastq

This will remove only the base pairs downstream from a 5' adapter, without the removing the adapter itself.


# To remove both X base pairs upstream from the adapter, as well as the adapter:
octosnipsnip -a ADAPTER SEQUENCE -g -c NUMBER OF BASE PAIRS -o output.fasta input.fasta


## Constraints
octo-snip-snip, currently, only accepts input files of type:
* .fasta
- .fa
+ .fna
- .csfasta
+ .cfs
* .fastq
+ .fq

## Motivation
Gaining accurate data from DNA sequences at each stage of the analysis is an essential part of genomic, transcriptomic, and proteomic studies; one of the foundational steps for these analyses is the accurate, and timely, location and removal of adaptors, primers, poly-A tails, and other wanted sequences from high throughput sequencing reads. A primary motivation behind our contribution is to improve the ability of existing read-manipulation programs that remove a sequence portion upstream or downstream from an adapter, without removing the adapter itself.


# COPYRIGHT

octo-snip-snip is released into the public domain by the copyright holders.

This README file was originally written by [Anaïs Hayes](https://github.com/ahayesfelts) and is likewise released into the public domain.
