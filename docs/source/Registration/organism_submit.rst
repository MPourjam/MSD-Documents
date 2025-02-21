.. _Register Organism:


Defining Organisms
------------------


So far the prerequisites to registration of **Organisms**, **Samples** and **Datasets** are submitted.
Registration of Organism and then Samples **always comes before datasets**. It is *recommended* that you define organisms for the experiment at MSD during the start of
the project and that you define samples at MSD for each sampling attempt. Having done 
that will help not only by tracking and documenting the project but also by registration of datasets.


In order to register the organisms you need to follow **three** major steps. Firstly you need to **Create Template** 
and then **Register Template**. For registration of *Samples* and *Datasets* these two major steps are followed 
as well.

.. note::
    Go to **Submit** tab -> **Organisms** subtab, in order to submit the samples and make the relation to their corresponding organisms.


I. Create Template
^^^^^^^^^^^^^^^^^^
You will see the various metadata tabs including **General Required Metadata**, **Human Required Metadata**,  
and **Mouse Required Metadata**.

* **General Required Metadata**: Under this tab there are general metadata required for each organism getting registered at `MSD <https://www.misigdb.org/>`_
* **Human Required Metadata**: Metadata specific to *human* organisms.
* **Mouse Required Metadata**: Metadata specific to *mouse* organisms.

.. note::
    Currently, all metadata attributes are preselected. We continue with preselected attributes, and we later provide only related metadata.



.. figure:: /media/Organims_Create_Template.png
    :align: center
    :scale: 100 %
    :alt: Create Organism Template
    :class: org_registration_scsh

    Clicking on **Create Organism Template** will  download an *Excel template*.


II. Fill in the Template
^^^^^^^^^^^^^^^^^^^^^^^^

In order to introduce the organisms to `MSD <https://www.misigdb.org/>`_, the rows of the downloaded Excel must be filled with the selected metadata as columns.

.. note::
    Please be careful to open the Excel file with **English Excel** and **NOT** the **German Excel**.


The description of each column is below:

.. _General Organism Metadata:


*General Required Metadata*

* **External_ID**: If the organism has been registered on any other platform and has an ID, then you can fill this cell with that ID. This field is not required.
* **MSD_ID**: If a value for this cell is provided MSD tries to find that organism with given *MSD_ID* and update its Metadata with current given metadata in the Excel.
  :ref:`Organisms View` contains the information about  the registered organisms.
* **Name**: The name you want to give to the organism.
* **Description**: Add some extra information to the organism. It will help you later to filter them.
* **Project_ID**: The MSD ID of the project this organism belongs to. :ref:`Projects View` contains the information about all of your uploaded projects.
* **Species**: This cell should contain the scientific name of **type** of the organism you are defining. There are three options: *Mus Musculus*,
  *Sus Scrofa*, *Homo sapiens*. **Note**: Currently pig organism are not supported.
* **Sex**: The sex of the organism : **Male** or **Female**

.. figure:: /media/Organism_Fill_Template_General_Metadata.png
    :align: center
    :scale: 100 %
    :alt: Organism Submit - General Metadata
    :class: org_registration_scsh


.. _Humans Organism Metadata:

*Human Required Metadata*

According to the type of organism you are submitting the related metadata should be saved . If you are defining **human** organisms, fill the following metadata:

* **Place of Birth**: Choose related regions from the drop-down menu.
* **Medical History**: If there is specific information about the medical history of the organism then add it here. No more than **100** characters.
* **IBD**: If the organism has been diagnosed with *IBD*. *Yes* or *No*
* **Cancer**: If the organism has been diagnosed with *cancer*. *Yes* or *No*

.. figure:: /media/Organism_Fill_Template_Human_metadata.png
    :align: center
    :scale: 100 %
    :alt: Organism Submit - Human Metadata
    :class: org_registration_scsh



.. _Mice Organism Metadata:


*Mouse Required Metadata*

If you are submitting **mouse** organisms then fill the following only.

* **General Genotype**: Choose genotype of the organism from the drop-down list.
* **Genetic Modification**: Choose type of genetic modification from the drop-down list.

.. figure:: /media/Organism_Fill_Template_Mouse_Metadata.png
    :align: center
    :scale: 100 %
    :alt: Organism Submit - Mouse Metadata
    :class: org_registration_scsh

    An example of filled row for these metadata.


The figure below shows an example of defining 3 mice and 2 human organisms to a project defined in :ref:`Register Project`.
After finding the **Project_ID** of the project the organisms will be defined in the :ref:`Protocol View`.
 The 5 rows for 5 organisms will be filled but as they belong to different species the rows will be filled differently as below.

.. note::
    Pay attention that for the sake of better representation relative columns are not shown.


.. figure:: /media/Organism_Fill_Template_Example_Mice.png
    :align: center
    :scale: 100 %
    :alt: Organism Submit - Mouse Metadata - Example
    :class: org_registration_scsh

    Columns A to G contain metadata and have values for any type of organism you are uploading.
    The first three rows belong to *mice* organisms, and they have values for *mice-specific metadata* so 
    that they are only filled for *mice* organisms and **left blank** for *human* organisms.
    Columns H to K are not shown in this figure.

.. figure:: /media/Organism_Fill_Template_Example_Human.png
    :align: center
    :scale: 100 %
    :alt: Organism Submit - Human Metadata - Example
    :class: org_registration_scsh

    Columns A to G contain metadata and have values for any type of organism you are uploading.
    The last two rows belong to *human* organisms, and they have values for *human-specific metadata* so 
    that they are only filled for *human* organisms and **left blank** for *mice* organisms.
    Columns L and M are not shown in this figure.


III. Uploading Template
^^^^^^^^^^^^^^^^^^^^^^^


As we have our organism template filled with related values, it's time to upload the template to **MSD**.
In order to do so we go to *Submit* tab -> *Organisms* -> *Register Template*. By clicking on **Browse** we 
 choose filled **organism_template.xlsx** and then click on **Upload Organisms**.


.. figure:: /media/Organism_Upload_Template.png
    :align: center
    :scale: 100 %
    :alt: Organism Submit - Upload Template
    :class: org_registration_scsh


After clicking on *Upload Organisms* you will be shown a message and redirected to :ref:`Dataset Register`.
In the **Organisms** newly uploaded *oranisms* will be shown.


.. figure:: /media/Organism_View_Table.png
    :align: center
    :scale: 100 %
    :alt: Organism Table
    :class: org_view_scsh

    For explanation of the table see :ref:`Organisms View`.

