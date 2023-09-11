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

**Allowed values**: *controlled list derived from title.type.schemaUri*

* Primary
* Short
* Acronym
* Alternative (*includes subtitle and other supplemental or alternative title*)

**Note**: one (and only one) current (as per start-end dates) primary title is mandatory for each title specified; additional titles are optional. 'Previous title' is managed by start-end dates. The controlled list was adapted from Vocabularies for Registry Schema 1.6.5 'Name Type'.

.. _3.2.2-title.type.schemaUri:

3.2.2 title.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the title type schema

**Requirement**: mandatory for each title.type.id supplied

**Occurrence**: 1

**Allowed values**: *Closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: the RAiD vocabulary on RVA is specified for https://raid.org and used by the ARDC RAiD service; Registration Agencies may implement other controlled vocabularies but they must provide a crosswalk. In 'core' elements like this one where variation of controlled vocabularies among Registration Agencies occurs, the RAiD service should return the 'local' term and schema as well as the 'standardised' term and schema. Mandatory for each title.TypeId specified.

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

**Allowed values**: *controlled list derived from title.language.schemaUri*

**Example**: ``eng`` (*ISO 639-3's 3-letter code*)

**Note**: currently limited to ISO 639-3's 3-letter code.

.. _3.3.2-title.languageId.schemaUri:

3.3.2 title.language.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the language identifier schema

**Requirement**: mandatory for each title.language.id supplied

**Occurrence**: 0-1

**Allowed values**: *Closed controlled list*

* ``https://www.iso.org/standard/39534.html``

**Note**: the controlled list is shared across all Registration Agencies. No crosswalk - queries return language code and scheme URI.  

.. _3.4-title.startDate:

3.4 title.startDate
-------------------

**Definition**: the date the project or activity's title began being used.

**Requirement**: mandatory for each title supplied

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

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

