.. _Database Structure:


MSD Database Structure
======================


MSD database has a hierarchical structure. We have the concepts of **Projects**, **Organisms**, **Samples**, and **Datasets**.
As a user has defined a project, the new project can host various *organisms*, *samples* and *datasets*. A defined *organism*
can have several samples assigned to and similarly each *sample* might have various *datasets*.

Imgaine this hypothetical situation: as a researcher you might have project in which you have three mice.
In this case each mouse would be an *organism* at MSD. Suppose that you plan to compare two types of samples 
(colon biopsy and feces) and two microbiome analysis methods (16S amplicon and Shotgun sequencing). In 
order to achieve this you need to attempt one sampling for each sample type and get enough sample for 
each sample type to send for different sequencing methods. It means that you would take 2 samples from each mouse 
and produce 2 datasets from each sample. Thus, you need to define all your mice as *organism* at MSD and 
for each of them define only **2** *samples* for which **2** *datasets* would get generated and uploaded to MSD. The table below
shows the case.

.. _Concepts Relaion:
.. csv-table:: Relation of entities at MSD
   :header: "No.", "Project", "Organism", "Sample", "Dataset Type"
   :widths: 5, 10, 10, 20

   "1", "My_Project", "Mouse_1", "M1_Biopsy_1", "M1_Biopsy_1_16S"
   "2", "My_Project", "Mouse_1", "M1_Biopsy_1", "M1_Biopsy_1_shotgun"
   "3", "My_Project", "Mouse_1", "M1_feces_1", "M1_feces_1_16S"
   "4", "My_Project", "Mouse_1", "M1_feces_1", "M1_feces_1_Shotgun"
   "5", "My_Project", "Mouse_2", "M2_Biopsy_1", "M2_Biopsy_1_16S"
   "6", "My_Project", "Mouse_2", "M2_Biopsy_1", "M2_Biopsy_1_Shotgun"
   "7", "My_Project", "Mouse_2", "M2_feces_1", "M2_feces_1_16S"
   "8", "My_Project", "Mouse_2", "M2_feces_1", "M2_feces_1_Shotgun"
   "9", "My_Project", "Mouse_3", "M3_Biopsy_1", "M3_Biopsy_1_16S"
   "10", "My_Project", "Mouse_3", "M3_Biopsy_1", "M3_Biopsy_1_Shotgun"
   "11", "My_Project", "Mouse_3", "M3_feces_1", "M3_feces_1_16S"
   "12", "My_Project", "Mouse_3", "M3_feces_1", "M3_feces_1_Shotgun"

The table above shows that each mouse has 4 samples and each sample has 2 datasets. In total, there are 12 datasets.

.. include:: MSD-ID_explanations.rst

.. note::
   Definition of a *sample* refers to each attempt of sampling. For example, two samples, both taken from
   feces, at the same time point would be considered two distinguished samples so that two different sample 
   objects at MSD.


.. image:: /media/crc_base.jpg
   :scale: 100 %
   :alt: MSD Database Structure
