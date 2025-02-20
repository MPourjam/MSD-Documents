.. _16S Dataset Register:


16S Dataset Registration
------------------------


So far organisms and samples taken from them are registered at MSD, and it's time to register datasets produced from samples. As explained in :ref:`Database Structure`,
from each sample taken several datasets could be produced. For example, sample by *biopsy* allows to produce *16S rRNA gene amplicon* dataset by sending some of it 
for sequencing and it allows to produce from the same sample producing metabolomics data.

In this part we explain the last step of dataset registration for **16S rRNA** amplicon sequences.

The steps we take, as it was for sample and organism registration, are **Creating** a template, **Filling** the template, **Preparation** of fastq files,and **Uploading** the template. For dataset uploading, 
we also upload the raw files needed to get processed with the template.


I. Create Template
^^^^^^^^^^^^^^^^^^

**16S rRNA** datasets Excel template can be created by going to **Submit** tab -> **Datasets** subtab -> **16S** -> **Create Template**.
Click on **Create Dataset Template** will have an Excel template downloaded.



II. Fill in the Template
^^^^^^^^^^^^^^^^^^^^^^^^

Now that we have the Excel template download we need to fill each of rows in the Excel template for each dataset produced from the sample.


.. note::
    The first two columns of dataset Excel template are important (**DIS_Sampling_ID** and **Sample_ID**). For each uploaded dataset *both* or *one of them* should be provided.
    - Providing only **DIS_Sampling_ID**: implies retrieval of metatada automatically from DIS and registration of related organisms and samples. 
    Therefore, there is *no need* to follow :ref:`Register Organism` and :ref:`Register Samples` steps.
    - Providing only **Sample_ID**: implies that the uploaded dataset belongs to the sample with provided MSD Sample ID (P1O34S3).
    - Providing **both**: implies updating a sample already registered at MSD (having MSD Sample ID) with metadata derived automatically from DIS.


Below is the description of each column and their valid values:


* **DIS_Sampling_ID**: In case it is a human dataset belonging to a patient whose metadata is already stored at Data Integration System (DIS), **DIS Sampling ID**  should be provided in this column.
  In any other cases should be left empty. DIS ID looks like **MTXXX1234**. It starts with *MT* followed by three other letters and 4 digits at the end.
* **Sample_ID**: If this dataset belongs to a sample already registered at MSD. Either this metadata or **DIS_Sampling_ID** or both of them is necessary.
* **Name**: Desired dataset name. It helps finding the dataset later in :ref:`Datasets 16S View`.
* **Target_Gene**: From drop-down menu choose **16S**.
* **Accession**: If the dataset is already registered at some public repositories such as SRA [1]_  provide the relevant information here. Otherwise, leave it blank.
* **Sequencer**: Choose the type of sequencing machine from the drop-down menu.
* **Preparation_Protocol**: In this drop-down menu there is a list of *preparation* protocols that were submitted at :ref:`Register Protocol`.
* **Sequencing_Protocol**: In this drop-down menu there is a list of *sequencing* protocols that were submitted at :ref:`Register Protocol`.
* **Paired_Sequencing**: If sequencing data is paired-end, then choose *Yes*. It means there should be two files one for forward and one for reverse reads both of which will need to get referenced later.
* **Forward_Filename**: If the sequencing layout is *paired-end* then forward sequence read file's name goes here. Provide the **exact** and **full name** of the file. If
  the samples were not sequenced paired-end, then put a single sequncing file full name here.
* **Backward_Filename**: If the sequencing layout is not *paried-end* then there is no need to provide a file name here. Otherwise, provide the *full name* of the *reverse* reads file.
* **Target_Region**: Which region of *Target_Gene*  was targeted for creating amplicon. For example, for 16S rRNA gene any choice of nine variable regions (V1 to V9) could go here.
  This information is to be retrieved from the sequencing facility.
* **DNA_Isolation**: Choose the DNA Isolation methods used for the samples before sequencing from the drop-down menu.
* **Forward_Primer**: Choose the forward primer used for sequencing library preparation. This information is to be retrieved from the sequencing facility.
* **Forward_Primer_Seq**: This will be the sequence ofthe chosen forward primer. It gets selected according to *Forward_Primer*
  value automatically.
