.. autosummary::
   :toctree: generated

.. _3-title:

3 title
=======

**Definition**: Metadata schema block containing the title of the RAiD and associated properties.

**Requirement**: Mandatory

**Occurrence**: 1-n

**Example JSON**

.. _3.1-title.text:

3.1 title.text
--------------

**Definition**: A name or title by which the project or activity is known.

**Requirement**: Mandatory for each title supplied

**Occurrence**: 1

**Allowed values**: Free text

**Constraints**: Maximum 100 characters

.. 3.2-title.type:

3.2 title.type
--------------

**Definition**: Metadata schema block containing information about the title type.

**Requirement**: Mandatory for each title supplied

**Occurrence**: 1

**Example JSON**

.. _3.2.1-title.type.id:

3.2.1 title.type.id
^^^^^^^^^^^^^^^^^^^

**Definition**: The type of title.

**Requirement**: Mandatory for each title supplied

**Occurrence**: 1

**Allowed values**: *Controlled list derived from title.type.schemaUri*

* Primary
* Short
* Acronym
* Alternative (*includes subtitle and other supplemental or alternative title*)

**Note**: One (and only one) current (as per start-end dates) Primary Title is mandatory for each Title specified; additional title are optional. 'Previous title' are managed by start-end dates. Controlled list adapted from Vocabularies for Registry Schema 1.6.5 'Name Type'.

.. _3.2.2-title.type.schemaUri:

3.2.2 title.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the title type schema.

**Requirement**: Mandatory for each title.type.id supplied

**Occurrence**: 1

**Allowed values**: *Closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: The RAiD vocabulary on RVA is specified for raid.org and used by ARDC registration service; Registration Agencies may implement other controlled vocabularies but must provide a crosswalk. In 'core' elements like this one where variation of controlled vocabularies amongst Registration Agencies occurs, the RAiD Service should return the 'local' term and schema as well as the ‘standardised’ term and schema. Mandatory for each title.TypeId specified.

.. _3.3-title.language:

3.3 title.language
------------------

**Definition**: Metadata schema block declaring the language of the title text.

**Requirement**: Recommended

**Occurrence**: 0-1

**Example JSON**

.. _3.3.1-title.languageId:

3.3.1 title.language.id
^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Language used for the title text identified by a code or other identifier.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: *Controlled list derived from title.language.schemaUri*

**Example**: ``eng`` (*ISO 639-3 three-letter code*)

**Note**: Currently limited to ISO 639-3 three-letter code.

.. _3.3.2-title.languageId.schemaUri:

3.3.2 title.language.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the language identifier schema.

**Requirement**: Mandatory for each title.language.id supplied

**Occurrence**: 0-1

**Allowed values**: *Closed controlled list*

* ``https://www.iso.org/standard/39534.html``

**Note**: Controlled list shared across all Registration Agencies. No crosswalk; queries return language code and scheme URI.  

.. _3.4-title.startDate:

3.4 title.startDate
-------------------

**Definition**: Date the project or activity title began being used.

**Requirement**: Mandatory for each title supplied

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: Only year is required, month and day are optional (but recommended when available).

.. _3.5-title.endDate:

3.5 title.endDate
-----------------

**Definition**: Date the project or activity title was changed or stopped being used.

**Requirement**: Recommended

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: Only year is required, month and day are optional (but recommended when available).

