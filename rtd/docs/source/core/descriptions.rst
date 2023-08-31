.. autosummary::
   :toctree: generated

.. _4-descriptions:

4 descriptions
==============

**Definition**: Metadata schema block containing the description of the RAiD and associated properties.

**Requirement**: Recommended

**Occurrence**: 0-n

**Example JSON**

.. _4.1-descriptions.text:

4.1 descriptions.text
---------------------

**Definition**: A project description. May include any additional information that does not fit in the other categories.

**Requirement**: Mandatory for each desription supplied

**Occurrence**: 0-1

**Allowed values**: Free text

**Constraints**: Maximum 1000 characters

. 4.2-descriptions.type:

4.2 descriptions.type
---------------------

**Definition**: Metadata schema block containing description type informaton.

**Requirement**: Mandatory for each description supplied

**Occurrence**: 1

**Example JSON**

.. _4.2.1-descriptions.type.id:

4.2.1 descriptions.type.id
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The type of description.

**Requirement**: Mandatory for each desription supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* Primary (*preferred full description or abstract*)
* Alternative (*additional full description or abstract*)
* Brief
* Significance Statement
* Methods
* Objectives
* Other (*any other descriptive information, e.g., a note or similar*)

**Note**: If a description is provided, a single, primary description is mandatory; additional Descriptions are optional. Type is mandatory for each description specified. Controlled list adapted from Vocabularies for Registry Schema 1.6.5 'Description Type' and DataCite Metadata Schema 4.4 Appendix 1 Table 10 'descriptiontype'.

.. _4.2.1.1-descriptions.type.id.schemaUri:

4.2.1.1 descriptions.type.id.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the description type schema.

**Requirement**: Mandatory for each descriptions.typeId supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: The RAiD vocabulary on RVA is specified for raid.org and used by ARDC registration service; Registration Agencies may implement other controlled vocabularies but must provide a crosswalk. In 'core' elements like this one where variation of controlled vocabularies amongst Registration Agencies occurs, the RAiD Service should return the 'local' term and schema as well as the ‘standardised’ term and schema.

.. _4.3-descriptions.languageId:

4.3 descriptions.languageId
---------------------------

**Definition**: Language used for the description identified by a code or other identifier.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: *Controlled list from language schema*

**Example**: ``eng`` (*ISO 649-4 three-letter code*)

**Note**: Currently limited to ISO 649-4 three-letter code.

.. _4.3.1-descriptions.languageId.schemaUri:

4.3.1 descriptions.languageId.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the language identifier schema.

**Requirement**: Mandatory for each descriptions.languageId supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://www.iso.org/standard/49544.html``

**Note**: Controlled list shared across all Registration Agencies. No crosswalk; queries return language code and scheme URI. Mandatory for each language specified. 
