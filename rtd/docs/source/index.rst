Research Activity Identifier (RAiD) Metadata Schema
===================================================

The RAiD Metadata Schema is a way of organising data elements that are common to minted RAiD names. It is the overall structure by which each RAiD metadata component and its properties are ordered, defined and standardised across all RAiD names.
The RAiD Metadata Schema specifies things like:

* the type and number of data elements recorded (e.g. dates, names and places)
* the designation of 'mandatory', 'recommended' and 'optional' fields
* encoding requirements
* use of that data content (e.g. controlled, uncontrolled, open or closed data lists)
* elements that are specific to a particular type of use (e.g. different types of schema)
* the vocabulary source for a particular property
* instructions on how to add another type of vocabulary.

The RAiD Metadata Schema underpins how RAiD names are identified, minted, resolved, updated and tracked via their metadata records. Any research project or activity with a RAiD name can be related to another RAiD or identified via the RAiD system, as well as cited in research documentation.

The RAiD system is developed by the Australian Research Data Commons (ARDC). In December 2022, the RAiD system was standardised for international use in `ISO 23527, Information and Documentation — Research Activity Identifier (RAiD) <https://www.iso.org/standard/75931.html>`_

RAiD Metadata Schema conventions used
-------------------------------------

'Core', 'extended' and 'local' metadata schema components
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The RAiD metadata schema is divided into 3 components:
<<<<<<< HEAD

1. core
2. extended
3. local
=======
>>>>>>> 9fbbfc1b73b5a426172d45134e980eaa2ac54e5a

#. core
#. extended
#. local.

**Core** components refer to metadata properties and controlled lists that are standardised across all RAiD Registration Agencies. If a Registration Agency uses its own controlled lists, it must provide a crosswalk to the RAiD's standardised core terms.

**Extended** components are properties that are standardised across all Registration Agencies, but their controlled lists may vary. A Registration Agency may use its own controlled lists, but it must first:

#. Publish each list in a machine-readable format, preferably on a vocabulary service (**Note**: the ARDC can assist with this requirement)
#. Register the controlled list(s) with the ARDC as the RAiD's ISO 23527 Registration Authority (RAu). Re-use of an existing published controlled list is acceptable. as long as it is published in machine-readable format.

**Local** components are properties and controlled lists that are entirely under the control of a Registration Agency, and only need to be reported to the ARDC (RAu) annually or whenever major changes are made. Local properties can be tailored to meet the needs of the research community served by the Registration Agency. However, a mechanism must be put in place by the Registration Agency to enable useful local metadata to be promoted into extended metadata, or extended properties into core metadata.

Component blocks
^^^^^^^^^^^^^^^^

Within each metadata schema component, the metadata properties are divided into groups or 'blocks' of related properties.

Block descriptions
^^^^^^^^^^^^^^^^^^

Sub-blocks contain no values, but instead bundle tightly bound properties together, for example, a recurring 'language' sub-block includes language code, language code scheme, and language code scheme URL. 

.. csv-table::

   "**Definition**", "briefly defines the property"
   "**Requirement**", "indicates whether a property is mandatory, recommended or optional, with additional information included where necessary (e.g. if a property is mandatory when only another property is present)"
   "**Occurrence**",  "indicates the number of times a property may occur:

<<<<<<< HEAD
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
=======
   * 0 – represents a recommended or optional property that may only occur once
   * 0-n – represents an optional property that may occur multiple times
   * 1 – represents a required property that may only occur once
   * 1-n – represents a required property that may occur multiple times
    
   "
   "**Allowed values**", "will indicate a controlled list of values' limiting input (such as a bulleted list) or the rules that govern those values (such as an italicised statement followed by format and constraints)"

In addition, some properties include additional information:

.. csv-table::

   "**Format**", "illustrates how a value should be formed (e.g. dates are formatted YYYY-MM-DD)"
   "**Examples**", "provide models for the value."
   "**Contraints**", "provide limitations for the value"
   "**Note**", "any additional information about the property."
>>>>>>> 9fbbfc1b73b5a426172d45134e980eaa2ac54e5a


.. note::

   This RAiD project is under active development by the ARDC.

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