# count_the_indexes

These programs count the indexes in Illumina fastq files.  

There are 3 programs:

countIndexes.py which will Count_both_indexes
countIndexes_i5_only.py which will count i5 (indexing read2) only
countIndexes_i7_only.py which will count i7 (indexing read1) only

The purpose of these programs is to determine the most common Illumina indexes within a fastq file.

You can use these programs to identify what indexes you actually had in a pool that was sequenced (as opposed to what you _thought_ was in the pool).

The typical use is when your demultiplexing of an Illumina run fails to obtain reads for some (or all) of the samples (which is based on the index information you put into the sample sheet).  In these cases, you can run these programs on your Undetermined_Reads file to see what indexes are most commonly in it.  You can then use that information to determine what indexes you actually used.

It is surprisingly common to make mistakes in the sample sheets and these programs can help you to determine what when wrong and then how to update the sample sheets so you can properly demultiplex (recover) your data.
