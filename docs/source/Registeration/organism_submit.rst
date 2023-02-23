Defining Organisms
==================

.. _Register Organism:

So far we have submitted prerequisites to registeration of **Organisms**, **Samples** and **Datasets**.
 Registeration of Organism and then Samples comes always before datasets. It is *recommended* that by start of
 your project define your organisms at MSD and by each sampling attempt define your samples at MSD. Having done 
 that will help not only by tracking and documenting your porject but also by registeration of datasets.


 In order to register your organisms you need to do **two** major step. Firstly you need to **Create Template** 
 and then **Register Template**. For registration of *Samples* and *Datasets* these two major steps are folowed 
 as well.



Create Template
---------------

In order to create a template you need to click on *Organisms* tab and then *Create Template* tab.

Create Template
^^^^^^^^^^^^^^^
You will see the various metadata tabs including **General Required Metadata**, **Human Required Metadata**,  
and **Mouse Required Metadata**.

* **General Required Metadata**: Under this tab there are genearal metadata required for each organism getting registerd at `MSD <https://www.misigdb.org/>`_
* **Human Required Metadata**: Metadata specific to *human* organisms.
* **Mouse Required Metadata**: Metadata specific to *mouse* organisms.

.. note::
    Currently all metadata attributes are preselected. We continue with preselected attributes and we later provide only related metadata.



.. figure:: /media/Organims_Create_Template.png
    :align: center
    :scale: 100 %
    :alt: Create Organism Template
    :class: org_registration_scsh

    By clicking on **Create Organism Template** you download an *excel template*.


Fill in the Template
^^^^^^^^^^^^^^^^^^^^

In order to introduce your organisms to `MSD <https://www.misigdb.org/>`_, you need to fill the rows of downloaded excel with selected metadta as columns.

.. note::
    Please be careful to open the excel file with **English Excel** and **NOT** the **German excel**.

You can find description of each column as below:

.. _General Organism Metadata:


*General Required Metadata*

* **External_ID**: If the organism you're submitting has been registered on any other platform and has an ID, then you can fill this cell with that ID. This field is not required.
* **MSD_ID**: If a value for this cell is provided MSD tries to find that organims with given *MSD_ID* and update its Metadata with current given metadata in the excel.
You can find information about your registerd organisms at :ref:`Organisms View`.
* **Name**\\*: The name you want to give to your organism.
* **Description**\\*: Add some extra information to your organism. It will help you later to filter your organisms.
* **Project_ID**\\*: The MSD ID of the project this organism belongs to. You can find information about your projects
 at :ref:`Projects View`.
* **Species**\\*: This cell should contain the scientific name of **type** of organism you are defining. You have three options: *Mus Musculus*,
 *Sus Scrofa*, *Homo sapiens*. **Note**: Currently pig organims are not supported.
* **Sex**\\*: The gender of your organism : **Male** or **Female**

.. figure:: /media/Organism_Fill_Template_General_Metadata.png
    :align: center
    :scale: 100 %
    :alt: Organism Submit - General Metadata
    :class: org_registration_scsh


.. _Humans Organism Metadata:

*Human Required Metadata*

According to type of organism you are submitting you need to related metadata. If you are defining **human** organisms
 then fill following metadata:

* **Place of Birth**\\*: Choose related regions from the drop down menu.
* **Medical History**: If there is a specific information about the medical history of your organism then add it here. No more than **100** characters.
* **IBD**: If your organism has been diagnosed with *IBD*. *Yes* or *No*
* **Cancer**: If your organism has been diagnosed with *cancer*. *Yes* or *No*

.. figure:: /media/Organism_Fill_Template_Human_metadata.png
    :align: center
    :scale: 100 %
    :alt: Organism Submit - Human Metadata
    :class: org_registration_scsh



.. _Mice Organism Metadata:


*Mouse Required Metadata*

If you are submitting **mouse** organisms then fill the following only.

* **General Genotype**: Choose genotype of your organism from the drop-down list.
* **Genetic Modification**: Choose type of genetic modification from the drop-down list.

.. figure:: /media/Organism_Fill_Template_Mouse_Metadata.png
    :align: center
    :scale: 100 %
    :alt: Organism Submit - Mouse Metadata
    :class: org_registration_scsh



