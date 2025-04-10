.. autosummary::
   :toctree: generated

.. _4-description:

4 description
==============

**Definition**: a metadata schema block containing the description of the RAiD and associated properties

**Requirement**: recommended

**Occurrence**: 0-n

**Example JSON**

.. _4.1-description.text:

4.1 description.text
--------------------

**Definition**: a project description that may include any additional information not captured by other metadata properties

**Requirement**: mandatory for each description supplied

**Occurrence**: 1

**Allowed values**: free text

**Constraints**: maximum 1000 characters

**Note**: Descriptions are intended to be flexible, and projects can use them liberally to capture information about the project that is not recorded elsewhere in the RAiD.

. 4.2-description.type:

4.2 description.type
--------------------

**Definition**: a metadata schema block declaring the type of description

**Requirement**: mandatory for each description supplied

**Occurrence**: 1

**Example JSON**

.. _4.2.1-description.type.id:

4.2.1 description.type.id
^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the type of description.

**Requirement**: mandatory for each description.type supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from description.type.schemaUri*

* ``https://vocabulary.raid.org/description.type.id/326`` (Primary, i.e., a preferred full description or abstract)
* ``https://vocabulary.raid.org/description.type.id/321`` (Alternative, i.e., an additional or supplementary full description or abstract)
* ``https://vocabulary.raid.org/description.type.id/322`` (Brief, i.e., a shorted version of the primary description)
* ``https://vocabulary.raid.org/description.type.id/327`` (Significance Statement)
* ``https://vocabulary.raid.org/description.type.id/323`` (Methods)
* ``https://vocabulary.raid.org/description.type.id/324`` (Objectives)
* ``https://vocabulary.raid.org/raid_placeholder/392`` (Acknowledgements, i.e., for recognition of people not listed as Contributors or organisations not listed as Organisations)
* ``https://vocabulary.raid.org/description.type.id/325`` (Other, i.e., any other descriptive information such as a note)

**Default**: description.type.id for first-entered description (only) defaults to 'Primary'

**Constraints**: if a description is provided, one (and only one) primary description is mandatory

.. _4.2.2-description.type.id.schemaUri:

4.2.2 description.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the description type schema

**Requirement**: mandatory for each description.type supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list defined at https://vocabulary.raid.org/description.type.schemaUri/275*

* ``https://vocabulary.raid.org/description.type.schema/320``

**Note**: Controlled list adapted from Vocabularies for Registry Schema 1.6.5 'Description Type' and DataCite Metadata Schema 4.4 Appendix 1 Table 10 'Description of descriptiontype'.

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

**Requirement**: mandatory for each description.language supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from titles.language.schemaUri*

**Example**: ``eng``

.. _4.3.1-description.languageId.schemaUri:

4.3.2 description.language.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the language identifier schema

**Requirement**: mandatory for each description.language supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list of allowed language schemas defined at https://vocabulary.raid.org/description.language.schemaUri/240*

* ``https://www.iso.org/standard/74575.html`` (ISO 639:2023 Code for individual languages and language groups (Set 3))

**Constraints**: currently limited to ISO 639:2023 (Set 3)
