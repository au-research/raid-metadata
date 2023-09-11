.. autosummary::
   :toctree: generated

.. _4-description:

4 description
==============

**Definition**: a metadata schema block containing the description of the RAiD and associated properties.

**Requirement**: recommended

**Occurrence**: 0-n

**Example JSON**

.. _4.1-description.text:

4.1 description.text
--------------------

**Definition**: a project description that may include any additional information that does not fit in the other categories

**Requirement**: mandatory for each description supplied

**Occurrence**: 0-1

**Allowed values**: free text

**Constraints**: maximum 1000 characters

. 4.2-description.type:

4.2 description.type
--------------------

**Definition**: a metadata schema block declaring the type of description.

**Requirement**: mandatory for each description supplied

**Occurrence**: 1

**Example JSON**

.. _4.2.1-description.type.id:

4.2.1 description.type.id
^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the type of description.

**Requirement**: mandatory for each description.type supplied

**Occurrence**: 0-1

**Allowed values**: *controlled list derived from description.type.schemaUri*

* Primary (*preferred full description or abstract*)
* Alternative (*additional full description or abstract*)
* Brief
* Significance Statement
* Methods
* Objectives
* Other (*any other descriptive information, e.g. a note or similar*)

**Note**: if a description is provided, a single primary description is mandatory while additional Descriptions are optional. The type is mandatory for each description specified. The controlled list adapted from Vocabularies for Registry Schema 1.6.5 'Description Type' and DataCite Metadata Schema 4.4 Appendix 1 Table 10 'descriptiontype'.

.. _4.2.2-description.type.id.schemaUri:

4.2.2 description.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the description type schema

**Requirement**: mandatory for each description.type.id supplied

**Occurrence**: 0-1

**Allowed values**: *closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: the RAiD vocabulary on RVA is specified for https://raid.org and used by the ARDC RAiD service; Registration Agencies may implement other controlled vocabularies but they must provide a crosswalk. In 'core' elements like this one where variation of controlled vocabularies among Registration Agencies occurs, the RAiD service should return the 'local' term and schema as well as the 'standardised' term and schema.

.. _4.3-description.language:

4.3 description.language
------------------------

**Definition**: a metadata schema block declaring the language of the description text

**Requirement**: recommended

**Occurrence**: 0-1

**Example JSON**

.. _4.3.1-description.languageId:

4.3.1 description.language.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the language used for the description text identified by a code or other identifier

**Requirement**: recommended

**Occurrence**: 0-1

**Allowed values**: *controlled list derived from titles.language.schemaUri*

**Example**: ``eng`` (*ISO 649-3's 3-letter code*)

**Note**: Currently limited to ISO 649-3's 3-letter code.

.. _4.3.1-description.languageId.schemaUri:

4.3.2 description.language.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the language identifier schema

**Requirement**: mandatory for each description.language.id supplied

**Occurrence**: 0-1

**Allowed values**: *controlled list*

* ``https://www.iso.org/standard/49544.html``

**Note**: the controlled list is shared across all Registration Agencies. No crosswalk - queries return language code and scheme URI. 
