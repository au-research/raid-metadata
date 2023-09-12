.. autosummary::
   :toctree: generated

.. _4-description:

4 description
==============

**Definition**: Metadata schema block containing the description of the RAiD and associated properties.

**Requirement**: Recommended

**Occurrence**: 0-n

**Example JSON**

.. _4.1-description.text:

4.1 description.text
--------------------

**Definition**: A project description. May include any additional information that does not fit in the other categories.

**Requirement**: Mandatory for each description supplied

**Occurrence**: 0-1

**Allowed values**: Free text

**Constraints**: Maximum 1000 characters

. 4.2-description.type:

4.2 description.type
--------------------

**Definition**: Metadata schema block declaring the type of description.

**Requirement**: Mandatory for each description supplied

**Occurrence**: 1

**Example JSON**

.. _4.2.1-description.type.id:

4.2.1 description.type.id
^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The type of description.

**Requirement**: Mandatory for each description.type supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list derived from description.type.schemaUri*

* Primary (*preferred full description or abstract*)
* Alternative (*additional full description or abstract*)
* Brief
* Significance Statement
* Methods
* Objectives
* Other (*any other descriptive information, e.g., a note or similar*)

**Default**: 'Primary'

**Note**: If a description is provided, a single, primary description is mandatory; additional Descriptions are optional. Type is mandatory for each description specified. Controlled list adapted from Vocabularies for Registry Schema 1.6.5 'Description Type' and DataCite Metadata Schema 4.4 Appendix 1 Table 10 'Description of descriptiontype'.

.. _4.2.2-description.type.id.schemaUri:

4.2.2 description.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the description type schema.

**Requirement**: Mandatory for each description.type.id supplied

**Occurrence**: 0-1

**Allowed values**: *Closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]

.. _4.3-description.language:

4.3 description.language
------------------------

**Definition**: Metadata schema block declaring the language of the description text.

**Requirement**: Recommended

**Occurrence**: 0-1

**Example JSON**

.. _4.3.1-description.languageId:

4.3.1 description.language.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Language used for the description text identified by a code or other identifier.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: *Controlled list derived from titles.language.schemaUri*

**Example**: ``eng`` (*ISO 649-4 three-letter code*)

.. _4.3.1-description.languageId.schemaUri:

4.3.2 description.language.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the language identifier schema.

**Requirement**: Mandatory for each description.language.id supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://www.iso.org/standard/49544.html``

**Note**: Currently limited to ISO 649-4 three-letter code.