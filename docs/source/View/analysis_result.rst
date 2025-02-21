.. _Analysis Result:

Analysis Result
===============

For each 16 analysis done on the platform, you can download the results from the :ref:`JobsView` by clicking on the download icon. 
By the download result is a ZIP file like the one below.

:download:`AnalysisResult.zip </source/downloads/AnalysisResults/Analysis_75.zip>`


Analysis result files
---------------------

mapping.tab
^^^^^^^^^^^
This table file contains metadata information about each dataset in **feature tables** (e.g: SOTUs, ZOTUs, Metabolites, ... tables). This is the serialized 
version of the metadata for each dataset uploaded to the platform. The columns are ordered as follows:

- **dataset-specific columns**: metadata at dataset Level (e.g: dataset name, dataset type, sequencing method)
- **project-specific columns**: metadata at project Level (e.g: project name, project description)
- **organism-specific columns**: metadata at organism Level (e.g: organism name, organism species, genetic modification)
- **sample-specific columns**: metadata at sample Level (e.g: sample name, sample type, sample collection date)

.. note:: 
    The column *dataset_name_in_feature_table* contains the names of the datasets in the corresponding **feature tables**. 
    This column is used to map the metadata to the corresponding dataset in the **feature tables**. 

    Various dataset types of a sample can then be distinguished by sorting rows by **dataset_type** for a specific **sample_msd_id**. 


:download:`mapping.tab </source/downloads/AnalysisResults/mapping.tab>`


SOTUs-Table.tab
^^^^^^^^^^^^^^^

This table has its rows as SOTUs (Species-level OTUs) and columns as datasets names with format of **D<DatasetID>_<given dataset name>** (see `Datasets ID prefix Table`_). 
Final column of this table is **Taxonomy** which includes the taxonomy assigned to the SOTU by *Sina* and *SILVA database version 138.1*.


.. note:: 

    In order to map corresponding metadata to datasets in this table, use **dataset_name_in_feature_table** column in the **mapping.tab** file. 


:download:`SOTUs-Table.tab </source/downloads/AnalysisResults/SOTUs-Table.tab>`


SOTUs-Tree-nj.tre
^^^^^^^^^^^^^^^^^
This is a phylogenetic tree of SOTUs in **Newick** format.


:download:`SOTUs-Tree-nj.tre </source/downloads/AnalysisResults/SOTUs-Tree-nj.tre>`


SOTUs-Seqs.fasta
^^^^^^^^^^^^^^^^
This file contains the sequences of SOTUs in **FASTA** format.

:download:`SOTUs-Seqs.fasta </source/downloads/AnalysisResults/SOTUs-Seqs.fasta>`


ZOTUs-Table.tab
^^^^^^^^^^^^^^^
This table has its rows as ZOTUs and columns as datasets names with format of **D<DatasetID>_<Dataset name>**.

:download:`ZOTUs-Table.tab </source/downloads/AnalysisResults/ZOTUs-Table.tab>`


ZOTUs-Seqs.fasta
^^^^^^^^^^^^^^^^
This file contains the sequences of ZOTUs in **FASTA** format.

:download:`ZOTUs-Seqs.fasta </source/downloads/AnalysisResults/ZOTUs-Seqs.fasta>`


ZOTUs-Tree-nj.tre
^^^^^^^^^^^^^^^^^
This is a phylogenetic tree of ZOTUs in **Newick** format.


:download:`ZOTUs-Tree-nj.tre </source/downloads/AnalysisResults/ZOTUs-Tree-nj.tre>`


krona_plot.html
^^^^^^^^^^^^^^^
This is a Krona plot of the SOTUs.It shows the taxonomic distribution of the SOTUs in a hierarchical way.


:download:`krona_plot.html </source/downloads/AnalysisResults/krona_plot.html>`


Map-GOTU-FOTU.tab
^^^^^^^^^^^^^^^^^
This two-column table file contains the mapping information to assign GOTUs to their corresponding FOTUs.


:download:`Map-GOTU-FOTU.tab </source/downloads/AnalysisResults/Map-GOTU-FOTU.tab>`


Map-SOTU-GOTU.tab
^^^^^^^^^^^^^^^^^
This two-colum table file contains the mapping information to assign SOTUs to their corresponding GOTUs.


:download:`Map-SOTU-GOTU.tab </source/downloads/AnalysisResults/Map-SOTU-GOTU.tab>`


Map-ZOTU-SOTU.tab
^^^^^^^^^^^^^^^^^
This two-colum table file contains the mapping information to assign ZOTUs to their corresponding SOTUs.


:download:`Map-ZOTU-SOTU.tab </source/downloads/AnalysisResults/Map-ZOTU-SOTU.tab>`


Metabolites-Table.tab
^^^^^^^^^^^^^^^^^^^^^
This table has its rows as metabolites and columns as datasets names with format of **DTM<DatasetID>_<given dataset name>** (see :ref:`Datasets ID prefix Table`). Each metabolite measurement is unique by combining *Metabolites_Name*, 
*Normalization_Method*, and *Unit*. The rest of columns are dataset names with format of **DTM<DatasetID>_<given dataset name>**. The values in the table are the measurements of the metabolites in the corresponding dataset.

.. note:: 

    In order to map corresponding metadata to datasets in this table, to use **dataset_name_in_feature_table** column in the **mapping.tab** file. 


:download:`Metabolites-Table.tab </source/downloads/AnalysisResults/Metabolites-Table.tab>`

