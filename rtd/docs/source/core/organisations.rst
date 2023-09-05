.. autosummary::
   :toctree: generated

.. _6-organisation:

6 organisation
==============

**Definition**: Metadata schema block containing organisation to a RAiD and associated properties.

**Requirement**: Recommended

**Occurrence**: 0-n

**Example JSON**

.. _6.1-organisation.id:

6.1 organisation.id
-------------------

**Definition**: Organisation associated with a project or activity identified by a PID.

**Requirement**: Mandatory for each organisation supplied

**Occurrence**: 0-1

**Allowed values**: Identifier defined by organisation.schemaUri

.. _6.2-organisation.schemaUri:

6.2 organisation.schemaUri
--------------------------

**Definition**: The URI of the organisation identifier schema.

**Requirement**: Mandatory for each organisation.id supplied

**Occurrence**: 0-1

**Allowed values**: *Closed controlled list*

* ``https://ror.org/``

**Note**: Controlled list shared across all Registration Agencies.

.. _6.3-organisation.role:

6.3 organisation.role
---------------------

**Definition**: Metadata schema sub-block describing an organisation's role on a project.

**Requirement**: Mandatory for each organisation supplied

**Occurrence**: 0-1

**Note**: An organisation's role may change over time, but each may have one and only one role at any given time.

.. _6.3.1-organisation.role.id:

6.3.1 organisation.role.id
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Organisation role.

**Requirement**: Mandatory for each organisation.role supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list derived from organisation.role.schemaUri*

* Lead Research Organisation
* Other Research Organisation
* Partner Organisation (*i.e., a non-research organisation, such as an industry, government, or community partner collaborating on the project, as a research partner rather than a hired consultant or contractor*) 
* Contractor (*consultant or contractor hired by project*)
* Funder (*organisation underwriting the research via a cash or in-kind grant, prize, or investment, but not otherwise listed as a Research Organisation, Partner Organisation, or Contractor*)
* Facility (*organisation providing access to physical or digital infrastructure, but not otherwise listed as a Research Organisation, Partner Organisation, or Contractor*)
* Other Organisation (*not covered by the roles above*)

**Note**: One Organisation must be designated as Lead. In 'core' elements where variation of controlled vocabularies amongst Registration Agencies is allowed, Registration Agencies must provide a crosswalk. In 'core' elements where variation of controlled vocabularies amongst Registration Agencies occurs, we should return the 'local' term and schema as well as the ‘standardised’ term and schema. Mandatory for each Contributor specified. In this case, roles are going to vary by region, and maybe by grant scheme within a region. Controlled list adapted from Simon Cox's Project Ontology, OpenAIRE ‘Project’ guidelines, NIH definitions, ARC definitions, and DataCite Metadata Schema 4.4 Appendix 1 Table 6.

.. _6.3.2-organisation.role.schemaUri:

6.3.2 organisation.role.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the role schema used.

**Requirement**: Mandatory for each organisation.role.id supplied

**Occurrence**: 0-1

**Allowed values**: *Closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: Controlled list shared across all Registration Agencies.

.. _6.3.3-organisation.role.startDate:

6.3.3 organisation.role.startDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Date the contributor began role associated with the project or activity.

**Requirement**: Mandatory for each organisation.role supplied

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2026-08-28``; ``2026-08``; ``2026``

**Note**: Only year is required, month and day are optional (but recommended when available).

.. _6.3.4-organisation.role.endDate:

6.3.4 organisation.role.endDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Date the contributor terminated role associated with the project or activity.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2026-08-28``; ``2026-08``; ``2026``

**Note**: Only year is required, month and day are optional (but recommended when available).