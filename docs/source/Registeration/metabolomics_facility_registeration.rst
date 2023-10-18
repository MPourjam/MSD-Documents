.. _Register Metabolomics Dataset:

==================================
Submission of Metabolomics Dataset
==================================


.. _Submission of Metabolomics Runs:
I. Defining a Metabolomic Run
=============================

.. note::
    This section applies to metabolomics facility operators or members. Here the analysis 
    run preformed at metabolomics facility gets registered and given an ID. If your are 
    a scientist using MSD and need to upload metabolomics dataset to your samples then 
    please read `II. Submission of Metabolites`_.



.. _Submission of Metabolites:

II. Submission of Metabolites
=============================

As explained :ref:`here <Concepts Relaion>`, you can assign different types of dataset to 
one specific sample (See :ref:`Sample Submission <Register Samples>`). In order to add 
measured metabolites to your samples you need to follow the steps as below:

#. Submission of your :ref:`samples <Register Samples>` and assign them to related 
:ref:`organisms <Register Organism>` in one of your :ref:`projects <Register Project>`. 
After having registered your samples you will be given a sample ID for each registered 
sample (See :ref:`view samples <View Samples>`).

#. Sending your samples material for metabolites measurement.
.. note::
    It's recommended to submit your samples before sending their material to metabolomics 
    lab and use MSD Sample IDs (e.g: P10O252S134) as identifer of your samples in :ref:`metabolomics 
    runs <Metabolomics Run>`.

#. Receive metabolites excel files of your metabolites measurement requests from metabolomics 
runs. Below you can find two example files you should expect from metabolomics facility.

    1. :download:`Example 1 </downloads/MetabolitesExample1.xlsx>`
    2. :download:`Example 2 </downloads/MetabolitesExample2.xlsx>`

Metabolites excel files should have columns described as below and **an extra row below column headers** 
containing units of measurements for each metabolites.

**Columns:**
    *   *Sample_ID*: This column holds the MSD ID of your samples to be used in order to assign upcoming 
        metabolites in the file to proper samples of yours at MSD. MSD knows your samples by this IDs so 
        that if you provide wrong MSD ID your metabolites in this exel won't be assigned to your registered 
        sample at MSD. **NOTE** the second row of this column is empty.
    *   *Normalization*: The normalization method which the metabolomics facility used for normalization. 
        **NOTE** the second row of this column is empty.
    *   *Metabolites Columns*: From column **C** you should have metabolites names as first row (i.e: header) 
        and the unit of values in the next row. There should be values of the corresponding metabolites in the 
        rows related to each of your samples. In case of not having values for a specific metabolites in a 
        sample value **N/A** should be placed. (See figure of second metabolites example excel)

.. _MetabolitesExcelScreenShot1:
.. figure:: /media/MetabolitesExcelScreenShot1.png
    :align: center
    :scale: 100 %
    :alt: An examle of metabolites excel you will receive from metabolomic facility
    :class: metabolites_submission

    This figure shows an example of a typcial metabolites excel you will receive from metabolomics center.


.. _MetabolitesExcelScreenShot2:
.. figure:: /media/MetabolitesExcelScreenShot2.png
    :align: center
    :scale: 100 %
    :alt: An examle of metabolites excel with added custom metabolites
    :class: metabolites_submission

    Another example of emtabolites excel with custom added metabolites in the last column.

#. Compress all metabolites excels you want to upload into a zip file. 
You can download an example here: :download:`Metabolites Zip </downloads/Metabolites.zip>`

.. note::
    Make sure that you have used your samples MSD ID in the first column of your metabolites excel. 
    MSD will use those IDs to relate your metaboites to proper samples of your project.


#. Download metabolomics data submission template. 
You can follow the steps as shown in the picture to download it.

.. figure:: /media/MetabolomicsCreateTemplate.png
    :align: center
    :scale: 100 %
    :alt: How to download metabolomics data to MSD
    :class: metabolites_submission


.. _Metabolomics Dataset Template:
#. Fill out the metabolomics data submission template. 
The template has three main columns explained as below:


.. figure:: /media/MetabolomicsDataTemplate.png
    :align: center
    :scale: 100 %
    :alt: Metabolomics Dataset Submission Template
    :class: metabolites_submission

    **Columns**:
    *   *Dataset_Name*: This name will be prepended to the name of samples you have given in the metabolites excel 
        given as *File_Name*. Imagine you have given the dataset the name *"Measurement-1-Project-1"* (as 
        shown in the figure above) and content of *"MetabolitesExample1.xlsx"* are as shown in 
        `Metabolites Excel 1 <MetabolitesExcelScreenShot1>`_. When you submit your dataset MSD will take name of the 
        first sample (the sample with ID of *P10O2S3*) and prepend it with the value given as *Dataset_Name*. If the 
        name of sample (*P10O2S3*) is *TM7258_B3* then the name of corresponding metabolomics dataset for this sample 
        will be **Measurement-1-Project-1_TM7258_B3**. It means that you will see a row in 
        :ref:`metabolomics dataset table <View Metabolomics Dataset>` with a name as **Measurement-1-Project-1_TM7258_B3** 
        which includes all the metabolites assigned to sample with ID of *P10O2S3* in 
        `Metabolites Excel 1 <MetabolitesExcelScreenShot1>`_ .

    *   *RUN_ID*: This cell should be a drop-down choice list containing *Run IDs* submitted by metabolomics facility 
        to MSD (refer to :ref:` Submission of Run IDs <Submission of Metabolomics Runs>`). You should ask metabolomics 
        facility which did your measurements for this ID then choose the correct ID for your dataset. By this ID we 
        relate your dataset to proper raw run files submitted by metabolomics facility.
        .. note::
            If you are using excel programm with default language other than *English* version, the drop-down might not 
            work due to translation of formulas. In this case, you can refer to *Sheet 2* of the excel and find valid 
            Run IDs under a column named **Raw Sources ID**.


    *   *File_Name*:  This columns stablish a relation between metabolites excel files containing metabolites and sample IDs.
        to your *Dataset_Name* and *RUN_ID*. MSD will look in the zip file containing your metabolites excel files and tries 
        to find the given file name under this column there. Then it parses the metabolites in the metabolites excel files and 
        assign them to proper metabolomics run (i.e\: *RUN_ID*) and metabolomic dataset name (i.e: *Dataset_Name*)

#. Upload your comporessed metabolites excel files and your :ref:`metabolomics dataset submission template <Metabolomics Dataset Template>`.

As it's shown below in the screenshot you need to upload the zip file containing your metabolite excels and a mapping excel for submission as 
described above.


.. figure:: /media/MetabolomicsUpload.png
    :align: center
    :scale: 100 %
    :alt: Metabolomics Datasets Upload
    :class: metabolites_submission

    There are two fields you need to give files. **Dataset template**: here you give the filled template 
    mapping metabolites excel files to *RUN_ID* and *Dataset_Name* :ref:`Metabolomics Dataset Template <Metabolomics Dataset Template>`.
    **Dataset raw**\: Here you upload the zip file containing all emtaboliltes excel (e.g\: :ref:`Example of metabolites excel <MetabolitesExcelScreenShot1>`)



#. When the upload is finished you can view your matabolites datasets :ref:`Metaqbolomics View  <View Metabolomics Dataset>`


