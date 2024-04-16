.. _16S Dataset Register:


16S Dataset Registration
------------------------


So far organisms and samples taken from them are registered at MSD, and it's time to register datasets produced from samples. As explained in :ref:`Database Structure`,
from each sample taken several datasets could be produced. For example, you can take a sample by *biopsy* and produce *16S rRNA gene amplicon* dataset by sending some of it 
to for sequencing and from the same sample producing metabolomics data.

In this part we explain the last step of dataset registration for **16S rRNA** amplicon sequences.

The steps we take, as it was for sample and organism registration, are **Creating** a template, **Filling** the template, **Preparation** of fastq files,and **Uploadin** the template. For dataset uploading, 
we also upload the raw files needed to get processed with the template.


I. Create Template
^^^^^^^^^^^^^^^^^^

**16S rRNA** datasets Excel template can be created by going to **Submit** tab -> **Datasets** subtab -> **16S** -> **Create Template**.
By clicking on **Create Dataset Template** and you will have an Excel template downloaded.



II. Fill in the Template
^^^^^^^^^^^^^^^^^^^^^^^^

Now that we have the Excel template download we need to fill each of rows in the Excel template for each of datasets produced from our sample.


.. note::
    The first two columns of dataset Excel template are important (**DIS_Sampling_ID** and **Sample_ID**). You can for each dataset you are 
    uploading you can provide *both* or *one of them*.
    - Providing only **DIS_Sampling_ID**: implies retrieval of metatada automatically from DIS and registration of related organisms and samples. 
    Therefore, there is *no need* to follow :ref:`Register Organism` and :ref:`Register Samples` steps.
    - Providing only **Sample_ID**: implies that the dataset you are uploading belongs to the sample with provided MSD Sample ID (P1O34S3).
    - Providing **both**: implies updating a sample already registered at MSD (having MSD Sample ID) with metadata derived automatically from DIS.


Below you find the description of each column and their valid values:


* **DIS_Sampling_ID**: If you dataset belong to human patient whose metadata is already stored at Data Integration System (DIS), you can provide **DIS Sampling ID** in this column.
  If you don't have it you can leave it empty. DIS ID looks like **MTXXX1234**. It starts with *MT* followed by three other letters and 4 digits at the end.
* **Sample_ID**: If this dataset belongs to a sample already registered at MSD. Either this metadata or **DIS_Sampling_ID** or both of them is necessary.
* **Name**: Name you want to give to your dataset. It helps you finding your dataset in :ref:`Datasets 16S View`.
* **Target_Gene**: From drop-down menu choose **16S**.
* **Accession**: If your dataset is already registered at some public repositories such as SRA [1]_ you can provide it here. Otherwise, leave it blank.
* **Sequencer**: Choose the type of sequencing machine from the drop-down menu.
* **Preparation_Protocol**: In this drop-down menu you can see a list of *preparation* protocols you submitted at :ref:`Register Protocol`.
* **Sequencing_Protocol**: In this drop-down menu you can see a list of *sequencing* protocols you submitted at :ref:`Register Protocol`.
* **Paired_Sequencing**: If your sequence has been done paired-end, then choose *Yes*. It means you have two files of forward and reverse reads which you need to provide later.
* **Forward_Filename**: If your sequencing layout is *paired-end* then your forward sequence read file's name goes here. Provide the **exact** and **full name** of your file. If
  you have not had your samples sequenced paired-end, then you will have one file whose full name you need to provide here.
* **Backward_Filename**: If your sequencing layout has been *paried-end* then no need to provide a file name here. Otherwise, provide the *full name* of your *reverse* reads file.
* **Target_Region**: Which region of *Target_Gene* you have targeted for creating amplicon. For example, for 16S rRNA gene any choice of nine variable regions (V1 to V9) could go here.
  You can ask for this information from the sequencing facility.
* **DNA_Isolation**: Choose the DNA Isolation methods used for your samples before sequencing from the drop-down menu.
* **Forward_Primer**: Choose the forward primer used for sequencing library preparation. You can ask for this
  information from the sequencing facility.
* **Forward_Primer_Seq**: This will be the sequence of your chosen forward primer. It gets selected according to *Forward_Primer*
  value automatically.
* **Reverse_Primer**: Choose the reverse primer used for sequencing library preparation. You can ask for this
  information from the sequencing facility.
* **Reverse_Primer_Seq**: This will be the sequence of your chosen reverse primer. It gets selected according to *Forward_Primer*
  value automatically.
* **Run_Length**: Run length of your sequencing run. Choose from drop-down menu. You can ask for this information from the
  sequencing facility.
* **Amplification_Steps**: Valid values here are **1** or **2**.
* **First_Step**: The number of PCR cycles for the first step (or only step if you have had only 1 step of amplification) of PCR amplification.
* **Second_Step**: The number of PCR cycles for the second step of PCR amplification, if you have had two steps of amplification.
* **Reads_Number**: Total number of reads for your dataset. If you don't know it you can leave it blank.
* **Spike_Amount(ng)**: If your dataset has been spiked, put the amount of spike in your dataset as Nanogram here. Otherwise put **0** value.
* **Sample_Weight(g)**: Weight of sample taken for library preparation in grams. You can ask for this information from the
  sequencing facility. If you don't know it just put a positive value digit there. For example: **1**
* **Sample_Type**: Type of sample to sent for sequencing.
* **Custom_1**: After **Sample_Type** column you can add your desired columns and corresponding values to each of your dataset and have them stored
  at MSD.
* **Custom_2**: After **Sample_Type** column you can add your desired columns and corresponding values to each of your dataset and have them stored
  at MSD.


III. Preparation of fastq files.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Now that you have your template ready. It's time to prepare zip file of your fastq files for uploading.
Your zip file should contain your *fastq files* (all you have put their file names in the Excel template, 
*Forward_Filename* and *Backward_Filename*). The zip file should **NOT** contain any folders inside. 
By opening the zip file you should only see the fastq (or fastq.gz) files. 

An example of filled dataset excel you can find as below:

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

    Forward file name and Reverse file name provided. Note that the **full** name of files are given. The sequencing
    has targeted V3-V4 region.


.. figure:: /media/Dataset_register_ForwP-RunLength.png
    :align: center
    :scale: 100 %
    :alt: Filled Template - from forward primer to run length
    :class: dat16s_registration_scsh

    As all datasets have been sequenced with the same protocol and same facility, the forward and reverse primer used are the same.
    Note that there is no need to choose primers sequences as they would be automatically chosen according to your chosen primers names.


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
    After **Sample_Type** column you can add your own columns with desired names and values for each dataset to have them stored at MSD.
    In this example I did not provide **additional metadata**, but you can provide yours after **Sample_Type** column.
  

IV. Uploading Template
^^^^^^^^^^^^^^^^^^^^^^^

It's time to upload the Excel template and your zip file containing all your fastq (or fastq.gz) files.


