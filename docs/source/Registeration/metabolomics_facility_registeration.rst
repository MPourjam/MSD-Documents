.. _Register Metabolomics Dataset:

==================================
Submission of Metabolomics Dataset
==================================


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
        and the unit of values in the next row. There should be values of the corresponsing metabolites in the 
        rows related to each of your samples. In case of not having values for a specific metabolites in a 
        sample value **N/A** should be placed. (See figure of second metabolites example excel)
.. figure:: /media/MetabolitesExcelScreenShot1.png
    :align: center
    :scale: 100 %
    :alt: An examle of metabolites excel you will receive from metabolomic facility
    :class: metabolites_submission
    This 



.. figure:: /media/MetabolitesExcelScreenShot2.png
    :align: center
    :scale: 100 %
    :alt: An examle of metabolites excel with added custom metabolites
    :class: metabolites_submission


MSD database schema tries to comply with every usual research project which starts with defining a project.
Similarly, the first step at MSD is alos creation of a project to which all your samples would be assigned.
In order to to that follow the steps below.

Under **Submit** tab:

#. Click on **Project**
#. Give your project a **Name**
#. If you have your project already registered at `SRA <https://www.ncbi.nlm.nih.gov/sra>`_ [1]_ and you have an *accession* assigned, you can give it as **Accession** field to your project.
#. You can also give your project an **Acronym** for ease of use. Leaving it empty means no acronym for you project.
#. **Crceator** is the owner of project. You have to select your *username*.
#. You *should* give your project **Description**. The more you are descriptive, the more your project would get appreared in your searches for datasets within various projects you have.
#. **Availability** Checkbox will make other users of MSD able to see the description of your project in their :ref:`Dashboard` and ask for permission to have access to your project datasets.
#. Click on **Create Project** to finalize the project creation.

.. figure:: /media/Project_Register_Form.png
    :align: center
    :scale: 100 %
    :alt: Project Register Form
    :class: prj_registration_scsh

    An example of project creation form. After new project is created you will be redirected to :ref:`Datasets 16S View`.

