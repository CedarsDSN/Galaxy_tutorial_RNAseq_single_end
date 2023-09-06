**Using example data**
=======================

Example data can be used to run this workflow. The original tutorial has provided some example data that can be easily downloaded from `here <https://zenodo.org/record/4541751>`_ and used in Galaxy. For this workflow, since it uses only single-end data, we will be using only the single-end samples from the example data. 

* On the homepage of Galaxy, on the left-hand side, click on "Upload data"

* Click on the "Paste/Fetch data" button on the textbox that appears

* Paste the below lines and then click "Start"

.. code-block:: RST

  https://zenodo.org/record/4541751/files/GSM461176.fastqsanger
  https://zenodo.org/record/4541751/files/GSM461179.fastqsanger
  https://zenodo.org/record/4541751/files/GSM461182.fastqsanger


* The files should start uploading. One more way is to download the files to your computer from the site and upload them to Filezilla and use FTP to transfer these files (Please use these `instructions <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/Importing%20large%20data.html>`_)
                                                                                                                                                                          
* Once these files have been uploaded, they have to be renamed appropriately to be used in the workflow. When successfully uploaded, the files should appear in a green background in the current history
                                                                                                                                                                           
* Here, samples GSM461176 and GSM461182 are untreated while GSM461179 is treated
                                                                                                                                                                           
* For renaming, click on the pencil icon next to each sample name. This will open a new window in Galaxy with "Edit Dataset attributes"
                                                                                                                                                                           
* Under name, change the first sample GSM461176.fastqsanger to GSM461176_untreat and GSM461179.fastqsanger to GSM461179_treat. Repeat this for GSM461182.fastqsanger as well                                                                                                                                                                                                                                                  
* You are now ready to use your fastq files. The next step so as to make it workflow-ready is to create a collection of fastq files. Please refer to these `instructions <https://galaxy-tutorial-rnaseq-single-end.readthedocs.io/en/latest/Primary%20analysis/Importing%20data.html>`_ to create a collection of your files                                                                                                                                                                            
                                                                                                                                                                          
