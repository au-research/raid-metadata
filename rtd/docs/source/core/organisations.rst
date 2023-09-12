.. autosummary::
   :toctree: generated

.. _6-organisation:

6 organisation
==============

**Definition**: a metadata schema block containing the organisation associated with a RAiD and its associated properties.

**Requirement**: recommended

**Occurrence**: 0-n

**Example JSON**

.. _6.1-organisation.id:

6.1 organisation.id
-------------------

**Definition**: the organisation associated with a project or activity, as identified by a persistent identifier (PID)

**Requirement**: mandatory for each organisation supplied

**Occurrence**: 0-1

**Allowed values**: the identifier is defined by organisation.schemaUri

.. _6.2-organisation.schemaUri:

6.2 organisation.schemaUri
--------------------------

**Definition**: the URI of the organisation identifier schema.

**Requirement**: mandatory for each organisation.id supplied

**Occurrence**: 0-1

**Allowed values**: *closed controlled list*

* ``https://ror.org/``

**Note**: the controlled list shared across all Registration Agencies.

.. _6.3-organisation.role:

6.3 organisation.role
---------------------

**Definition**: a metadata schema sub-block describing an organisation's role on a project.

**Requirement**: mandatory for each organisation supplied

**Occurrence**: 0-1

**Note**: an organisation's role may change over time, but each organisation may have one and only one role at any given time.

.. _6.3.1-organisation.role.id:

6.3.1 organisation.role.id
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the organisation's role

**Requirement**: mandatory for each organisation.role supplied

**Occurrence**: 0-1

**Allowed values**: *controlled list derived from organisation.role.schemaUri*

* Lead Research Organisation
* Other Research Organisation
* Partner Organisation (*i.e. a non-research organisation, such as an industry, government, or community partner that is collaborating on the project or activity, as a research partner rather than a hired consultant or contractor*) 
* Contractor (*consultant or contractor hired by project or activity*)
* Funder (*organisation underwriting the research via a cash or in-kind grant, prize, or investment, but not otherwise listed as a research organisation, partner organisation or contractor*)
* Facility (*organisation providing access to physical or digital infrastructure, but not otherwise listed as a research organisation, partner organisation or contractor*)
* Other Organisation (*not covered by the roles above*)

**Note**: one organisation must be designated as Lead. In 'core' elements where variation of controlled vocabularies amongst Registration Agencies is allowed, Registration Agencies must provide a crosswalk. In 'core' elements where variation of controlled vocabularies amongst Registration Agencies occurs, we should return the 'local' term and schema as well as the ‘standardised’ term and schema. Mandatory for each organisation specified. In this case, roles are going to vary by region, and maybe by grant scheme within a region. Controlled list adapted from Simon Cox's Project Ontology, OpenAIRE ‘Project’ guidelines, NIH definitions, ARC definitions, and DataCite Metadata Schema 4.4 Appendix 1 Table 6.

.. _6.3.2-organisation.role.schemaUri:

6.3.2 organisation.role.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the role schema used.

**Requirement**: mandatory for each organisation.role.id supplied

**Occurrence**: 0-1

**Allowed values**: *Closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: the controlled list shared across all Registration Agencies.

.. _6.3.3-organisation.role.startDate:

6.3.3 organisation.role.startDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the date that the organisation began a role associated with the project or activity.

**Requirement**: mandatory for each organisation.role supplied

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2026-08-28``; ``2026-08``; ``2026``

**Note**: only the year is required; month and day are optional (but recommended when available).

.. _6.3.4-organisation.role.endDate:

6.3.4 organisation.role.endDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the date that the organisation terminated a role associated with the project or activity.

**Requirement**: recommended

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2026-08-28``; ``2026-08``; ``2026``

**Note**: only the year is required; month and day are optional (but recommended when available).