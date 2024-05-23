.. autosummary::
   :toctree: generated

.. _11-access:

11 access
=========

**Definition**: a metadata schema block containing RAiD access information

**Requirement**: mandatory

**Occurrence**: 1

**Example JSON**

.. _11.1-access.type:

11.1 access.type
----------------

**Definition**: a metadata schema block containing RAiD access type information

**Requirement**: mandatory

**Occurrence**: 1

**Example JSON**

.. _11.2-access.typeId:

11.1.1 access.type.id
^^^^^^^^^^^^^^^^^^^^^

**Definition**: the type of access granted to a RAiD metadata record

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from access.type.schemaUri*

* ``https://vocabularies.coar-repositories.org/access_rights/c_abf2/`` (Open access) 
* ``https://vocabularies.coar-repositories.org/access_rights/c_f1cf/`` (Embargoed access)

**Default**: 'Open access' 

**Constraints**: 'Restricted access' and 'Metadata only', though part of the upstream vocabulary, are disallowed

.. _11.1.2-access.typeId.schemaUri:

11.1.2 access.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the access type schema

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: *closed controlled list*

* ``https://vocabulary.raid.org/access.type.id/241``

**Note**: The RAiD controlled list includes a subset of the COAR vocabulary (https://vocabularies.coar-repositories.org/access_rights/1.1/), including 'Open access' and 'Embargoed access', but excluding 'Restricted access' (since no permanently restricted RAiDs are allowed), and ‘Metadata only’ (since RAiDs by design contain only metadata).

.. _11.2-access.embargoExpiry:

11.2 access.embargoExpiry
-------------------------

**Definition**: the date any embargo on access to the RAiD metadata ends

**Requirement**: mandatory if access.type is 'embargoed'

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Constraints**: embargo expiration dates may not lay more than 18 months from the date the RAiD was registered; year, month, and day must be specified

**Example**: ``20211-08-28``

.. _11.3-access.statement:

11.3 access.statement
---------------------

**Definition**: a metadata schema block containing an explanation for any access type that is not 'open', with the explanation's associated properties

**Requirement**: mandatory if access.type.id is not 'open'

**Occurrence**: 0-1

**Example JSON**

.. _11.3.1-access.statement.text:

11.3.1 access.statement.text
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the text of an access statement that explains any restrictions on access

**Requirement**: mandatory if access.type.id is not 'open'

**Occurrence**: 0-1

**Allowed values**: free text

**Constraints**: maximum 1,000 characters

**Example JSON**

.. _11.3.2-access.statement.language:

11.3.2 access.statement.language
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: a metadata schema block declaring the language of the text in the access statement

**Requirement**: recommended

**Occurrence**: 0-1

**Example JSON**

.. _11.3.2.1-access.statement.language.id:

11.3.2.1 access.statement.language.id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: the language used for the access statement text, identified by a code or other identifier

**Requirement**: recommended

**Occurrence**: 0-1

**Allowed values**: *closed controlled list derived from access.statement.language.schemaUri*

**Example**: ``eng`` (*ISO 639-3 three-letter code*)

.. _11.3.2.2-access.statement.language.schemaUri:

11.3.2.2 access.statement.language.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: the URI of the language identifier schema

**Requirement**: mandatory for each access.statement.language supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list of allowed language schemas*

* ``https://vocabulary.raid.org/access.statement.language.schemaUri/196``

**Note**: currently limited to ISO 639-3 three-letter code (https://www.iso.org/standard/39534.html).