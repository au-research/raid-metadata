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

RAiD Metadata Schema conventions
--------------------------------

'Core', 'extended' and 'local' metadata schema components
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The RAiD metadata schema is divided into 3 components:

1. core
2. extended
3. local

The  **Core** component refers to metadata properties and controlled lists that are standardised across all RAiD Registration Agencies. Controlled lists are 'closed' and may not be altered. If a Registration Agency substitutes its own controlled lists, it must provide a cross-walk to the RAiD's standardised core terms. Properties may not be altered.

The **Extended** component refers to properties that are standardised across all Registration Agencies, but where controlled lists may vary. A Registration Agency may ammend the controlled list (lists are 'open'), or substitute its own controlled list entierely. In either case, it must:
* Publish each non-standard list in a machine-readable format, preferably on a vocabulary service (the ARDC can assist with this requirement). Re-use of an existing published controlled list is acceptable. as long as it is published in machine-readable format.
* Register the controlled list(s) with the ARDC as the RAID's ISO 23527 Registration Authority (RAu). 
Properties may not be altered.

The **Local** components refers to properties and controlled lists that are entirely under the control of Registration Agencies, and only need to be reported to the ARDC (RAu) annually or when major changes are made. Local properties can be tailored to meet the needs of the research community served by the Registration Agency. The Registration Authority will provide a system enabling local metadata properties to be promoted into extended metadata if they are found broadly useful.

Component blocks
^^^^^^^^^^^^^^^^

Within each metadata schema component, the metadata properties are divided into groups or 'blocks' of related properties.

Sub-blocks
^^^^^^^^^^

Sub-blocks contain no values, but instead bundle tightly bound properties together, for example, a recurring 'language' sub-block includes language code, language code scheme, and language code scheme URL. 

Properties
^^^^^^^^^^^

Each metadata property is described with the following characteristics:

**Definition** briefly defines the property

**Requirement** indicates whether a property is mandatory, recommended or optional, with additional information where necessary (e.g., if a property is mandatory only if another property is present)

**Occurrence** indicates the number of times a property may occur:

* 0 represents a recommended or optional property that may only occur only once
* 0-n represents an optional property that may occur one or many times
* 1 represents a required property that may only occur only once
* 1-n represents a required property that may occur one or many times

**Allowed values** will either indicate a controlled list of values limiting input (as a bulleted list), or rules governing the values (as an italicised statement followed by format and constraints). Controlled lists are described as 'open' if Registration Agencies can add new terms to them, with the only restriction being that the Registration Authority must be notified. Such lists are 'closed' if they cannot be altered by Registration Agencies, in which cases changes must be proposed during the normal metadata review cycle. 

In addition, some properties include additional information:

**Default** represents a prefilled value set by the system, which can usually (but not always) be changed by the user. If only one value appears in the controlled list, it is automatically the default.

**Format** illustrates how a value should be formed (e.g. dates are formatted YYYY-MM-DD).

**Constraints** are further limits or requirements governing 'Allowed values'.

**Examples** provide models for the value.

**Example JSON** provides an indicative JSON code snippet.

**Note** contains any additional information about the property.


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