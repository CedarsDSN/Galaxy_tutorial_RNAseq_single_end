**RNA-seq introduction**
=======================

Gene expression is a process where genes are transcribed to an RNA molecule and then eventually translated to form a protein product. Quantifying the expression of genes under a certain condition can be carried out using RNA-Sequencing (RNA-Seq). When a gene is expressed, it produces RNA molecules and the number of RNA molecules helps quantify the amount to which it is expressed.  There are different classes of RNA molecules, one of which is messenger RNA (mRNA), which enters into the cytoplasm from the nucleus where it is translated to the final protein product. For comparing two conditions, quantifying the number of transcripts can be a good indicator of the expression repertoire and help understand what genes are turned on or off between two circumstances. In RNA-Seq, one of the most important downstream analyses is differential expression analysis and pathway analysis. We will be conducting Primary, secondary and tertiary analysis through this tutorial and you will also learn how to use the Galaxy platform. 

===========

With next-generation sequencing, the number of genes that can be profiled for expression levels has increased to tens of thousands. There are several steps in data analysis that have been refined over the years. This tutorial goes through the steps of RNA-Seq analysis mentioned below and is based on a Galaxy RNA-Seq `tutorial <https://training.galaxyproject.org/training-material/topics/transcriptomics/tutorials/ref-based/tutorial.html>`_ -  
  - Primary analysis 
      * Processing raw data
      * Quality check and read processing
      * Trimming raw reads
  - Secondary analysis
      * Alignment
      * Quantification of reads
  - **Tertiary analysis**
      
      * Analysis of differential gene expression
        
        + Identification of differentially expressed features
        
        + Annotation of DESeq2 results
        
        + Extraction and annotation of differentially expressed genes
        
        + Visualization of the expression of differentially expressed genes
      
      * Functional enrichment analysis of DE genes
        
        + Gene Ontology analysis
        
        + goseq output
        
        + KEGG pathway analysis

This tutorial will go into the details of each step and the inputs and outputs for each step for the Galaxy workflow "RNA-Seq Primary analysis" and "RNA-seq Tertiary analysis".

.. note::

  1. The "RNA-seq Primary analysis" workflow is designed for single-end data. If you would like to run RNA-seq analysis on your paired-end data, please use the DSN Galaxy `documentation <https://galaxy-tutorial.readthedocs.io/en/latest/>`_ for the same.

  2. For users who need to run this tutorial with their data and need to run differential expression analysis, only run this "RNA-seq Tertiary" workflow if you have one factor that you know can contribute to differences in gene expression (for example treatment)

  3. For users who have more than one factor that they think may affect the gene expression, it would be better to use the "RNA-Seq Primary analysis" workflow and then run each step of the "RNA-seq Tertiary Analysis single factor final version" workflow on their own so they can change the number of factors 

  4. For all the workflows, until all the inputs have been entered and each step is discussed, do not click on the "Run workflow" button

