.. _Register Metabolomics Dataset:


Metabolomics Dataset Registration
---------------------------------


Defining a Metabolomic Run
^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. note::
    This section applies to metabolomics facility operators or members. Here the analysis 
    run preformed at metabolomics facility gets registered and given an ID. If you are 
    a scientist using MSD and need to upload metabolomics dataset to your samples then 
    please read :ref:`Registration of Metabolites`.

In order to submit the metabolomics runs to MSD you need to follow the steps as below:


1. Make sure that your account has been added to metabolomics group operators. If it is not \
added to the group please contact MSD administrator to do so.

2. Log in with your user account and navigate to **Submit/Datasets/Metabolomics** as shown below:  

.. figure:: /media/MetabolomicsRunSubmission-TabView.png
    :align: center
    :scale: 100 %
    :alt: View of Metabolomics Run Submission Tab
    :class: metabolites_run_submission

    This figure shows the navigation path to the metabolomics run submission tab.

3. Click on **Metabolomics Run** tab. There will be a table with all the metabolomics runs submitted \
to MSD. The status of each run is displayed there in the table including **RUN_ID**, **Name**, **Wiff**, \
**Scan**, **Submitter**, **Upload Date**, and **Action**.

    By clicking on delete icon beside the Wiff file the uploaded file be deleted. Also, you can use **download**, **delete**, and **edit** to manage the run entry.

4. For adding new run fill the form as shown below and click on **Save Metabolomics Run** button.

.. figure:: /media/MetabolomicsRunSubmissionForm.png
    :align: center
    :scale: 100 %
    :alt: Metabolomics Run Submission Form
    :class: metabolites_run_submission

    This figure shows the form for submitting a new metabolomics run.
    Adding **Wiff** and **Scan** output will help managing running and 
    storing your files at MSD.


.. _Registration of Metabolites:

Registration of Metabolites (Targeted Metabolomics)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

As explained :ref:`here <Concepts Relaion>`, different types of datasets can be assigned to 
one specific sample (See :ref:`Sample Submission <Register Samples>`). In order to add 
measured metabolites to the samples you need to follow the steps as below:


1. Submission and assignment of the :ref:`samples <Register Samples>` to related \
:ref:`organisms <Register Organism>` in one of the :ref:`projects <Register Project>`. \
After registering the samples, each will be given a sample ID 
 (See :ref:`view samples <View Samples>`).

2. Sending the sample material for metabolites measurement.


.. note::
    It's recommended to submit the samples before sending the material to metabolomics \
    lab and use MSD Sample IDs (e.g: P10O252S134) as identifier of the samples in :ref:`metabolomics runs <Metabolomics Run>`.

3. Receive metabolites Excel files of the metabolites' measurement requests from metabolomics \
runs. Below there are two example files as if they are from metabolomics facility.

    1. :download:`Example 1 </source/downloads/MetabolitesExample1.xlsx>`
    2. :download:`Example 2 </source/downloads/MetabolitesExample2.xlsx>`

Metabolites Excel files should have columns described as below and **an extra row below column headers** 
containing units of measurements for each metabolite.

**Excel Template Columns:**

- *Sample_ID*: This column holds the MSD ID of the samples to be used in order to assign upcoming \
    metabolites in the file to proper samples  at MSD. MSD knows these samples by these IDs so \
    that if the wrong MSD ID is provided then metabolites in this Excel won't be assigned to ther registered \
    sample at MSD. **NOTE** the second row of this column is empty.\
    *Normalization*: The normalization method which the metabolomics facility used for normalization. \
    **NOTE** the second row of this column is empty. \


- *Metabolites Columns*: From column **C** metabolites names should be in a first row (i.e: header) \
    and the unit of values in the next row. There should be values of the corresponding metabolites in the \
    rows related to each of the samples. In case of not having values for a specific metabolite in a \
    sample value **N/A** should be placed. (See figure of second metabolites example Excel)


.. _MetabolitesExcelScreenShot1:

.. figure:: /media/MetabolitesExcelScreenShot1.png
    :align: center
    :scale: 100 %
    :alt: An example of metabolites Excel received from metabolomic facility
    :class: metabolites_submission

    This figure shows an example of a typical metabolites Excel received from metabolomics center.


.. _MetabolitesExcelScreenShot2:


