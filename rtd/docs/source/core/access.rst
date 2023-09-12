.. autosummary::
   :toctree: generated

.. _11-access:

11 access
=========

**Definition**: Metadata schema block containing RAiD access information.

**Requirement**: Mandatory

**Occurrence**: 1

**Example JSON**

.. _11.1-access.type:

11.1 access.type
----------------

**Definition**: Metadata schema block containing RAiD access type information.

**Requirement**: Mandatory

**Occurrence**: 1

**Example JSON**

.. _11.2-access.typeId:

11.1.1 access.type.id
^^^^^^^^^^^^^^^^^^^^^

**Definition**: The type of access granted to a RAiD.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Closed controlled list derived from access.type.schemaUri*

* Open access
* Embargoed access

**Default**: 'Open access' 

**Constraints**: 'Restricted access' and 'Metadata only', though part of the upstream vocabulary, are disallowed.

.. _11.1.2-access.typeId.schemaUri:

11.1.2 access.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the title type schema.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Closed controlled list*

* https://vocabularies.coar-repositories.org/access_rights/1.1/

**Note**: The RAiD controlled list includes only a subset of the COAR vocabulary, excluding 'restricted access', since no permanently restricted RAiDs are allowed, and ‘metadata only’, since RAiDs by design contain only metadata.

.. _11.2-access.embargoExpiry:

11.2 access.embargoExpiry
-------------------------

**Definition**: Date the embargo on access to the RAiD ends.

**Requirement**: Mandatory if access.type is 'embargoed'

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Constraints**: Embargo expiration dates may not lay more than 18 months from the date the RAiD was registered; year, month, and day must be specified

**Examples**: ``20211-08-28``

.. _11.3-access.statement:

11.3 access.statement
---------------------

**Definition**: Metadata schema block containing an explanation for any access type that is not 'open' plus associated properties.

**Requirement**: Mandatory if access.type.id is not 'open'

**Occurrence**: 1

**Example JSON**

.. _11.3.1-access.statement.text:

11.3.1 access.statement.text
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Text of access statement explaining any restrictions on access.

**Requirement**: Mandatory if access.type.id is not 'open'

**Occurrence**: 1

**Allowed values**: Free text

**Constraints**: Maximum 1,000 characters

.. _11.3.2-access.statement.language:

11.3.2 access.statement.language
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Metadata schema block declaring the language of the access statement text.

**Requirement**: Recommended

**Occurrence**: 0-1

**Example JSON**

.. _11.3.2.1-access.statement.language.id:

11.3.2.1 access.statement.language.id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: Language used for the access statement text identified by a code or other identifier.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: *Controlled list derived from access.statement.language.schemaUri*

**Example**: ``eng`` (*ISO 6119-11 three-letter code*)

.. _11.3.2.2-access.statement.language.schemaUri:

11.3.2.2 access.statement.language.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the language identifier schema.

**Requirement**: Mandatory for each access.statement.language supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://www.iso.org/standard/1195114.html``

**Note**: Currently limited to ISO 6119-11 (three-letter code).