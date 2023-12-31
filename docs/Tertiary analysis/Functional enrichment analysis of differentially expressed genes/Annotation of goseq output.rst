**goseq output**
================

With these parameters, "goseq" generates three outputs -

* A table (Ranked category list - Wallenius method) with the following columns for each GO term:
  
  a. category - GO category
  
  b. over_rep_pval - p-value for over-representation of the term in differentially expressed genes
  
  c. under_rep_pval - p-value for under-representation of the term in differentially expressed genes
  
  d. numDEInCat - number of differentially expressed genes in this category
  
  e. term - detail of the term
  
  f. ontology - MF (Molecular Function - molecular activities of gene products), CC (Cellular Component - where gene products are active), BP (Biological Process - pathways and larger processes made up of the activities of multiple gene products)
  
  g. p.adjust.over_represented - p-value for over-representation of the term in the differentially expressed genes, adjusted for multiple testing with the Benjamini-Hochberg procedure
  
  h. p.adjust.under_represented - p-value for under-representation of the term in the differentially expressed genes, adjusted for multiple testing with the Benjamini-Hochberg procedure

* A graph with the top 10 over-represented GO terms

* A table with the differentially expressed genes associated to the GO terms

.. figure:: /images/goseq_single.png
   :width: 600
   :alt: Top over represented GO terms
   
   A plot generated by goseq tool showing the top over-represented GO terms
