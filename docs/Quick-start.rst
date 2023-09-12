**Quick-start**
===============

**Primary analysis workflow (includes Primary and Secondary analysis)**


This is the list of steps that one would require to run the RNA-seq "Primary analysis" workflow without getting into too much detail about each step. To understand each step in-depth, please proceed to the next page.

1. Open Galaxy and sign in with your username and password 
2. Create a new history for this analysis and rename this history with a name that is intuitive to you
3. Next, a very important step is deciding whether you want to run the Tertiary analysis workflow. If you do, renaming your files is very important. Rename each of your sample names such that it has a unique sample name followed by the treatment that you think is a factor in your RNA-seq differential analysis
  a. For example, if my samples are treated and untreated, my samples would be named GSM11_untreat, GSM11_untreat, GSM13_treat, GSM13_treat and so on
  b. Make sure that you do this for every sample before you upload your samples
4. Upload your fastq files that you would like to run the RNA-seq analysis with (Instructions are `here <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/Importing%20data.html>`_) If you would like to use an example dataset, please use these detailed `instructions <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/Using%20example%20data.html>`_. 
5. Under "Create a collection of input files", select your collection of fastq files from the dropdown menu. To create a collection of your fastq files, refer to the steps on `this <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/Importing%20large%20data.html>`_ page. If your files are larger than 10 GB, consider using FTP, the instructions of which are `here <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/Importing%20large%20data.html>`_
6. Navigate to the "Workflows" tab on the top of the Galaxy homepage
7. Next to the workflow named "RNA-seq Primary analysis Single-end", click on the start button 
8. This will navigate you to the page to enter all the values to run this workflow. Here, you can either send all the output to the current history or make a new history
9. Further, upload your GTF/GFF3 annotation file for the organism of interest for which you are working. For detailed instructions, please go to the Note on `Primary analysis <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/index.html>`_
10. Another file that you will need is the fasta file of your adapter sequences. If you have your own set of adapter sequences, create a file and upload it using the "Upload data" button. If you don't have a file with your adapter sequences, you can use the file uploaded to the "Data Libraries" under "Shared data". The instructions for accessing a file in the "Data Libraries" is `here <https://galaxy-tutorial.readthedocs.io/en/latest/Supplementary%20files/Obtaining%20files%20from%20Data%20Libraries.html>`_. These instructions will help you obtain the said file into your current history
11. Under "Cutadapt", under "Read options", select your adapter file or the "adapters.fa" file under "5' or 3' (Anywhere) Adapters"
12. Under "FastQC", select your adapter file or the "adapters.fa" file under "Adapter list"
13. Under "RNA STAR", select your genome of interest by clicking on the icon next to "Select reference genome", and select the genome of interest. If your genome isn't available, please contact the DSN team with your request. If using the example dataset, use "dm6 sequence index"
14. Under "featureCounts", select your gene annotation GFF3 from the dropdown menu that appears (This would be the GTF/GFF3 file from your history)
15. Scroll to the top of the page and click on "Run workflow"
16. You have successfully conducted primary and secondary analysis using the "Primary analysis" workflow in Galaxy

**Tertiary analysis workflow (includes Tertiary analysis)**


1. For the "RNA-seq Tertiary analysis" workflow, you would either run it after the Primary Analysis workflow (please refer to `this <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Tertiary%20analysis/Importing%20data/Importing%20count%20data%20from%20Primary%20Analysis.html>`_ page) or run it on your own dataset (please refer to `this <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Tertiary%20analysis/Importing%20data/Importing%20example%20data%20for%20running%20Tertiary%20Analysis.html>`_ page)
2. Rename each of your count file names such that it has a unique sample name followed by the treatment that you think is a factor in your RNA-seq differential analysis
  a. For example, if my count files are treated and untreated, my count files would be named GSM11_untreat, GSM12_untreat, GSM13_treat, and GSM14_treat
  b. Make sure that you do this for every count file before you upload your samples
3. Navigate to the workflows tab, and select the Run button for the “RNA-seq Tertiary Analysis single factor final version” workflow to open the workflow and select datasets
4. For the header file, download the file from `this page <https://github.com/CedarsDSN/Galaxy_tutorial_RNAseq_single_end/blob/main/docs/source/header.txt>`_ (Above "History", click on the three dots and download the file) and upload the file to Galaxy using instructions from `here <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Supplementary%20files/Creating%20a%20data%20file.html>`_ 
5. For the KEGG pathway file, download the file from `this page <https://github.com/CedarsDSN/Galaxy_tutorial_RNAseq_single_end/blob/main/docs/source/KEGG_pathways_to_plot.txt>`_ and upload the file to Galaxy using instructions from `here <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Supplementary%20files/Creating%20a%20data%20file.html>`_
6. Under "DESeq2", under the first factor under "Specify a factor name, e.g. effects_drug_x or cancer_markers" using the edit button and under that enter the factor level under "Specify a factor level, typical values could be 'tumor', 'normal', 'treated' or 'control'". Here, the factor is Treatment and the factor levels are treated and untreated. 
  a. An important thing to note is that the factor you used in your count name file should match the word under "Select groups that correspond to this factor level"
  b. Here, the words used in the count file names are "treat" and "untreat"
  c. Hence, the default entries under "untreated" is "untreat" while under "treated" is "treat"
  d. Please change these entries according to what is in your count file names
7. For more detailed steps, please refer to the Screenshot 3 on `this page <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Tertiary%20analysis/Importing%20data/Importing%20count%20data%20from%20Primary%20Analysis.html>`_  page under Tertiary Analysis
8. Under GTF file - gene annotation, select your gene annotation file from your history
9. An important note is for the "18: goseq", "19: goseq" tool and "26: Pathview" tools. For all three, depending on the gene ID format in your GTF file, scroll down to the two goseq tools and the Pathview tool in the workflow, expand each, and check the format under "Select Gene ID format". Use the button next to it to select your gene ID format from the dropdown list. Repeat this for the "Pathview" tool as well
10. Another important note is for the "30: Cut" tool. The current setting in this tool assumes that you have three single-end samples (therefore, "Cut columns" is set to c1-c4). c1 is the name of the gene and the c2-c4 are the expression columns for the samples. Please use the edit button next to "Cut columns" to change this accordingly. If you have four paired-end samples, you should change this parameter to c1-c5.
11. Scroll to the top of the page and click on "Run workflow"
12. You have run the tertiary workflow successfully on Galaxy
