MSD
===

.. _database_structure:

Database Structure
------------------

MSD databse has a hierarchical structure. We have concepts of Projects, Organisms, Samples, and Datasets.
As a user has defined a project, the new project can host various organisms. Similarly a defined organism
can have several samples assigned to. From each defined sampels one can produce various datasets and have
assigned to the sample. For example: as a researcher you might have project in which you have several mice.
In this case each each mouse would be an *organism* at MSD. Suppose that you plan to compare two sampling
methods (biopsy and faeces) and two microbiome anlaysis methods (16S amplicon and Shotgun sequencing). In 
order to achieve this you need to attempt one sampling for each sampling method and get enough sample for 
each to send for different sequencing strategies. It means that you would take 2 samples from each mouse 
and produce 2 datasets from each sample. Thus, you need to define all your mice as *organism* at MSD and 
for each define only 2 *samples* for each organism and 2 *datasets* for each sample.


.. note::
   The definion of a *sample* refers to each attempt of sampling. For example, two samples, both taken from
   faeces, at the same timepoint would be considered two distintuished samples so that two differnt sample 
   objects at MSD.

.. image:: media/pics/crc_base.jpg
   :width: 400
   :alt: MSD Database Structure
