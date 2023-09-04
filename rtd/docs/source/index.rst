Research Activity Identifier (RAiD) Metadata Schema
===================================================

A *Research Activity Identifier* (RAiD) is a globally unique, persistent identifier (PID) for research projects or activities. It consists of a unique identifier (a DOI) and a metadata record. The metadata record links various components (e.g., contributors, organisations, grants, instruments, publications, datasets, etc.) to the project, via their own PIDs where available (e.g., ORCiDs, RORs, Crossref or Datacite DOIs, etc.). These components are only linked to the project itself; a RAiD does not assert links between components (e.g., contributors to organisations). RAiDs also contain project information not found elsewhere, such as project title, start date, description, and subject. RAiDs do not, however, duplicate information found elsewhere. Finally, RAiDs can be linked to one another using arbitrary qualified relationships so that, e.g., subprojects can be created. 

RAiD has been developed by the Australian Research Data Commons (ARDC). 

Conventions
-----------

Core, extended, and local metadata components
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The RAiD metadata schema is divided into three components: core, extended, and local. **Core** metadata properties and controlled lists are standardised across all Registration Agencies. If a Registration Agency employs its own contolled lists, it must provide a cross-walk to the standardised terms. **Extended** properties are standardised across all Registration Agencies, but controlled lists may vary. A Registration Agency can employ it's own controlled lists, but (a) must publish the list in a machine-readable format, preferrably on a vocabulary service (the ARDC can assist with this requirement), and (b) register the controlled list with the Registration Authority. Re-use of an existing, published controlled list is acceptable so long as it is published in machine-readable format. **Local** properties and controlled lists are entirely under the control of a Registration Agency, and only need to be reported to the Registration Authority annually (or when major changes are made). Local properties can be tailored to meet the needs of the community served by the Registration Agency. A mechanism will be put in place by the Registration agency to promote useful local properties into extended metadata, or extended properties into core metadata. For more information, please contact the ARDC.

Blocks
^^^^^^

Within each component, metadata properties are divided into blocks of related properties. 

Property descriptions
^^^^^^^^^^^^^^^^^^^^^

All property descriptions include a number of elements:

**Definition** briefly defines the property

**Requirement** indicates whether a property is mandatory, recommended, or optional, with additional information where necessary (e.g., if the property is mandatory only if another property is present)

**Occurrence** indicates the number of times a property may occur:

* 0 represents a recommended or optional property that may only occur once
* 0-n represents an optional property that may occur multiple times
* 1 represents a required property that may only occur once
* 1-n represents a required property that may occur multiple times

**Allowed values** will either indicate a controlled list of values limiting input (as a bulleted list), or rules governing the values (as an italicised statement followed by format and constraints).

In addition, some properties include additional information:

**Format** illustrates how a value should be formed, e.g., that dates are formatted YYYY-MM-DD.

**Examples** provide models for the value.

**Note** any additional information about the property.


.. note::

   This project is under active development.

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