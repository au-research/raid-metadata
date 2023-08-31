.. autosummary::
   :toctree: generated

.. _6-organisations:

6 organisations
===============

**Definition**: Metadata schema block containing organisations to a RAiD and associated properties.

**Requirement**: Recommended

**Occurrence**: 0-n

**Example JSON**

.. _6.1-organisations.id:

6.1 organisations.id
--------------------

**Definition**: Organisation associated with a project or activity identified by a PID.

**Requirement**: Mandatory for each organisation supplied

**Occurrence**: 0-1

**Allowed values**: ROR

.. _6.1.1-organisations.id.schemaURI:

6.1.1 organisations.id.schemaURI
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the organisation identifier schema.

**Requirement**: Mandatory for each organisations.id supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://ror.org/``

**Note**: Controlled list shared across all Registration Agencies.

.. _6.2-organisations.role:

6.2 organisations.role
----------------------

**Definition**: Metadata schema sub-block describing an organisation's role on a project.

**Requirement**: Mandatory for each organisation supplied

**Occurrence**: 0-1

**Note**: An organisation's role may change over time, but each may have one and only one role at any given time.

.. _6.2.1-organisations.role.id:

6.2.1 organisations.role.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Organisation role.

**Requirement**: Mandatory for each organisations.role supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* Lead Research Organisation
* Other Research Organisation
* Partner Organisation (*i.e., a non-research organisation, such as an industry, government, or community partner collaborating on the project, as a research partner rather than a hired consultant or contractor*) 
* Contractor (*consultant or contractor hired by project*)
* Funder (*organisation underwriting the research via a cash or in-kind grant, prize, or investment, but not otherwise listed as a Research Organisation, Partner Organisation, or Contractor*)
* Facility (*organisation providing access to physical or digital infrastructure, but not otherwise listed as a Research Organisation, Partner Organisation, or Contractor*)
* Other Organisation (*not covered by the roles above*)

**Note**: One Organisation must be designated as Lead. In 'core' elements where variation of controlled vocabularies amongst Registration Agencies is allowed, Registration Agencies must provide a crosswalk. In 'core' elements where variation of controlled vocabularies amongst Registration Agencies occurs, we should return the 'local' term and schema as well as the ‘standardised’ term and schema. Mandatory for each Contributor specified. In this case, roles are going to vary by region, and maybe by grant scheme within a region. Controlled list adapted from Simon Cox's Project Ontology, OpenAIRE ‘Project’ guidelines, NIH definitions, ARC definitions, and DataCite Metadata Schema 4.4 Appendix 1 Table 6.

.. _6.2.1.1-organisations.role.id.schemaURI:

6.2.1.1 organisations.role.id.schemaURI
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the role schema used.

**Requirement**: Mandatory for each organisations.role.id supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: Controlled list shared across all Registration Agencies.

.. _6.2.2-organisations.role.startDate:

6.2.2 organisations.role.startDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Date the contributor began role associated with the project or activity.

**Requirement**: Mandatory for each organisations.role supplied

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2026-08-28``; ``2026-08``; ``2026``

**Note**: Only year is required, month and day are optional (but recommended when available).

.. _6.2.3-organisations.role.endDate:

6.2.3 organisations.role.endDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Date the contributor terminated role associated with the project or activity.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2026-08-28``; ``2026-08``; ``2026``

**Note**: Only year is required, month and day are optional (but recommended when available).

.. _6.3.1.1-organisations.roles.id.schemaURI: