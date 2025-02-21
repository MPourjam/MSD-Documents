.. _Register Samples:


Defining Samples
----------------


So far we have some organisms like above registered at **MSD**. It's time now to define samples which we have taken
from these organisms. The process of sample registration follows the general registration approach in MSD.


In order to register the organisms you need to follow **three** major steps. Firstly **Create Template**, then
**Fill the Template**, and then **Register Template**. The same as registration of organisms which we did in previous section.



.. note::
    In order to submit the samples and make the relation to their corresponding organisms,  go to **Submit** tab in top bar -> **Samples** subtab.


I. Create Template
^^^^^^^^^^^^^^^^^^
Under **Samples** subtab there will be other tabs named **Sample Required Metadata**, **Optional Human Metadata**, and **Optional Mouse/Pig Metadata**.
Below is the description description of each:\

* **Sample Required Metadata**: Under this tab there are all metadata entries that are required for each sample to be registered at **MSD**. They are automatically preselected.
* **Optional Human Metadata**:  Under this tab there are all metadata entries relevant to each sample **derived from human**. You can select which metadata entries will be stored in the databse. 
* **Optional Mouse/Pig Metadata**: Under this tab there are all metadata entries relevant to each sample **derived from mouse or pig**. You can select which metadata entries will be stored in the databse.

.. note::
    The metadata values not provided by the user a default value would be assigned in the database.

.. note::
    All optional metadata entries will have **choices** for values in the Excel template.

After the desired metadata has been configured, it's time to create an **Excel template** with desired columns representing the chosen entries.
To do so click on **Create Sample Template** button.

An example in the figure below, creates a template to submit **both** *human* and *mouse* samples to organisms  defined in :ref:`Register Organism` part.


.. figure:: /media/Sample_Create_Template_required.png
    :align: center
    :scale: 100 %
    :alt: Create Organism Template - Required Metadata
    :class: sample_registration_scsh

    All *required* sample metadata entries are already selected.


.. figure:: /media/Sample_Create_Template_human.png
    :align: center
    :scale: 100 %
    :alt: Create Organism Template - Human Metadata
    :class: sample_registration_scsh

    You can select any number of human-related metadata entries and create an Excel
    containing this metadata as columns to fill.


.. figure:: /media/Sample_Create_Template_mouse.png
    :align: center
    :scale: 100 %
    :alt: Create Organism Template - Mouse Metadata
    :class: sample_registration_scsh

    You can select any number of mouse-related metadata entries and create an Excel
    containing these metadata as columns to fill.


    
Now that the metadata is selected, a pool of the samples to upload should be provided, click on **Create Sample Template** button to download the
Excel template with the desired metadata to be filled.

II. Fill in the Template
^^^^^^^^^^^^^^^^^^^^^^^^


Now there is an Excel template with columns being the metadata chosen in the previous step. For each row that is a sample provide the corresponding values.

.. note::
    Please be careful to open the Excel file with **English Excel** and **NOT** the **German Excel**.

The descriptions of different metadata entries are listed below:

**Required Sample Metadata**


.. note::
    All sample metadata corresponds to the value at the **time of sampling**. For example, if the organism (human) used to smoke regularly when the sampling
    took place, then the value of "smoking" column for the samples taken place then should be **YES**.



* **External_ID**: The external ID to the sample *if* it is registered in other platforms such as *SRA* [1]_. If  it's not registered to any platform then leave it blak.
* **MSD_ID**: If you want to modify metadata of the samples already registered, you can put their *MSD ID* here and fill the column values. Doing so will tell MSD to update
  the metdata of the sample with provided *MSD ID* with new ones you are providing in this Excel template.
* **Name**: The name you want to give to the sample. It should be **unique** throughout all samples registered in the project to which origin organism belongs.
* **Description**: A description of for the sample. It will make it easier to search through the  samples using :ref:`Advanced Search` feature.
* **ORID**: ORID stands for "**Ori**gin **ID**". This ID tells MSD from which part the sample comes from. In order to get this ID you need to
  use the search box in :ref:`Origin View`. The ORID of the sample is to be copied to this cell. For example, **1.3.7** is the ID of saliva (material) taken from Salivary Gland (localization)
  in mouth (organ). You can choose this ORID from the drop-down menu.
* **Organism_ID**: The MSD ID of the organism from which the sample was taken. :ref:`Organism View` contains all of the organisms for the project. You can choose the organism MSD ID from the drop-down menu.
* **Weight**: Weight of the sample.
* **Weight_Unit**: The unit of Weight of the sample.
* **Age**: Age of the **organism** at time of sampling.
* **Age_Unit**: The unit of Age.
* **Preservation**: Type of sample preservation you have used for preserving the taken samples. Choose from drop-down menu. 
* **Sampling_Protocol_ID**: The sampling protocol that was used for sampling and registered in :ref:`Register Protocol` step.
* **Collection_Date**: Date of sampling in the YYYY-MM-DD format.
* **Collection_Time**: Time of sampling in the HH:MM format.
* **Collection_Country**: The country where the sampling has taken place. It should be a two-letter standard code of the country according to `ISO_3166 <https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2>`_.
* **Collection_Location_(GPS)**: The coordinates of the Sample Collection Location. Please watch this tutorial video about how to find the latitude and longitude on google maps: `video <https://www.youtube.com/watch?v=2yOX7soSPeQ&ab_channel=TechIntimidation>`_.
  The format is like: Latitude, Longitude. For example: 48.39814451278265, 11.737600673415221

**Human Sample Metadata**

