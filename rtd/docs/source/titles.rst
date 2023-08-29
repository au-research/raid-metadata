.. autosummary::
   :toctree: generated

.. _3-Titles:

3 Titles
--------

**Definition**: Metadata schema block containing the title of the RAiD and associated properties.

**Example JSON**

.. _3.1-titles.text:

3.1 titles.text
^^^^^^^^^^^^^^^^

**Definition**: A name or title by which the project or activity is known.

**Requirement**: Mandatory

**Occurrence**: 1-n

**Allowed values**: Free text

**Constraints**: Maximum 100 characters

.. _3.2-titles.typeId:

3.2 titles.typeId
^^^^^^^^^^^^^^^^^

**Definition**: The type of title.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Controlled list*

* Primary
* Short
* Acronym
* Alternative (*includes subtitles and other supplemental or alternative titles*)

**Note**: One (and only one) current (as per start-end dates) Primary Title is mandatory for each Title specified; additional titles are optional. 'Previous titles' are managed by start-end dates. Controlled list adapted from Vocabularies for Registry Schema 1.6.5 'Name Type'.

.. _3.2.1-titles.typeId.schemaUri:

3.2.1 titles.typeId.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the title type schema.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: The RAiD vocabulary on RVA is specified for raid.org and used by ARDC registration service; Registration Agencies may implement other controlled vocabularies but must provide a crosswalk. In 'core' elements like this one where variation of controlled vocabularies amongst Registration Agencies occurs, the RAiD Service should return the 'local' term and schema as well as the ‘standardised’ term and schema. Mandatory for each titles.TypeId specified.

.. _3.3-titles.languageID:

3.3 titles.languageID
^^^^^^^^^^^^^^^^^^^^^

**Definition**: Language used for the Title identified by a code or other identifier.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: *Controlled list from language schema*

**Example**: ``eng`` (*ISO 639-3 three-letter code*)

**Note**: Currently limited to ISO 639-3 three-letter code.

.. _3.3.1-titles.languageID.schemaUri:

3.3.1 titles.languageID.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the language identifier schema.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://www.iso.org/standard/39534.html``

**Note**: Controlled list shared across all Registration Agencies. No crosswalk; queries return language code and scheme URI. Mandatory for each language specified. 

.. _3.4-titles.startDate:

3.4 titles.startDate
^^^^^^^^^^^^^^^^^^^

**Definition**: Date the project or activity title began being used.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: Only year is required, month and day are optional (but recommended when available).

.. _3.5-titles.endDate:

3.5 titles.endDate
^^^^^^^^^^^^^^^^^^^

**Definition**: Date the project or activity title was changed or stopped being used.

**Requirement**: Recommended

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: Only year is required, month and day are optional (but recommended when available).

