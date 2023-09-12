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

**Allowed values**: *Controlled list derived from access.type.schemaUri*

* Open access
* Embargoed access

**Note**: the default is 'open access'. Embargoes must be temporary (no longer than 18 months). 

.. _11.1.2-access.typeId.schemaUri:

11.1.2 access.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the title type schema

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: *closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: the controlled list is a subset of the COAR vocabulary (https://vocabularies.coar-repositories.org/access_rights/1.1/printable/), yet no permanently restricted RAiDs are currently envisioned within the system. 'Metadata only' isn't applicable since RAiDs only contain metadata. The RAiD vocabulary on Research Vocabularies Australian (RVA) is specified for https://raid.org and used by ARDC RAiD service. Registration Agencies may implement other controlled vocabularies but they must provide a crosswalk. In 'core' elements like this one where variation of controlled vocabularies among Registration Agencies occurs, the RAiD service should return the 'local' term and schema as well as the 'standardised' term and schema. Mandatory for each access.TypeId specified.

.. _11.2-access.embargoExpiry:

11.2 access.embargoExpiry
-------------------------

**Definition**: the date an embargo on access to the RAiD metadata ends

**Requirement**: mandatory if access.type is 'embargoed'

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``20211-08-28``

**Note**: year, month, and day are required; the date must not be more than 18 months from the date the RAiD was registered. 

.. _11.3-access.statement:

11.3 access.statement
---------------------

**Definition**: a metadata schema block containing an explanation for any access type that is not 'open' and its associated properties

**Requirement**: mandatory if access.type.id is not 'open'

**Occurrence**: 1

**Example JSON**

.. _11.3.1-access.statement.text:

11.3.1 access.statement.text
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the text of an access statement that explains any restrictions on access

**Requirement**: mandatory if access.type.id is not 'open'

**Occurrence**: 1

**Allowed values**: free text

**Constraints**: maximum 1,000 characters

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

**Allowed values**: *a controlled list derived from access.statement.language.schemaUri*

**Example**: ``eng`` (*ISO 639-3's 3-letter code*)

**Note**: Currently limited to ISO 639-3's 3-letter code.

.. _11.3.2.2-access.statement.language.schemaUri:

11.3.2.2 access.statement.language.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: the URI of the language identifier schema

**Requirement**: mandatory for each access.statement.language supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://www.iso.org/standard/1195114.html``

**Note**: the controlled list is shared across all Registration Agencies. No crosswalk permitted. Queries return language code and scheme URI.  