.. figure:: /media/MetabolitesExcelScreenShot2.png
    :align: center
    :scale: 100 %
    :alt: An example of metabolites Excel with added custom metabolites
    :class: metabolites_submission

    Another example of metabolites Excel with custom added metabolites in the last column.

4. Compress all metabolites Excels that should be uploaded into a zip file.  
 Example zip filehere: :download:`Metabolites Zip </source/downloads/Metabolites.zip>`

.. note::
    Make sure that the first column has the MSD ID for the samples in the metabolites Excel. 
    MSD will use these IDs to relate the metabolites to proper samples of the project.


5. Download metabolomics data submission template.  
You can follow the steps as shown in the picture to download it.

.. figure:: /media/MetabolomicsCreateTemplate.png
    :align: center
    :scale: 100 %
    :alt: How to download metabolomics data to MSD
    :class: metabolites_submission


.. _Metabolomics Dataset Template:
6. Fill out the metabolomics data submission template.  
The template has three main columns explained as below:

**Excel Template Columns**:
- *Dataset_Name*: This name will be prepended to the name of samples from the metabolites Excel \
given as *File_Name*. Imagine the dataset has the following name *"Measurement-1-Project-1"* (as \
shown in the figure above) and content of *"MetabolitesExample1.xlsx"* is as shown in \
`Metabolites Excel 1 <MetabolitesExcelScreenShot1>`_. When the dataset is submitted to MSD  it will take name of the \
first sample (the sample with ID of *P10O2S3*) and prepend it with the value given as *Dataset_Name*. If the \
name of sample (*P10O2S3*) is *TM7258_B3* then the name of corresponding metabolomics dataset for this sample \
will be **Measurement-1-Project-1_TM7258_B3**. It means that there will be a row in \
:ref:`metabolomics dataset table <View Metabolomics Dataset>` with a name as **Measurement-1-Project-1_TM7258_B3** \
which includes all the metabolites assigned to sample with ID of *P10O2S3* in \
`Metabolites Excel 1 <MetabolitesExcelScreenShot1>`_ .  

- *RUN_ID*: This cell should be a drop-down choice list containing *Run IDs* submitted by metabolomics facility \
    to MSD (refer to :ref:` Submission of Run IDs <Submission of Metabolomics Runs>`). Ask metabolomics \
    facility which did this measurements for this ID then choose the correct ID for the dataset. By this ID we \
    relate the dataset to proper raw run files submitted by metabolomics facility.

    .. note::
        If you are using Excel program with default language other than *English* version, the drop-down might not 
        work due to translation of formulas. In this case, you can refer to *Sheet 2* of the Excel and find valid 
        Run IDs under a column named **Raw Sources ID**.

- *File_Name*: These columns establish a relation between metabolites Excel files containing metabolites and sample IDs \
    to the *Dataset_Name* and *RUN_ID*. MSD will look in the zip file containing the metabolites Excel files and tries \
    to find the given file name under this column there. Then it parses the metabolites in the metabolites Excel files and \
    assign them to proper metabolomics run (i.e\: *RUN_ID*) and metabolomic dataset name (i.e: *Dataset_Name*)



.. figure:: /media/MetabolomicsDataTemplate.png
    :align: center
    :scale: 100 %
    :alt: Metabolomics Dataset Submission Template
    :class: metabolites_submission


7. Upload the compressed metabolites Excel files and :ref:`metabolomics dataset submission template <Metabolomics Dataset Template>`.

As it's shown in the screenshot below upload the zip file containing the metabolite Excels and a mapping Excel for submission as 
described above.


.. figure:: /media/MetabolomicsUpload.png
    :align: center
    :scale: 100 %
    :alt: Metabolomics Datasets Upload
    :class: metabolites_submission

    There are two fields for files. **Dataset template**: here  the filled template 
    mapping metabolites Excel files to *RUN_ID* and *Dataset_Name*  is upploaded:ref:`Metabolomics Dataset Template <Metabolomics Dataset Template>`
    **Dataset raw**\: Here the zip file containing all metabolites Excel is uploaded (e.g\: :ref:`Example of metabolites Excel <MetabolitesexcelScreenShot1>`)


8. When the upload is finished :ref:`Metabolomics View  <View Metabolomics Dataset>` will contain all of the metabolites datasets submitted to MSD.
