
Read Mapping
============

This is a Python project that does brute force read alignment between a reference genome and donor reads. The project finds substitutions and indels outputs a "predictions.txt" of these mutations in this format:

>S455 A G
>S460 A G
>S718 C A
>S863 T G
>I413 G
>I624 G
>D281 T
>D544 C

The project also does filters out random sequencing errors. 

Deliverables:
-------------
readmapping.py -- code for readmapping 

predictions.txt -- output after running project1a_10000_reference_genome.fasta and  project1a_10000_with_error_paired_reads.fasta 

predictions.zip -- zipped csv of predictions.txt


Usage
-----

To run the program, navigate to the project directory and run:

> python3 readmapping.py reference_genome.fasta donor_reads.fasta 

The program takes the following arguments:

* `--reference_genome.fasta`: A fasta file of the reference_genome.
* `--donor_reads.fasta `: A fasta file of the donor_reads.

Examples
--------

Here is an example of how to run the program: 

>python3 readmapping.py project1a_10000_reference_genome.fasta project1a_10000_with_error_paired_reads.fasta 


Performance
-----------

The program is not meant to be used for large reference genomes with a high number of donor reads. 

Runtime is based on laptop computer with the following specifications:
* Processor: 1.1 GHz Quad-Core Intel Core i5
* RAM: 8GB
* Operating System: MacOS Catalina 

For a reference genome of 1000 nucleotides and ~200 donor reads, the run time is:

real	0m16.763s
user	0m16.961s
sys	0m0.409s


For a reference genome of 10000 nucleotides and ~2000 donor reads, the run time is: 

real	32m13.156s
user	31m57.299s
sys	0m6.131s


