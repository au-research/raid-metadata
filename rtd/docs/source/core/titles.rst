.. autosummary::
   :toctree: generated

.. _3-title:

3 title
=======

**Definition**: a metadata schema block containing the title of the RAiD and associated properties

**Requirement**: mandatory

**Occurrence**: 1-n

**Example JSON**

.. _3.1-title.text:

3.1 title.text
--------------

**Definition**: a name or title by which the project or activity is known

**Requirement**: mandatory for each title supplied

**Occurrence**: 1

**Allowed values**: free text

**Constraints**: maximum 100 characters

.. 3.2-title.type:

3.2 title.type
--------------

**Definition**: a metadata schema block containing information about the title type

**Requirement**: mandatory for each title supplied

**Occurrence**: 1

**Example JSON**

.. _3.2.1-title.type.id:

3.2.1 title.type.id
^^^^^^^^^^^^^^^^^^^

**Definition**: the type of title

**Requirement**: mandatory for each title supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from title.type.schemaUri*

* Primary
* Short
* Acronym
* Alternative (*includes subtitle and other supplemental or alternative title*)

**Default** 'Primary'

**Note**: one (and only one) current (as per start-end dates) Primary Title is mandatory for each Title specified; additional title are optional; any previous titles are managed by start-end dates (title type does not change); controlled list adapted from Vocabularies for Registry Schema 1.6.5 'Name Type'.

.. _3.2.2-title.type.schemaUri:

3.2.2 title.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the title type schema

**Requirement**: mandatory for each title.type.id supplied

**Occurrence**: 1

**Allowed values**: *Closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]

.. _3.3-title.language:

3.3 title.language
------------------

**Definition**: a metadata schema block declaring the language of the title text

**Requirement**: recommended

**Occurrence**: 0-1

**Example JSON**

.. _3.3.1-title.languageId:

3.3.1 title.language.id
^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the language used for the title text, identified by a code or another identifier

**Requirement**: recommended

**Occurrence**: 0-1

**Allowed values**: *closed controlled list derived from title.language.schemaUri*

**Example**: ``eng`` (*ISO 639-3 three-letter code*)

.. _3.3.2-title.languageId.schemaUri:

3.3.2 title.language.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the language identifier schema

**Requirement**: mandatory for each title.language.id supplied

**Occurrence**: 0-1

**Allowed values**: *closed controlled list of allowed language schemas*

* ``https://www.iso.org/standard/39534.html``

**Note**: Currently limited to ISO 639-3 three-letter code.

.. _3.4-title.startDate:

3.4 title.startDate
-------------------

**Definition**: the date the project or activity's title began being used

**Requirement**: mandatory for each title supplied

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Default**: Date record created

**Examples**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: only the year is required, month and day are optional (but recommended when available).

.. _3.5-title.endDate:

3.5 title.endDate
-----------------

**Definition**: the date the project or activity title was changed or stopped being used

**Requirement**: recommended

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: only the year is required, month and day are optional (but recommended when available).