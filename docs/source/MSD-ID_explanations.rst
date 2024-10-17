.. _MSD-ID-Explanation:

MSD IDs Explanation
-------------------

In MSD database, each entity has a unique ID. This ID is used to identify the entity in the database. For example, a project has a unique ID, an organism has a unique ID, a sample has a unique ID, and a dataset has a unique ID called **MSD ID**. 
Taking the example in :ref:`MSD Database Structure <Database Structure>`, we have 12 datasets in total for their corresponding project. According :ref:`MSD Database Structure <Database Structure>`, these 12 datasets should belong to some samples 
and some organisms and ultimately to a project. For each entity in the table :ref:`Relation of entities at MSD <Concepts Relaion>`, there is a unique ID. The table below shows the unique IDs for each entity.

.. _MSD IDs Explanation Table:
.. csv-table:: MSD IDs for each entity
   :header: "Entity Name", "Entity Type", "Entity Explanation","Short MSD ID", "Long MSD ID", "ID Explanation"
   :widths: 5, 10, 10, 20

    "My_Project", "Project", "Your defined project to which you have uploaded datasets", **"P1"**, **"P1"**, "Project ID starts with **P** followed by a number"
    "Mouse_1", "Organism", "Mouse number 1 for which you generate data in the project ", **"O1"**, **"P1O1"**, "Organism ID starts with **O** followed by a number. Long ID includes project ID as well."
    "Mouse_2", "Organism", "Mouse number 2 for which you generate data in the project ", **"O2"**, **"P1O2"**, "Organism ID starts with **O** followed by a number. Long ID includes project ID as well."
    "Mouse_3", "Organism", "Mouse number 3 for which you generate data in the project ", **"O3"**, **"P1O3"**, "Organism ID starts with **O** followed by a number. Long ID includes project ID as well."
    "M1_Biopsy_1", "Sample", "Biopsy sample number 1 from Mouse number 1", **"S1"**, **"P1O1S1"**, "Sample ID starts with **S** followed by a number. Long ID includes organism ID as well."
    "M2_Biopsy_1", "Sample", "Biopsy sample number 1 from Mouse number 2", **"S2"**, **"P1O2S5"**, "Sample ID starts with **S** followed by a number. Long ID includes organism ID as well."
    "M3_Biopsy_1", "Sample", "Biopsy sample number 1 from Mouse number 3", **"S3"**, **"P1O3S9"**, "Sample ID starts with **S** followed by a number. Long ID includes organism ID as well."
    "M1_feces_1", "Sample", "Feces sample number 1 from Mouse number 1", **"S4"**, **"P1O1S4"**, "Sample ID starts with **S** followed by a number. Long ID includes organism ID as well."
    "M2_feces_1", "Sample", "Feces sample number 1 from Mouse number 2", **"S5"**, **"P1O2S5"**, "Sample ID starts with **S** followed by a number. Long ID includes organism ID as well."
    "M3_feces_1", "Sample", "Feces sample number 1 from Mouse number 3", **"S6"**, **"P1O3S11"**, "Sample ID starts with **S** followed by a number. Long ID includes organism ID as well."
    "M1_Biopsy_1_16S", "Dataset", "16S amplicon dataset from biopsy sample number 1 from Mouse number 1", **"D1"**, **"P1O1S1D1"**, "Dataset ID starts with **D** followed by a number. Long ID includes sample ID as well."
    "M1_Biopsy_1_Shotgun", "Dataset", "Shotgun dataset from biopsy sample number 1 from Mouse number 1", **"D2"**, **"P1O1S1D2"**, "Metagenomics (i.e: shotgun) dataset ID starts with **DM** followed by a number. Long ID includes sample ID as well."
    "M1_feces_1_16S", "Dataset", "16S amplicon dataset from feces sample number 1 from Mouse number 1", **"D3"**, **"P1O1S4D3"**, "Dataset ID starts with **D** followed by a number. Long ID includes sample ID as well."
    "M1_feces_1_Shotgun", "Dataset", "Shotgun dataset from feces sample number 1 from Mouse number 1", **"D4"**, **"P1O1S4D4"**, "Metagenomics (i.e: shotgun) dataset ID starts with **DM** followed by a number. Long ID includes sample ID as well."
    "M2_Biopsy_1_16S", "Dataset", "16S amplicon dataset from biopsy sample number 1 from Mouse number 2", **"D5"**, **"P1O2S5D5"**, "Dataset ID starts with **D** followed by a number. Long ID includes sample ID as well."
    "M2_Biopsy_1_Shotgun", "Dataset", "Shotgun dataset from biopsy sample number 1 from Mouse number 2", **"D6"**, **"P1O2S5D6"**, "Metagenomics (i.e: shotgun) dataset ID starts with **DM** followed by a number. Long ID includes sample ID as well."
    "M2_feces_1_16S", "Dataset", "16S amplicon dataset from feces sample number 1 from Mouse number 2", **"D7"**, **"P1O2S8D7"**, "Dataset ID starts with **D** followed by a number. Long ID includes sample ID as well."
    "M2_feces_1_Shotgun", "Dataset", "Shotgun dataset from feces sample number 1 from Mouse number 2", **"D8"**, **"P1O2S8D8"**, "Metagenomics (i.e: shotgun) dataset ID starts with **DM** followed by a number. Long ID includes sample ID as well."
    "M3_Biopsy_1_16S", "Dataset", "16S amplicon dataset from biopsy sample number 1 from Mouse number 3", **"D9"**, **"P1O3S9D9"**, "Dataset ID starts with **D** followed by a number. Long ID includes sample ID as well."
    "M3_Biopsy_1_Shotgun", "Dataset", "Shotgun dataset from biopsy sample number 1 from Mouse number 3", **"D10"**, **"P1O3S9D10"**, "Metagenomics (i.e: shotgun) dataset ID starts with **DM** followed by a number. Long ID includes sample ID as well."
    "M3_feces_1_16S", "Dataset", "16S amplicon dataset from feces sample number 1 from Mouse number 3", **"D11"**, **"P1O3S11D11"**, "Dataset ID starts with **D** followed by a number. Long ID includes sample ID as well."
    "M3_feces_1_Shotgun", "Dataset", "Shotgun dataset from feces sample number 1 from Mouse number 3", **"D12"**, **"P1O3S11D12"**, "Metagenomics (i.e: shotgun) dataset ID starts with **DM** followed by a number. Long ID includes sample ID as well."


Datasets ID prefix
^^^^^^^^^^^^^^^^^^

Various datasets types in MSD have different prefixes. For example, 16S amplicon datasets have a prefix **D** and shotgun datasets have a prefix **DM**. This is to differentiate between different types of datasets.

.. _Datasets ID prefix Table:
.. csv-table:: Datasets ID prefix
   :header: "Dataset Type", "ID Prefix"
   :widths: 20, 20

    "16S amplicon dataset", **"D"**
    "Metagenomics (i.e: shotgun) dataset", **"DM"**
    "Targeted metaboloimcs dataset", **"DTM"**
    "Untargeted metaboloimcs dataset", **"DUM"**
    "Metatranscriptomics dataset", **"DTR"**
    "Metaproteomics dataset", **"DPR"**


