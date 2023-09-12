.. autosummary::
   :toctree: generated

.. _5-contributor:

5 contributor
=============

**Definition**: Metadata schema block containing contributor to a RAiD and associated properties.

**Requirement**: At least one contributor is mandatory

**Occurrence**: 1-n

**Example JSON**

.. _5.1-contributor.id:

5.1 contributor.id
------------------

**Definition**: Contributor (person) associated with a project or activity identified by a PID.

**Requirement**: Mandatory for each contributor supplied

**Occurrence**: 1-n

**Allowed values**: Identifier defined by contributor.schemaUri 

.. _5.2-contributor.id.schemaUri:

5.2 contributor.schemaUri
-------------------------

**Definition**: The URI of the contributor identifier schema.

**Requirement**: Mandatory for each contributor.id supplied

**Occurrence**: 1

**Allowed values**: *Closed controlled list*

* ``https://orcid.org/``
* ``https://isni.org/``

.. _5.3-contributor.position:

5.3 contributor.position
------------------------

**Definition**: Metadata schema sub-block describing a contributor's position on a project.

**Requirement**: Mandatory for each contributor supplied

**Occurrence**: 1

**Note**: Contributors must have one and only one position at any given time (but may also be flagged as a 'leader' or 'contact').

.. _5.3.1-contributor.position.id:

5.3.1 contributor.position.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Contributor's administrative position in the project.

**Requirement**: Mandatory for each contributor.position supplied

**Occurrence**: 1

**Allowed values**: *Closed controlled list derived from contributor.position.schemaUri*

* Principal or Chief Investigator
* Co-investigator or Collaborator
* Partner Investigator (industry, government, or community collaborator)
* Consultant (consultant or contractor hired by the project)
* Other Participant (not covered by one of the positions above; ‘member’; ‘other * significant contributor’)

**Default**: First-entered Contributor (only) defaults to 'Principal or Chief Investigator'

**Constraints**: One (and only one) Contributor must be designated as 'Principal or Chief Investigator'. 

**Note**: Controlled list adapted from Simon Cox's Project Ontology, OpenAIRE ‘Project’ guidelines, NIH definitions, ARC definitions, and DataCite Metadata Schema 4.4 Appendix 1 Table 5 'Description of contributorType'.

.. _5.3.2-contributor.position.id.schemaUri:

5.3.2 contributor.position.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the position schema used.

**Requirement**: Mandatory for each contributor.position.id supplied

**Occurrence**: 1

**Allowed values**: *Closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]

.. _5.3.3-contributor.position.startDate:

5.3.3 contributor.position.startDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Date the contributor began position associated with the project or activity.

**Requirement**: Mandatory for each contributor.position.id supplied

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Default**: Date record created

**Format**: ``YYYY-MM-DD``

**Examples**: ``2025-08-28``; ``2025-08``; ``2025``

**Note**: Only year is required, month and day are optional (but recommended when available).

.. _5.3.4-contributor.position.endDate:

5.3.4 contributor.position.endDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Date the contributor terminated position associated with the project or activity.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2025-08-28``; ``2025-08``; ``2025``

**Note**: Only year is required, month and day are optional (but recommended when available).

.. _5.4-contributor.position.leader:

5.4 contributor.leader
----------------------

**Definition**: Flag indicating that the contributor as a project leader.

**Requirement**: At least one contributor must be flagged as a project leader.

**Occurrence**: 0-1

**Allowed values**: Yes / Null

**Constraints**: At least one Contributor must be designated as a Leader. 

**Note**: More than one contributor can be flagged as a leader if the project is jointly led.

.. _5.5-contributor.position.contact:

5.5 contributor.contact
-----------------------

**Definition**: Flag indicating that the contributor as a project contact.

**Requirement**: At least one contributor must be flagged as a project contact.

**Occurrence**: 0-1

**Allowed values**: Yes / Null

**Constraints**: At least one Contributor must be designated as a Contact. 

**Note**: More than one Contributor can be flagged as a contact.

.. _5.6-contributor.role:

5.6 contributor.role
--------------------

**Definition**: Metadata schema sub-block describing a contributor's role on a project using the CRediT system.

**Requirement**: Recommended

**Occurrence**: 0-n

**Note**: Changes to roles are tracked through version history rather than explicitly declared, as with position.

.. _5.6.1-contributor.role.id:

5.6.1 contributor.role.id
^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: A contributor's (person) role(s) on the Project.

**Requirement**: Mandatory for each contributor.role provided

**Occurrence**: 0-1

**Allowed values**: *Controlled list from contributor.role.schemaUri*

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

**Definition**: The URI of the role schema used.

**Requirement**: Mandatory for each contributor.role.id provided

**Occurrence**: 0-1

**Allowed values**: *Closed controlled list*

* ``https://credit.niso.org/``