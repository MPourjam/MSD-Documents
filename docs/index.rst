==================================
MSD (Microbial Signature Database)
==================================

**Microbial Signatures Database** (MSD) aims to assist biological consortia and laboratories with handling,
storing, analyzing and sharing their data of interest. We aim to provide a solution that safely stores sensitive
and non-sensitive data, enables their search by using custom filters, runs analyses that each user can tune to suit
their needs and finally gives the opportunity for each member of the platform to share the raw data and the results
with all other members of the platform. By using cutting-edge technologies, this platform guarantees the safety and
resilience of the deposited data, while simultaneously creating an intuitive and all-inclusive enviroment.
This platform is currently being financed by the grant: `CRC 1371 <https://www.sfb1371.tum.de/>`_.

Having access to MSD will enable the researchers benefit from standardized metadata storage, integrated collection of 
data (16S, 18S, ITS, Metagenomics, Proteomics, Metabolomics, Transcriptomics), and project management using only one platform.


.. note::

   This project is under active development and thus it is subject to change.



.. toctree::
   :maxdepth: 3
   :caption: Explore The Documentation

   source/general_exp
   source/quickstart
   source/View/views_all
   source/View/analysis_result

Prequisites for uploading the datasets
-------------------------------
   There are some steps in using MSD that are trivial but take time if not thought of in advance. 
   Below is a comprehensive list of such steps to aleviate any potential delays:
   #. The users must be a member of CRC1371 consortium to get registrated. 
   #. After the initial registration there will be a waiting time for confirmation of the account manually performed by MSD that
      will not start till the user confirms the email address, so make an account in advance. It is also helpful to put information
      in the **Activation Reason** field to speed up the confirmation process.
   #. Define organisms at MSD at the same time as the project they will be investigated in.
   #. Define separate samples for each sampling attempt.
   #. The Data provided in the samples must correspond to the status at the time of taking the sample.
   #. For each of the 16S datasets ask the sequencing facility to provide the information about forward and reverse primers used in the sequencing.
      The information is required to registrate this datasets for MSD.
   #. For registration of a metabolomics dataset it is required to be registered as a metabolomics group operator at MSD.  So contact MSD administrator to be added in this group as soon as possible. 
   #. It is recommended to submit metabolomics sample to MSD before sending it in to the metabolomics lab. Using the MSD ID for the
      metabolomics run will help the further process of analysis and will help the user find the needed datsets with **Advanced Search**
   #. Get the information about what normalization methods the metabolomics facility used.
