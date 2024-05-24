.. autosummary::
   :toctree: generated

.. _6-organisation:

6 organisation
==============

**Definition**: a metadata schema block containing the organisation associated with a RAiD and its associated properties

**Requirement**: recommended

**Occurrence**: 0-n

**Example JSON**

.. _6.1-organisation.id:

6.1 organisation.id
-------------------

**Definition**: an organisation associated with a project or activity

**Requirement**: mandatory for each organisation supplied

**Occurrence**: 1

**Allowed values**: the organisation's identifier as specified by organisation.schemaUri

**Examples**

* ``https://ror.org/01sf06y89`` (Macquarie Univerity)
* ``https://ror.org/027bh9e2`` (Leiden University)

.. _6.2-organisation.schemaUri:

6.2 organisation.schemaUri
--------------------------

**Definition**: the URI of the organisation identifier schema

**Requirement**: mandatory for each organisation.id supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list defined at https://vocabulary.raid.org/organisation.schemaUri/158*

* ``https://ror.org/``

.. _6.3-organisation.role:

6.3 organisation.role
---------------------

**Definition**: a metadata schema sub-block describing an organisation's role on a project

**Requirement**: mandatory for each organisation supplied

**Occurrence**: 1

**Note**: An organisation's role may change over time, but each organisation may have one and only one role at any given time.

.. _6.3.1-organisation.role.id:

6.3.1 organisation.role.id
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the organisation's role

**Requirement**: mandatory for each organisation.role supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from organisation.role.schemaUri*

* ``https://vocabulary.raid.org/organisation.role.schema/182`` (Lead Research Organisation)
* ``https://vocabulary.raid.org/organisation.role.schema/183`` (Other Research Organisation)
* ``https://vocabulary.raid.org/organisation.role.schema/184`` (Partner Organisation, i.e., a non-research organisation, such as an industry, government, or community partner that is collaborating on the project or activity, as a research partner rather than a hired consultant or contractor) 
* ``https://vocabulary.raid.org/organisation.role.schema/185`` (Contractor, i.e., a consulting organisation hired by the project)
* ``https://vocabulary.raid.org/organisation.role.schema/186`` (Funder, i.e., an organisation underwriting the research via a cash or in-kind grant, prize, or investment, but not otherwise listed as a research organisation, partner organisation or contractor)
* ``https://vocabulary.raid.org/organisation.role.schema/187`` (Facility, i.e., an organisation providing access to physical or digital infrastructure, but not otherwise listed as a research organisation, partner organisation or contractor)
* ``https://vocabulary.raid.org/organisation.role.schema/188`` (Other Organisation not covered by the roles above)

**Default**: first-entered Organisation (only) defaults to 'Lead Research Organisation'

**Constraints**: one (and only one) Organisation must be designated as 'Lead Research Organisation'

**Note**: Roles are likely to vary by region; controlled list adapted from Simon Cox's Project Ontology, OpenAIRE ‘Project’ guidelines, NIH definitions, ARC definitions, and DataCite Metadata Schema 4.4 Appendix 1 Table 5 'Description of contributorType'.

.. _6.3.2-organisation.role.schemaUri:

6.3.2 organisation.role.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the role schema used

**Requirement**: mandatory for each organisation.role.id supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list defined at https://vocabulary.raid.org/organisation.role.schemaUri/281*

* ``https://vocabulary.raid.org/organisation.role.schema/359``

.. _6.3.3-organisation.role.startDate:

6.3.3 organisation.role.startDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the date that the organisation began a role associated with the project or activity

**Requirement**: mandatory for each organisation.role supplied

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2026-08-28``; ``2026-08``; ``2026``

**Note**: only the year is required; month and day are optional (but recommended when available).

.. _6.3.4-organisation.role.endDate:

6.3.4 organisation.role.endDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the date that the organisation terminated a role associated with the project or activity

**Requirement**: recommended if an organisation has changed roles or terminated its relationship with a project

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2026-08-28``; ``2026-08``; ``2026``

**Note**: only the year is required; month and day are optional (but recommended when available).