* **Reverse_Primer**: Choose the reverse primer used for sequencing library preparation. This information is to be retrieved from the sequencing facility.
* **Reverse_Primer_Seq**: This will be the sequence of the chosen reverse primer. It gets selected according to *Forward_Primer*
  value automatically.
* **Run_Length**: Run length for the sequencing run. Choose from drop-down menu. This information is to be retrieved from the sequencing facility.
* **Amplification_Steps**: Valid values here are **1** or **2**.
* **First_Step**: The number of PCR cycles for the first step (even if there was only on step) of PCR amplification.
* **Second_Step**: The number of PCR cycles for the second step of PCR amplification, if the were two steps of amplification.
* **Reads_Number**: Total number of reads for the dataset. It can be left blank.
* **Spike_Amount(ng)**: If the dataset has been spiked, put the amount of spike in Nanogram here. Otherwise put **0** value.
* **Sample_Weight(g)**: Weight of the sample taken for library preparation in grams. This information is to be retrieved from the sequencing facility.
 If the information is not available just put **1** here.
* **Sample_Type**: Type of sample sent for sequencing.
* **Custom_1**: After **Sample_Type** column it is possible to add desired columns and corresponding values to each of the datasets and have them stored
  at MSD.
* **Custom_2**: After **Sample_Type** column it is possible to add desired columns and corresponding values to each of the datasets and have them stored
  at MSD.


III. Preparation of fastq files.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Now that the template is ready. It's time to prepare zip file of the fastq files for uploading.
The zip file should contain all *fastq files* referenced in the Excel template so either *Forward_Filename* and *Backward_Filename*
or a single file for single end sequencing. The zip file must **NOT** contain any folders inside. 
By opening the zip file it should be possible to see the fastq (or fastq.gz) files directly. 

An example of filled dataset in Excel  as below:

.. figure:: /media/Dataset_register_DISID-Acc.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from DIS ID to Accession
    :class: dat16s_registration_scsh

    The first three datasets have MSD Sample ID (i.e: P1O273S155) and the last three does not have MSD Sample ID which means that they are coming 
    from human organisms whose metadata is already stored at DIS. The last three datasets would be created after their data is retrieved from DIS
    and related MSD organisms and samples will be created. The first three datasets are going to be assigned to already registered samples.


.. figure:: /media/Dataset_register_Seq-Paired.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from Sequencer to Paired Sequencing
    :class: dat16s_registration_scsh

    All datasets have been sequenced with Illumina MiSeq machine, same preparation protocol, same sequencing protocol and all of them are 
    paired-end.


.. figure:: /media/Dataset_register_Forw-DNAIso.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from Forward File name to DNA Isolation
    :class: dat16s_registration_scsh

    Forward file name and Reverse file name provided. Note that the **full** name of files is given. The sequencing
    has targeted V3-V4 region.


.. figure:: /media/Dataset_register_ForwP-RunLength.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from forward primer to run length
    :class: dat16s_registration_scsh

    As all datasets have been sequenced with the same protocol and same facility, the forward and reverse primer used are the same.
    Note that there is no need to choose primers sequences as they would be automatically chosen according to the chosen primers names.


.. figure:: /media/Dataset_register_Amp-SpikeAmount.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from amplification step to spike amount
    :class: dat16s_registration_scsh

    Two amplification steps for library preparation (PCR) with 15 and 10 cycles for the two steps, respectively. Reads number are not known
    and the first three datasets were spiked and the rest not, so that the amount of 6 Nanograms has been put for the first three and amount
    of **0** Nanogram for non-spiked ones.
  

.. figure:: /media/Dataset_register_SampleW-Cust2.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from Sample Weight to Custom 2
    :class: dat16s_registration_scsh

    Sample type and weight taken for sequencing for all datasets is provided (ask for this information from the sequencing facility).
    After **Sample_Type** column new custom columns with desired names and values for each dataset can be added to have them stored at MSD.
    In this example there is no **additional metadata**, but it can be provided after **Sample_Type** column.
  

IV. Uploading Template
^^^^^^^^^^^^^^^^^^^^^^^

It's time to upload the Excel template and the zip file containing all the fastq (or fastq.gz) files.


