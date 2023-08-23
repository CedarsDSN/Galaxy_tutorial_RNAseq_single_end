**Importing example data for running Tertiary Analysis**
========================================================

**If you haven't run the Primary analysis and would rather download the example counts file to run the Tertiary analysis workflow**, please follow the steps below - 

.. code-block:: RST

  https://zenodo.org/record/6457007/files/GSM461177_untreat_paired_featureCounts.counts
  https://zenodo.org/record/6457007/files/GSM461178_untreat_paired_featureCounts.counts
  https://zenodo.org/record/6457007/files/GSM461180_treat_paired_featureCounts.counts
  https://zenodo.org/record/6457007/files/GSM461181_treat_paired_featureCounts.counts

.. note::

  1. Import the four count files from Zenodo or the Shared Data library by pasting the above lines into the Upload data > "Paste/Fetch data" and clicking "Start"
  2. Rename each item so that it has the sample name, and the treatment - so for example - GSM461177_untreat_paired_featureCounts.counts becomes GSM461177_untreat. For renaming your sample, go to your sample name, and click on the pencil edit button next to the name and it will open the attributes of your sample. Go to the name and edit it and click "Save"
  3. Now, create a collection by clicking on the checkbox on the top of the history. Now, select all the 4 samples that you uploaded in the step 1. Under settings button, select "Build Dataset List" and in the new textbox, enter a name for your collection and then click on "Create List" and then click on the checkbox on the top of your history again 
  4. You will need three more files - "KEGG pathways" to provide pathways to goseq, "header" file to create a header file to attach to DESeq2, and the Drosophila gene annotation file to run this workflow.
  5. For the Drosophila gene annotation file, download the `file <https://zenodo.org/record/1185122>`_ "Drosophila_melanogaster.BDGP6.87.gtf" and upload it to the history
  6. For the header file, download the file (Above “History”, click on the three dots and download the file) from `this page <https://github.com/CedarsDSN/Galaxy_tutorial/blob/main/docs/source/header.txt>`_ and upload the file to Galaxy using instructions from `here <https://galaxy-tutorial.readthedocs.io/en/latest/Supplementary%20files/Creating%20a%20data%20file/>`_ 
  7. For the KEGG pathway file, download the file from `this page <https://github.com/CedarsDSN/Galaxy_tutorial/blob/main/docs/source/KEGG_pathways_to_plot.txt>`_ and upload the file to Galaxy using instructions from `here <https://galaxy-tutorial.readthedocs.io/en/latest/Supplementary%20files/Creating%20a%20data%20file/>`_
  8. You can now ready to run the Tertiary analysis workflow and go through the next pages to improve your understanding of each step
  9. Go to workflows > "RNA-seq Tertiary Analysis single factor final version" and click on the run button
  10. Under "Input Dataset Collection", select your collection of counts files
  11. Under GTF file - gene annotation, select your gene annotation file from your history
  12. Under "KEGG pathways to plot", select the KEGG pathway file from your history
  13. Under "header", select the header file from your history
  14. Another important note is for the “goseq” tool and “Pathview” tool. Depending on the gene ID format in your GTF file, scroll down to the two goseq tools in the workflow, expand each, and check the format under “Select Gene ID format”. Use the button next to it to select your gene ID format from the dropdown list. Repeat this for the “Pathview” tool as well
  15. Before you run the workflow, please review the changes you have to make to the DESeq2 tool `instructions <https://galaxy-tutorial.readthedocs.io/en/latest/Tertiary%20analysis/Analysis%20of%20differential%20gene%20expression/Identification%20of%20differentially%20expressed%20genes/>`_ in order to run it with your dataset
  16. Scroll to the top and select "Yes" to send the results to a new history in order to send your workflow results to a new history and rename it so it's intuitive to you
  17. Click on "Run Workflow"
