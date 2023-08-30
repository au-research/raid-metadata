.. autosummary::
   :toctree: generated

.. _5-dontributors:

5 contributors
==============

**Definition**: Metadata schema block containing contributors to a RAiD and associated properties.

**Requirement**: At least one contributor is mandatory

**Occurrence**: 1-n

**Example JSON**

.. _5.1-contributors.id:

5.1 contributors.id
-------------------

**Definition**: Contributor (person) associated with a project or activity identified by a PID.

**Requirement**: Mandatory for each contributor supplied

**Occurrence**: 1-n

**Allowed values**: ORCID or ISNI

.. _5.1.1-contributors.id.schemaURI:

5.1.1 contributors.id.schemaURI
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the contributor identifier schema.

**Requirement**: Mandatory for each contributors.id supplied

**Occurrence**: 1

**Allowed values**: *Controlled list*

* ``https://orcid.org/``
* ``https://isni.org/``


**Note**: Controlled list shared across all Registration Agencies.

.. _5.2-contributors.position:

5.2 contributors.position
-------------------------

**Definition**: Metadata schema sub-block describing a contributor's position on a project.

**Requirement**: Mandatory for each contributor supplied

**Occurrence**: 1

**Note**: Contributors must have one and only one position at any given time (but may also be flagged as a 'leader' or 'contact').

.. _5.2.1-contributors.position.id:

5.2.1 contributors.position.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Contributor's administrative position in the project.

**Requirement**: Mandatory for each contributors.position supplied

**Occurrence**: 1

**Allowed values**: *Controlled list*

* Principal or Chief Investigator
* Co-investigator or Collaborator
* Partner Investigator (industry, government, or community collaborator)
* Consultant (consultant or contractor hired by the project)
* Other Participant (not covered by one of the positions above; ‘member’; ‘other * significant contributor’)

**Note**: In 'core' elements where variation of controlled vocabularies amongst Registration Agencies is allowed, Registration Agencies must provide a crosswalk. In 'core' elements where variation of controlled vocabularies amongst Registration Agencies occurs, we should return the 'local' term and schema as well as the ‘standardised’ term and schema. Mandatory for each Contributor specified. In this case, Positions are going to vary by region, and maybe by grant scheme within a region. Controlled list adapted from Simon Cox's Project Ontology, OpenAIRE ‘Project’ guidelines, NIH definitions, ARC definitions, and DataCite Metadata Schema 4.4 Appendix 1 Table 5.

.. _5.2.1.1-contributors.position.id.schemaURI:

5.2.1.1 contributors.position.id.schemaURI
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the position schema used.

**Requirement**: Mandatory for each contributors.position.id supplied

**Occurrence**: 1

**Allowed values**: *Controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: Controlled list shared across all Registration Agencies.

.. _5.2.2-contributors.position.startDate:

5.2.2 contributors.position.startDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Date the contributor began position associated with the project or activity.

**Requirement**: Mandatory for each contributors.positionsupplied

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2025-08-28``; ``2025-08``; ``2025``

**Note**: Only year is required, month and day are optional (but recommended when available).

.. _5.2.3-contributors.position.endDate:

5.2.3 contributors.position.endDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Date the contributor terminated position associated with the project or activity.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2025-08-28``; ``2025-08``; ``2025``

**Note**: Only year is required, month and day are optional (but recommended when available).

.. _5.2.4-contributors.position.leader:

5.2.4 contributors.position.leader
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Flag indicating that the contributor as a project leader.

**Requirement**: At least one contributor must be flagged as a project leader.

**Occurrence**: 0-1

**Allowed values**: Yes / Null

**Note**: More than one contributor can be flagged as a leader if the project is jointly led.

.. _5.2.5-contributors.position.contact:

5.2.5 contributors.position.contact
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Flag indicating that the contributor as a project contact.

**Requirement**: At least one contributor must be flagged as a project contact.

**Occurrence**: 0-1

**Allowed values**: Yes / Null

**Note**: More than one Contributor can be flagged as a contact.

.. _5.3-contributors.roles:

5.3 contributors.roles
----------------------

**Definition**: Metadata schema sub-block describing a contributor's role on a project using the CRediT system.

**Requirement**: Recommended

**Occurrence**: 0-n

**Note**: Changes to roles are tracked through version history.

.. _5.3.1-contributors.roles.id:

5.3.1 contributors.roles.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: A contributor's (person) role(s) on the Project.

**Requirement**: Mandatory for each contributors.roles provided

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://credit.niso.org/contributor-roles/conceptualization/``
* ``https://credit.niso.org/contributor-roles/data-curation/``
* ``https://credit.niso.org/contributor-roles/formal-analysis/``
* ``https://credit.niso.org/contributor-roles/funding-acquisition/``
* ``https://credit.niso.org/contributor-roles/investigation/``
* ``https://credit.niso.org/contributor-roles/methodology/``
* ``https://credit.niso.org/contributor-roles/project-administration/``
* ``https://credit.niso.org/contributor-roles/resources/``
* ``https://credit.niso.org/contributor-roles/software/``
* ``https://credit.niso.org/contributor-roles/supervision/``
* ``https://credit.niso.org/contributor-roles/validation/``
* ``https://credit.niso.org/contributor-roles/visualization/``
* ``https://credit.niso.org/contributor-roles/writing-original-draft/``
* ``https://credit.niso.org/contributor-roles/writing-review-editing/``


**Note**: In 'core' elements where variation of controlled vocabularies amongst Registration Agencies is allowed, Registration Agencies must provide a crosswalk. In 'core' elements where variation of controlled vocabularies amongst Registration Agencies occurs, we should return the 'local' term and schema as well as the ‘standardised’ term and schema. 

.. _5.3.1.1-contributors.roles.id.schemaURI:

5.3.1.1 contributors.roles.id.schemaURI
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the roles schema used.

**Requirement**: Mandatory for each contributors.roles.id provided

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://credit.niso.org/``

**Note**: Registration Agencies may implement other contributorRole controlled vocabularies but must provide a crosswalk to CRediT. 