* **cancer_related_symptoms**: "Yes", "No", or not assigned ("NA"). Choose from the drop-down menu.
* **arterial_hypertension**: "Yes", "No", or not assigned ("NA"). Choose from the drop-down menu.
* **hypercholesterolemia**: "Yes", "No", or not assigned ("NA"). Choose from the drop-down menu.
* **smoking**: "Yes", "No", or not assigned ("NA"). Choose from the drop-down menu.
* **alcohol_dependance**: "Yes", "No", or not assigned ("NA"). Choose from the drop-down menu.
* **physical_activity**: "Yes", "No", or not assigned ("NA"). Choose from the drop-down menu.
* **regular_medication**: "Yes" or "No". Choose from the drop-down menu.
* **regular_medication_categories**: If the value of *regular_medication* columns is "Yes" choose one option here. Otherwise, leave it blank.
* **antibiotics**: "Yes" or "No". Choose from the drop-down menu.
* **probiotics**: "Yes" or "No". Choose from the drop-down menu.
* **supplements**: "Yes" or "No". Choose from the drop-down menu.
* **bristol_score**: The bristol score for stool samples. If the sample is not stool, leave it blank.
* **tissue_available**: "Yes" or "No". Choose from the drop-down menu. If there is still some tissue, from which samples are taken, stored.
* **tissue_type**: Which method was used for taking tissue. "Biopsy" or "Resection"
* **human_diet_category**: To which diet category can  the patient be assigned at the time of sampling.
* **coffee**: "Yes", "No", or not assigned ("NA"). If the patient was taking coffee at the time of sampling.


**Mouse/Pig Sample Metadata**


* **feed_provider**: Type of feed provider. "Sniff", "Altromin" and "Other"
* **mouse_diet_category**: Type of diet the which the organism (mouse) was taking at time of sampling.
* **animal_facility**: To which animal facility within CRC, the organism is coming. Choose from the drop-down menu.
* **housing_hygiene_level**: Choose from the drop-down menu.
* **caging**: Type of caging. Choose from the drop-down menu.
* **basal_microbiota**: Choose from the drop-down menu.
* **biotic_challenge**: Choose from the drop-down menu.
* **abiotic_challenge**: Choose from the drop-down menu.

**Custom Sample Metadata**


After all the columns of selected metadata you can place any number of *custom metadata* columns with any name and provide related value to them 
for each of the samples. These custom metadata entries are stored and available for export for downstream analysis.

* **Custom_1**: You can rename these default columns to hold metadata entry to any name.
* **Custom_1**: You can rename these default columns to hold metadata entry to any name.

You can also add any number of columns after all MSD standard metadata and provide values for them.

You see and example of filled sample template Excel below:


.. figure:: /media/Sample_register_example_-ORID.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - Until ORID
    :class: sample_registration_scsh

    Eight new samples with no External_ID are going to get uploaded. Values until ORID columns. the first four rows are mouse samples and the rest human samples.


.. figure:: /media/Sample_register_example_OrgID-Preservation.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - From Organism ID to Preservation Type
    :class: sample_registration_scsh

    The same samples as prevoius figure. Filled from *Organims_ID* to *Preservation*. the first four rows are mouse samples and the rest human samples.


.. figure:: /media/Sample_register_example_SampProt-GPS.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from Sampling_Protocol_ID to *Collection_Location_(GPS)*
    :class: sample_registration_scsh

    The same samples as prevoius figure. Filled from *Sampling_Protocol_ID* to *Collection_Location_(GPS)*. the first four rows are mouse samples and the rest human samples.


.. figure:: /media/Sample_register_example_Cancer-alcohol.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from cancer_related_symptoms to alcohol_dependance
    :class: sample_registration_scsh

    The same samples as prevoius figure. Filled from *cancer_related_symptoms* to *alcohol_dependance*. the first four rows are mouse samples and the rest human samples.
    Since the first four samples are mouse samples we leave their cells empty for human metadata.


.. figure:: /media/Sample_register_example_PhysicalActivity-probiotics.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from physical_activity to *probiotics*
    :class: sample_registration_scsh

    The same samples as prevoius figure. Filled from *physical_activity* to *probiotics*. the first four rows are mouse samples and the rest human samples.
    Since the first four samples are mouse samples we leave their cells empty for human metadata.


.. figure:: /media/Sample_register_example_Supplement-Coffee.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from supplements to coffee
    :class: sample_registration_scsh

    The same samples as prevoius figure. Filled from *supplements* to *coffee*. the first four rows are mouse samples and the rest human samples.
    Since the first four samples are mouse samples we leave their cells empty for human metadata.


.. figure:: /media/Sample_register_example_feedprovider-caging.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from feed_provider to caging
    :class: sample_registration_scsh

    The same samples as prevoius figure. Filled from *feed_provider* to *caging*. the first four rows are mouse samples and the rest human samples.
    Since the last four samples are human samples we leave their cells empty for mouse metadata.


.. figure:: /media/Sample_register_example_basal_microbioata-cust2.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from basal_microbiota to Custom_2
    :class: sample_registration_scsh

    The same samples as prevoius figure. Filled from *basal_microbiota* to *Custom_2*. the first four rows are mouse samples and the rest human samples.
    Since the last four samples are human samples we leave their cells empty for mouse metadata.



III. Uploading Template
^^^^^^^^^^^^^^^^^^^^^^^

Now that we have filled the Excel template it's time to upload it and register our samples to MSD. In order to upload the filled Excel you need to go to 
**Submit** tab -> **Samples** sub-tab -> **Register Template**. There you can *Browse* your computer for the filled Excel template, clicking 
**Upload Samples** button will introduce the samples to MSD.



.. figure:: /media/Sample_upload_template.png
    :align: center
    :scale: 100 %
    :alt: Sample Template Upload
    :class: sample_registration_scsh


When the sample uploading is done, a message will be shown like "Your samples have been successfully uploaded!" and you will be redirected to :ref:`Datasets 16S View`


