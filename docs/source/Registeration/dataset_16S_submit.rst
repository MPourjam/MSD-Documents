.. _16S Dataset Register:


16S Dataset Registration
========================


So far organisms and samples taken from them are registered at MSD and it's time to register datasets produced from samples. As explained in :ref:`Database Structure`,
from each sample taken several dataset could be produced. For example, you can take a sample by *biopsy* and produce *16S rRNA gene amplicon* dataset by sending some of it 
to for sequencing and from the same sample producing metabolomics data.

In this part we explain the last step of dataset registration for **16S rRNA** amplicon sequences.

The steps we take, as it was for sample and organism registration, are **Creating** a template, **Filling** the template, **Preparation** of fastq files,and **Uploadin** the template. For dataset uploading, 
we also upload the raw files needed to get processed with the template.


I. Create Template
^^^^^^^^^^^^^^^^^^

**16S rRNA** datasets excel template can be created by going to **Submit** tab -> **Datasets** subtab -> **16S** -> **Create Template**.
By clicking on **Create Dataset Template** and you will have an excel template downloaded.



II. Fill in the Template
^^^^^^^^^^^^^^^^^^^^^^^^

Now that we have the excel template download we need to fill each of rows in the excel template for each of datasets produced from our sample.


.. note::
    The first two columns of dataset excel template are important (**DIS_Sampling_ID** and **Sample_ID**). You can for each dataset you are 
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
* **Forward_Filename**: If your sequncing layout is *paired-end* then your forward sequence read file's name goes here. Provide the **exact** and **full name** of your file. If 
    you have not had your samples sequenced paired-end, then you will have one file whose full name you need to provide here.
* **Backward_Filename**: If your sequncing layout has been *paried-end* then no need to provide a file name here. Otherwise, provide the *full name* of your *reverse* reads file.
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
* **Sample_Type**: Type of sample to sent for seuqncing.
* **Custom_1**: After **Sample_Type** column you can add your desired columns and corresponding values to each of your dataset and have them stored 
    at MSD.
* **Custom_2**: After **Sample_Type** column you can add your desired columns and corresponding values to each of your dataset and have them stored 
    at MSD.


III. Preparation of fastq files.
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Now that you have your template ready. It's time to prepare zip file of your fastq files for uploading.
Your zip file should contain your *fastq files* (all you have put their file names in the excel template, 
*Forward_Filename* and *Backward_Filename*). The zip file should **NOT** contain any folders inside. 
By opening the zip file you should only see the fastq (or fastq.gz) files. 


III. Uploading Template
^^^^^^^^^^^^^^^^^^^^^^^


It's time to upload the excel template and your zip file containing all your fastq (or fastq.gz) files.


