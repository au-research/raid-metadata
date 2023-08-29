.. autosummary::
   :toctree: generated

.. _4-Descriptions:


3 Descriptions block
--------------

.. _3.1-descriptions.description:

3.1 descriptions.description
^^^^^^^^^^^^^^^^

**Definition**: A project description. May include any additional information that does not fit in the other categories.

**Requirement**: Recommended

**Occurrence**: 0-n

**Allowed values**: Free text

**Constraints**: Maximum 1000 characters

.. _3.2-descriptions.typeId:

3.2 descriptions.typeId
^^^^^^^^^^^^^^^^^

**Definition**: The type of description.

**Requirement**: Recommended

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
.

.. _3.2a-descriptions.typeId.schemaUri:

3.2.a descriptions.typeId.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the description type schema.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: The RAiD vocabulary on RVA is specified for raid.org and used by ARDC registration service; Registration Agencies may implement other controlled vocabularies but must provide a crosswalk. In 'core' elements like this one where variation of controlled vocabularies amongst Registration Agencies occurs, the RAiD Service should return the 'local' term and schema as well as the ‘standardised’ term and schema. Mandatory for each descriptions.TypeId specified.

.. _3.2-descriptions.languageID:

3.3 descriptions.languageID
^^^^^^^^^^^^^^^^^^^^^

**Definition**: Language used for the description identified by a code or other identifier.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: *Controlled list from language schema*

**Example**: ``eng`` (*ISO 639-3 three-letter code*)

.. _3.2a-descriptions.languageID.schemaUri:

**Note**: Currently limited to ISO 639-3 three-letter code.

3.3.a descriptions.languageID.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the language identifier schema.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://www.iso.org/standard/39534.html``

**Note**: Controlled list shared across all Registration Agencies. No crosswalk; queries return language code and scheme URI. Mandatory for each language specified. 

