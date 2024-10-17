.. _Analysis Result:

Analysis Result
===============

For each 16 analysis done on the platform, you can download the results from the :ref:`JobsView` by clicking on the download icon. 
By downloading the result you will get a ZIP file like the one below.

.. download:: AnalysisResult.zip
    :description: Download an example of analysis result ZIP
    :filename: source/downloads/AnalysisResults/Analysis_75.zip


Analysis result files
---------------------

mapping.tab
"""""""""""
This table file contains metadata information about each dataset in **features tables** (e.g: SOTUs, ZOTUs, Metabolites, ... tables). This is the serialized 
version of the metadata for each dataset uploaded to the platform. The columns are ordered as follows:

- **dataset-specific columns**: metadata at dataset Level (e.g: dataset name, dataset type, sequencing method)
- **project-specific columns**: metadata at project Level (e.g: project name, project description)
- **organism-specific columns**: metadata at organism Level (e.g: organism name, organism species, genetic modification)
- **sample-specific columns**: metadata at sample Level (e.g: sample name, sample type, sample collection date)

.. note:: 
    The column *dataset_name_in_features_table* contains the names of the datasets in the corresponding **features tables**. 
    This column is used to map the metadata to the corresponding dataset in the **features tables**. 

    Various dataset types of a sample can then be distinguished by sorting rows by **dataset_type** for a specific **sample_msd_id**. 



.. raw:: text

        .. literalinclude:: source/downloads/AnalysisResults/mapping.tab
            :language: none


.. download:: mapping.tab
    :description: Download a mapping.tab example file
    :filename: source/downloads/AnalysisResults/mapping.tab


SOTUs-Table.tab
---------------

This table has its rows as SOTUs (Species-level OTUs) and columns as datasets names with format of **D<DatasetID>_<given dataset name>** (see `Datasets ID prefix Table`_). 
Final column of this table is **Taxonomy** which includes the taxonomy assigned to the SOTU by *Sina* and *SILVA database version 138.1*.


.. note:: 

    In order to map corresponding metadata to datasets in this table, you need to use **dataset_name_in_features_table** column in the **mapping.tab** file. 


.. raw:: text

    .. literalinclude:: source/downloads/AnalysisResults/SOTUs-Table.tab
        :language: none




.. download:: SOTUs-Table.tab
    :description: Download a SOTUs-Table.tab example file
    :filename: source/downloads/AnalysisResults/SOTUs-Table.tab


SOTUs-Tree-nj.tre
-----------------
This is a phylogenetic tree of SOTUs in **Newick** format.


.. raw:: text

    .. literalinclude:: source/downloads/AnalysisResults/SOTUs-Tree-nj.tre
        :language: none


.. download:: SOTUs-Tree-nj.tre
    :description: Download a SOTUs-Tree-nj.tre example file
    :filename: source/downloads/AnalysisResults/SOTUs-Tree-nj.tre


SOTUs-Seqs.fasta
----------------
This file contains the sequences of SOTUs in **FASTA** format.


.. raw:: text

    .. literalinclude:: source/downloads/AnalysisResults/SOTUs-Seqs.fasta
        :language: none


.. download:: SOTUs-Seqs.fasta
    :description: Download a SOTUs-Seqs.fasta example file
    :filename: source/downloads/AnalysisResults/SOTUs-Seqs.fasta


ZOTUs-Table.tab
---------------
This table has its rows as ZOTUs and columns as datasets names with format of **D<DatasetID>_<Dataset name>**.

.. raw:: text

    .. literalinclude:: source/downloads/AnalysisResults/ZOTUs-Table.tab
        :language: none


.. download:: ZOTUs-Table.tab
    :description: Download a ZOTUs-Table.tab example file
    :filename: source/downloads/AnalysisResults/ZOTUs-Table.tab


ZOTUs-Seqs.fasta
----------------
This file contains the sequences of ZOTUs in **FASTA** format.

.. raw:: text

    .. literalinclude:: source/downloads/AnalysisResults/ZOTUs-Seqs.fasta
        :language: none


.. download:: ZOTUs-Seqs.fasta
    :description: Download a ZOTUs-Seqs.fasta example file
    :filename: source/downloads/AnalysisResults/ZOTUs-Seqs.fasta


ZOTUs-Tree-nj.tre
-----------------
This is a phylogenetic tree of ZOTUs in **Newick** format.

.. raw:: text


    .. literalinclude:: source/downloads/AnalysisResults/ZOTUs-Tree-nj.tre
        :language: none


.. download:: ZOTUs-Tree-nj.tre
    :description: Download a ZOTUs-Tree-nj.tre example file
    :filename: source/downloads/AnalysisResults/ZOTUs-Tree-nj.tre


krona_plot.html
---------------
This is a Krona plot of the SOTUs.

.. raw:: html

    <iframe src="/source/downloads/AnalysisResults/krona_plot.html" width="100%" height="500px"></iframe>


.. download:: krona_plot.html
    :description: Download a krona_plot.html example file
    :filename: source/downloads/AnalysisResults/krona_plot.html


Map-GOTU-FOTU.tab
-----------------
This two-colum table file contains the mapping information to assign GOTUs to their corresponding FOTUs.

.. raw:: text

    .. literalinclude:: source/downloads/AnalysisResults/Map-GOTU-FOTU.tab
        :language: none


.. download:: Map-GOTU-FOTU.tab
    :description: Download a Map-GOTU-FOTU.tab example file
    :filename: source/downloads/AnalysisResults/Map-GOTU-FOTU.tab


Map-SOTU-GOTU.tab
-----------------
This two-colum table file contains the mapping information to assign SOTUs to their corresponding GOTUs.

.. raw:: text

    .. literalinclude:: source/downloads/AnalysisResults/Map-SOTU-GOTU.tab
        :language: none


.. download:: Map-SOTU-GOTU.tab
    :description: Download a Map-SOTU-GOTU.tab example file
    :filename: source/downloads/AnalysisResults/Map-SOTU-GOTU.tab


Map-ZOTU-SOTU.tab
-----------------
This two-colum table file contains the mapping information to assign ZOTUs to their corresponding SOTUs.

.. raw:: text

    .. literalinclude:: source/downloads/AnalysisResults/Map-ZOTU-SOTU.tab
        :language: none


.. download:: Map-ZOTU-SOTU.tab
    :description: Download a Map-ZOTU-SOTU.tab example file
    :filename: source/downloads/AnalysisResults/Map-ZOTU-SOTU.tab


Metabolites-Table.tab
---------------------
This table has its rows as metabolites and columns as datasets names with format of **DTM<DatasetID>_<given dataset name>** (see :ref:`Datasets ID prefix Table`). Each metabolite measurement is unique by combining *Metabolites_Name*, 
*Normalization_Method*, and *Unit*. The rest of columns are dataset names with format of **DTM<DatasetID>_<given dataset name>**. The values in the table are the measurements of the metabolites in the corresponding dataset.

.. note:: 

    In order to map corresponding metadata to datasets in this table, you need to use **dataset_name_in_features_table** column in the **mapping.tab** file. 


.. raw:: text

    .. literalinclude:: source/downloads/AnalysisResults/Metabolites-Table.tab
        :language: none


.. download:: Metabolites-Table.tab
    :description: Download a Metabolites-Table.tab example file
    :filename: source/downloads/AnalysisResults/Metabolites-Table.tab

