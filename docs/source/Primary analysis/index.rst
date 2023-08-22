
**Primary analysis**
====================

The initial step in every next-generation sequencing experiment should be to check the sequencing quality of the reads before doing any secondary or tertiary analysis. The quality of the data is important in order to trust the biological conclusions that can be drawn. During any kind of sequencing, some errors could be introduced, mostly incorrect nucleotides being called. These errors could bias the analysis and lead to improper interpretation of the data. Most NGS technologies use adapters and trimming these could improve the quality of the data.

.. note::

  Users of the quick start can use this part to download the gtf/ggf3 annotation file which is required for the workflow. 
  
  1. Go to `Ensembl <http://www.ensembl.org/index.html>`_ or `UCSC <https://hgdownload.soe.ucsc.edu/downloads.html>`_
  
  2. Enter your species of interest in the search button if you are using Ensembl or use the genome you're interested in UCSC
  
  3. Download the GFF3 file / GTF file. Most of the times, it would be gzipped
  
  4. If you're using a Mac device, double click and this would expand the file and this would make it as gtf or gff3 file
  
  5. If you're using a Windows device, use the putty terminal and type "gunzip name_of_the_gff3/gtf_file"
  
  6. You can now use the upload button on the left-hand corner of the page to upload this gff3/gtf file

The Galaxy workflow uses FastQC for quality checks and assessments. Before you start, create a history for your work. The history is always on the right side and can be renamed by clicking on history and entering a custom name such as "RNA-Seq analysis"

.. note::

  Important note for renaming files if you want to use your samples for carrying out Tertiary analysis as well
  
  1. Before you upload your files, remember to rename each of your samples
  
  2. For each sample, rename each of your sample names such that it has a unique sample name followed by the treatment that you think is a factor in your RNA-seq differential analysis
  
  3. For example, if my samples are treated and untreated, my samples would be named GSM11_untreat, GSM12_untreat, GSM13_treat and GSM14_treat
  
  4. Make sure that you do this for every sample before you upload your samples

Below are the links to perform quality checks, and process and trim raw reads -



.. toctree::

   Using example data
   Importing data
   Importing large data
   Quality check and read processing
   Trimming raw reads
