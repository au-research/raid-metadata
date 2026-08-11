.. autosummary::
   :toctree: generated

.. _4-title:

4 title
=======

**Definition**: a metadata schema block containing the title of the RAiD and associated properties

**Requirement**: mandatory

**Occurrence**: 1-n

**Example JSON**

.. _4.1-title.text:

4.1 title.text
--------------

**Definition**: a name or title by which the project or activity is known

**Requirement**: mandatory for each title supplied

**Occurrence**: 1

**Allowed values**: free text

**Constraints**: maximum 100 characters

.. 3.2-title.type:

4.2 title.type
--------------

**Definition**: a metadata schema block containing information about the title type

**Requirement**: mandatory for each title supplied

**Occurrence**: 1

**Example JSON**

.. _4.2.1-title.type.id:

4.2.1 title.type.id
^^^^^^^^^^^^^^^^^^^

**Definition**: the type of title

**Requirement**: mandatory for each title.type supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from title.type.schemaUri*

* ``https://vocabulary.raid.org/title.type.schema/5`` (Primary, i.e., a preferred full or long title)
* ``https://vocabulary.raid.org/title.type.schema/157`` (Short)
* ``https://vocabulary.raid.org/title.type.schema/156`` (Acronym)
* ``https://vocabulary.raid.org/title.type.schema/4`` (Alternative, including subtitle or other supplemental title)

**Default** 'Primary'

**Note**: One (and only one) current (as per start-end dates) Primary Title is mandatory for each Title specified; additional titles are optional; any previous titles are managed by start-end dates (title type does not change).

.. _4.2.2-title.type.schemaUri:

4.2.2 title.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the title type schema

**Requirement**: mandatory for each title.type supplied

**Occurrence**: 1

**Allowed values**: *Closed controlled list defined at https://vocabulary.raid.org/title.type.schemaUri/scheme*

* ``https://vocabulary.raid.org/title.type.schema/376``

**Note**: Controlled list adapted from Vocabularies for Registry Schema 1.6.5 'Name Type'.

.. _4.3-title.language:

4.3 title.language
------------------

**Definition**: a metadata schema block declaring the language of the title text

**Requirement**: recommended

**Occurrence**: 0-1

**Example JSON**

.. _4.3.1-title.languageId:

4.3.1 title.language.id
^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the language used for the title text, identified by a code or another identifier

**Requirement**: mandatory for each title.language supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from title.language.schemaUri*

**Example**: ``eng``

.. _4.3.2-title.languageId.schemaUri:

4.3.2 title.language.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the language identifier schema

**Requirement**: mandatory for each title.language supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list of allowed language schemas defined at https://vocabulary.raid.org/title.language.schemaUri/163*

* ``https://www.iso.org/standard/74575.html`` (ISO 639:2023 Code for individual languages and language groups (Set 3))

**Constraints**: currently limited to ISO 639:2023 (Set 3)

.. _4.4-title.startDate:

4.4 title.startDate
-------------------

**Definition**: the date the project or activity's title began being used

**Requirement**: mandatory for each title supplied

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Default**: Date record created

**Examples**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: Only the year is required, month and day are optional (but recommended when available).

.. _4.5-title.endDate:

4.5 title.endDate
-----------------

**Definition**: the date the project or activity title was changed or stopped being used

**Requirement**: recommended

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: Only the year is required, month and day are optional (but recommended when available).