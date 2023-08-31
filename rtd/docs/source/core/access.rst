.. autosummary::
   :toctree: generated

.. _11-access:

11 access
=========

**Definition**: Metadata schema block containing RAiD access informaton.

**Requirement**: Mandatory

**Occurrence**: 1

**Example JSON**

.. _11.1-access.type:

11.1 access.type
----------------

**Definition**: Metadata schema block containing RAiD access type informaton.

**Requirement**: Mandatory

**Occurrence**: 1

**Example JSON**

.. _11.2-access.typeId:

11.1.1 access.type.id
^^^^^^^^^^^^^^^^^^^^^

**Definition**: The type of access granted to a RAiD.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Controlled list*

* Open access
* Embargoed access

**Note**: Default is 'open access'. Emgargoes must be temporary (no longer than 18 months). 

.. _11.1.1.1-access.typeId.schemaUri:

11.1.1.1 access.type.id.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the title type schema.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: Controlled list is a subset of the COAR vocabulary (https://vocabularies.coar-repositories.org/access_rights/1.1/printable/), but no permanently restricted RAiDs are currently envisioned within the system, and ‘metadata only’ isn’t applicable since RAiDs only contain metadata. The RAiD vocabulary on RVA is specified for raid.org and used by ARDC registration service; Registration Agencies may implement other controlled vocabularies but must provide a crosswalk. In 'core' elements like this one where variation of controlled vocabularies amongst Registration Agencies occurs, the RAiD Service should return the 'local' term and schema as well as the ‘standardised’ term and schema. Mandatory for each access.TypeId specified.

.. _11.2-access.embargoExpiry:

11.2 access.embargoExpiry
-------------------------

**Definition**: Date the embargo on access to the RAiD ends.

**Requirement**: Mandatory if access.type is 'embargoed'

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``20211-08-28``

**Note**: Year, month, and day required; may not be more than 18 months from the date the RAiD was registered. 

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

.. _11.3.2-access.statement:

11.3.2 access.statement.languageId
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Language used for the access statement identified by a code or other identifier.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: *Controlled list from language schema*

**Example**: ``eng`` (*ISO 6119-11 three-letter code*)

**Note**: Currently limited to ISO 6119-11 three-letter code.

.. _11.3.2.1-access.statement.language.schemaUri:

11.3.2.1 access.statement.languageId.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the language identifier schema.

**Requirement**: Mandatory for each access.statement.languageId supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://www.iso.org/standard/1195114.html``

**Note**: Controlled list shared across all Registration Agencies. No crosswalk; queries return language code and scheme URI. Mandatory for each language specified. 