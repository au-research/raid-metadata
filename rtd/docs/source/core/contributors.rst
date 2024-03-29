.. autosummary::
   :toctree: generated

.. _5-contributor:

5 contributor
=============

**Definition**: a metadata schema block containing a contributor to a RAiD and their associated properties

**Requirement**: at least one contributor is mandatory

**Occurrence**: 1-n

**Example JSON**

.. _5.1-contributor.id:

5.1 contributor.id
------------------

**Definition**: the contributor (person) associated with a project or activity identified by a persistent identifier (PID)

**Requirement**: mandatory for each contributor supplied

**Occurrence**: 1-n

**Allowed values**: identifier defined by contributor.schemaUri 

.. _5.2-contributor.id.schemaUri:

5.2 contributor.schemaUri
-------------------------

**Definition**: the URI of the contributor identifier schema

**Requirement**: mandatory for each contributor.id supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list*

* ``https://orcid.org/``
* ``https://isni.org/``

**Note**: the controlled list is shared across all Registration Agencies.

.. _5.3-contributor.position:

5.3 contributor.position
------------------------

**Definition**: a metadata schema sub-block describing a contributor's position on a project or activity

**Requirement**: mandatory for each contributor supplied

**Occurrence**: 1

**Note**: contributors must have one and only one position at any given time (but they may also be flagged as a 'leader' or 'contact').

.. _5.3.1-contributor.position.id:

5.3.1 contributor.position.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: a contributor's administrative position in the project

**Requirement**: mandatory for each contributor.position supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from contributor.position.schemaUri*

* Principal or Chief Investigator
* Co-investigator or Collaborator
* Partner Investigator (industry, government, or community collaborator)
* Consultant (consultant or contractor hired by the project)
* Other Participant (not covered by one of the positions above: i.e., 'member' or 'other significant contributor')

**Default**: first-entered Contributor (only) defaults to 'Principal or Chief Investigator'

**Constraints**: one (and only one) Contributor must be designated as 'Principal or Chief Investigator'. 

**Note**: Controlled list adapted from Simon Cox's Project Ontology, OpenAIRE ‘Project’ guidelines, NIH definitions, ARC definitions, and DataCite Metadata Schema 4.4 Appendix 1 Table 5 'Description of contributorType'.

.. _5.3.2-contributor.position.id.schemaUri:

5.3.2 contributor.position.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the position schema used

**Requirement**: mandatory for each contributor.position.id supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]

.. _5.3.3-contributor.position.startDate:

5.3.3 contributor.position.startDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: date the contributor began position associated with the project or activity

**Requirement**: mandatory for each contributor.position.id supplied

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Default**: date record created

**Format**: ``YYYY-MM-DD``

**Examples**: ``2025-08-28``; ``2025-08``; ``2025``

**Note**: only year is required, month and day are optional (but recommended when available).

.. _5.3.4-contributor.position.endDate:

5.3.4 contributor.position.endDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: date the contributor terminated position associated with the project or activity.

**Requirement**: recommended

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2025-08-28``; ``2025-08``; ``2025``

**Note**: only year is required, month and day are optional (but recommended when available).

.. _5.4-contributor.position.leader:

5.4 contributor.leader
----------------------

**Definition**: flag indicating that the contributor as a project leader

**Requirement**: at least one contributor must be flagged as a project leader

**Occurrence**: 0-1

**Allowed values**: Yes / Null

**Note**: more than one contributor can be flagged as a leader if the project is jointly led.

.. _5.5-contributor.position.contact:

5.5 contributor.contact
-----------------------

**Definition**: flag indicating that the contributor as a project contact.

**Requirement**: at least one contributor must be flagged as a project contact.

**Occurrence**: 0-1

**Allowed values**: Yes / Null

**Note**: more than one Contributor can be flagged as a contact.

.. _5.6-contributor.role:

5.6 contributor.role
--------------------

**Definition**: metadata schema sub-block describing a contributor's role on a project using the CRediT system.

**Requirement**: recommended

**Occurrence**: 0-n

**Note**: changes to roles are tracked through version history rather than explicitly declared.

.. _5.6.1-contributor.role.id:

5.6.1 contributor.role.id
^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: a contributor's (person) role(s) on the Project

**Requirement**: mandatory for each contributor.role provided

**Occurrence**: 0-1

**Allowed values**: *closed controlled list from contributor.role.schemaUri*

* ``https://credit.niso.org/contributor-role/conceptualization/``
* ``https://credit.niso.org/contributor-role/data-curation/``
* ``https://credit.niso.org/contributor-role/formal-analysis/``
* ``https://credit.niso.org/contributor-role/funding-acquisition/``
* ``https://credit.niso.org/contributor-role/investigation/``
* ``https://credit.niso.org/contributor-role/methodology/``
* ``https://credit.niso.org/contributor-role/project-administration/``
* ``https://credit.niso.org/contributor-role/resources/``
* ``https://credit.niso.org/contributor-role/software/``
* ``https://credit.niso.org/contributor-role/supervision/``
* ``https://credit.niso.org/contributor-role/validation/``
* ``https://credit.niso.org/contributor-role/visualization/``
* ``https://credit.niso.org/contributor-role/writing-original-draft/``
* ``https://credit.niso.org/contributor-role/writing-review-editing/``

.. _5.6.2-contributor.role.id.schemaUri:

5.6.2 contributor.role.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the role schema used

**Requirement**: mandatory for each contributor.role.id provided

**Occurrence**: 0-1

**Allowed values**: *closed controlled list*

* ``https://credit.niso.org/``