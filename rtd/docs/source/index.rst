Research Activity Identifier (RAiD) Metadata Schema
===================================================

Research Activity Identifier (RAiD) is a globally unique, persistent identifier (PID) system used for identifying research projects and activities. The RAiD system relies on a RAiD metadata schema that enables any research project or activity to be identified globally and linked to in research citations.

What is a RAID?
---------------

Each RAiD comprises 2 parts:
1. a unique RAiD name, which is the Digital Object Identifier (DOI)
2. a metadata record.

A **RAiD name** will always start with the digits '10' and contain a prefix-slash-suffix using a string of numbers and letters (e.g. `<https://raid.org/102.100.100/62855>`_).

A RAiD's **metadata record** links various components (e.g. contributors, organisations, grants, instruments, publications, datasets) to a project via their own pre-existing PIDs where available (e.g. ORCiDs, RORs, Crossref or DataCite DOIs). These components are only linked to the project itself and not with each other (e.g. a RAiD contributor is not linked with a RAiD organisation).

RAiDs contain project information not found in other PIDs (e.g. a project's title, start date, description or subject), yet they do not duplicate information used in other PIDs either.

RAiDs can also be linked to one another using arbitrary qualified relationships so that (e.g.) subprojects can be created.

The RAiD system was developed by the `Australian Research Data Commons (ARDC) <https://www.ardc.edu.au>`_ and has been standardised for international use by `ISO 23527, Information and Documentation — Research Activity Identifier (RAiD) <https://www.iso.org/standard/75931.html>`_.

RAiD Metadata Schema conventions used
-------------------------------------

'Core', 'extended' and 'local' metadata schema components
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The RAiD metadata schema is divided into 3 components:
1. core
2. extended
3. local.

The  **Core** component refers to metadata properties and controlled lists that are standardised across all RAiD Registration Agencies. If a Registration Agency uses its own controlled lists, it must provide a cross-walk to the RAiD's standardised core terms.

The **Extended** component refers to properties that are standardised across all Registration Agencies, but their controlled lists may vary. A Registration Agency may use its own controlled lists, but it must first:
* publish each list in a machine-readable format, preferably on a vocabulary service (Note: the ARDC can assist with this requirement)
* register the controlled list(s) with the ARDC as the RAID's ISO 23527 Registration Authority (RAu). Re-use of an existing published controlled list is acceptable. as long as it is published in machine-readable format.

The **Local** components refers to properties and controlled lists that are entirely under the control of a Registration Agency, and only need to be reported to the ARDC (RAu) annually or whenever major changes are made. Local properties can be tailored to meet the needs of the research community served by the Registration Agency. However, a mechanism must be put in place by the Registration Agency to enable useful local metadata properties to be promoted into extended metadata, or extended properties into core metadata.

Component blocks
^^^^^^^^^^^^^^^^

Within each metadata schema component, the metadata properties are divided into groups or 'blocks' of related properties.

Property block descriptions
^^^^^^^^^^^^^^^^^^^^^^^^^^

All property block descriptions include these elements:

.. csv-table:: Example :rst:dir:`csv-table`

   "**Definition**", "briefly defines the property"
   "**Requirement**",               "indicates whether a property is mandatory, recommended or optional, with additional information where necessary (e.g., if a property is mandatory only if another property is present)"
   "**Occurrence**",               "indicates the number of times a property may occur:

* 0 represents a recommended or optional property that may only occur once
* 0-n represents an optional property that may occur multiple times
* 1 represents a required property that may only occur once
* 1-n represents a required property that may occur multiple times"
   "**Allowed values**",               "will either indicate a controlled list of values limiting input (as a bulleted list), or rules governing the values (as an italicised statement followed by format and constraints).
"

**Definition** briefly defines the property

**Requirement** indicates whether a property is mandatory, recommended or optional, with additional information where necessary (e.g., if a property is mandatory only if another property is present)

**Occurrence** indicates the number of times a property may occur:

* 0 represents a recommended or optional property that may only occur once
* 0-n represents an optional property that may occur multiple times
* 1 represents a required property that may only occur once
* 1-n represents a required property that may occur multiple times

**Allowed values** will either indicate a controlled list of values limiting input (as a bulleted list), or rules governing the values (as an italicised statement followed by format and constraints).

In addition, some properties include additional information:

**Format** illustrates how a value should be formed (e.g. dates are formatted YYYY-MM-DD)

**Examples** provide models for the value.

**Note** any additional information about the property.


.. note::

   This project is under active development by the ARDC

Contents
--------

.. toctree::

   core/core
      core/identifier
      core/dates
      core/titles
      core/descriptions
      core/contributors
      core/organisations
      core/relatedObjects
      core/alternateIdentifiers
      core/alternateUrls
      core/relatedRaids
      core/access
   extended/extended
      extended/subjects
      extended/traditionalKnowledgeLabels
      extended/spatialCoverages