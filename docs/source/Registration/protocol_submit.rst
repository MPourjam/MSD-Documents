.. _Register Protocol:


Defining Protocols
------------------


Different projects might have different protocols for **Sampling**, **Sequencing**, **Analysis**, **Preparation**, etc.
Each sample and dataset which is to be submitted to MSD should have a protocol assigned. Before registration of organisms,
samples, and datasets to MSD you need to have the protocols you used for sample *preparation*, *sampling* as well as protocols
used for *Sequencing* and *Analysis*.


There are already some common protocols available at MSD which you can view and download at :ref:`Protocol View` tab.

The definition of different proton helps you with protocol definition.

* **Preparation Protocol**: This protocol refers to steps you have taken until your organism is prepared for sampling.
* **Sampling Protocol**: This protocol refers to steps taken to get samples for measurement (i.e: sequencing).
* **Sequencing Protocol**: This protocol refers to steps taken after sampling utility a library is prepared for sequencing.
  If you have had your samples sequenced by **CFM** [2]_ then you don't need to define any *Sequencing* protocols, and you can use the one provided by MSD: *Sequencing_protocol_Default*
* **Analysis Protocol**: This protocol refers to steps taken for processing the sample you have uploaded to MSD.
  As all your 16S amplicon sequences get analyzed at MSD, you don't need to define any *Analysis* protocols and can use the one provided by MSD: *Analysis_protocol_Default*

.. figure:: /media/Protocol_Register_Form.png
    :align: center
    :scale: 100 %
    :alt: Protocol Register Form
    :class: prot_registration_scsh

    An example of protocol creation form.


  

If your protocol is an extension to other protocol, you can make it related to other protocol by 
clicking on **Extension** and choosing one of **already submitted** protocols at MSD.

.. figure:: /media/Protocol_Register_Form_Extension.png
    :align: center
    :scale: 100 %
    :alt: Protocol Extension Register Form
    :class: prot_registration_scsh

    An example of extending a protocol.

 
