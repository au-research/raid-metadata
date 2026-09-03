.. autosummary::
   :toctree: generated

.. _6-contributor:

6 contributor
=============

**Definition**: a metadata schema block containing a contributor to a RAiD and their associated properties

**Requirement**: at least one contributor is mandatory

**Occurrence**: 1-n

**Example JSON**

.. code-block:: json

   {
     "contributor": [
       {
         "id": "https://orcid.org/0000-0002-1825-0097",
         "schemaUri": "https://orcid.org/",
         "position": [
           {
             "id": "https://vocabulary.raid.org/contributor.position.schema/307",
             "schemaUri": "https://vocabulary.raid.org/contributor.position.schema/305",
             "startDate": "2024-03-01"
           }
         ],
         "role": [
           {
             "id": "https://credit.niso.org/contributor-roles/conceptualization/",
             "schemaUri": "https://credit.niso.org/"
           },
           {
             "id": "https://credit.niso.org/contributor-roles/supervision/",
             "schemaUri": "https://credit.niso.org/"
           }
         ],
         "leader": true,
         "contact": true
       },
       {
         "id": "https://orcid.org/0000-0001-9971-0253",
         "schemaUri": "https://orcid.org/",
         "position": [
           {
             "id": "https://vocabulary.raid.org/contributor.position.schema/308",
             "schemaUri": "https://vocabulary.raid.org/contributor.position.schema/305",
             "startDate": "2024-06-01"
           }
         ],
         "role": [
           {
             "id": "https://credit.niso.org/contributor-roles/investigation/",
             "schemaUri": "https://credit.niso.org/"
           }
         ],
         "leader": false,
         "contact": false
       }
     ]
   }

.. _6.1-contributor.id:

6.1 contributor.id
------------------

**Definition**: the contributor (person) associated with a project or activity identified by a persistent identifier (PID)

**Requirement**: mandatory for each contributor supplied

**Occurrence**: 1-n

**Allowed values**: identifier defined by contributor.schemaUri 

.. _6.2-contributor.id.schemaUri:

6.2 contributor.schemaUri
-------------------------

**Definition**: the URI of the contributor identifier schema

**Requirement**: mandatory for each contributor supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list defined at https://vocabulary.raid.org/contributor.schemaUri/215*

* ``https://orcid.org/`` (ORCID)
* ``https://isni.org/`` (ISNI)

**Constraints**: a PID is required; ORCID and ISNI are currently allowed

**Note**: The controlled list of allowed identifier schemas is shared across all Registration Agencies. An ORCID Sandbox schema (``https://sandbox.orcid.org/``) is also present in the controlled list within the RAiD Demo environment. This schema is for the purposes of RAiD testing only and should not be used for real RAiD records minted in the Production environment. ISNI existence is verified against the ISNI registry.

.. _6.3-contributor.position:

6.3 contributor.position
------------------------

**Definition**: a metadata schema sub-block describing a contributor's administrative position on a project or activity

**Requirement**: mandatory for each contributor supplied

**Occurrence**: 1

**Constraints**: contributors must have one and only one position at any given time (contributors may also be flagged as a 'leader' or 'contact' separately)

**Note**: This property represents a contributor's administrative position on a project (such as their position on a grant application); use contributor.role to define for scientific or scholarly contribution.

.. _6.3.1-contributor.position.id:

6.3.1 contributor.position.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: a contributor's administrative position in the project

**Requirement**: mandatory for each contributor.position supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from contributor.position.schemaUri, published at https://vocabulary.raid.org/contributor.position.id/scheme*

* ``https://vocabulary.raid.org/contributor.position.schema/307`` (Principal or Chief Investigator)
* ``https://vocabulary.raid.org/contributor.position.schema/308`` (Co-investigator or Collaborator)
* ``https://vocabulary.raid.org/contributor.position.schema/309`` (Partner Investigator, e.g., industry, government, or community collaborator)
* ``https://vocabulary.raid.org/contributor.position.schema/310`` (Consultant, e.g., someone hired as a contract researcher by the project)
* ``https://vocabulary.raid.org/contributor.position.schema/311`` (Other Participant not covered by one of the positions above, e.g., 'member' or 'other significant contributor')

**Default**: contributor.position.id for first-entered contributor (only) defaults to 'Principal or Chief Investigator' 

.. _6.3.2-contributor.position.id.schemaUri:

6.3.2 contributor.position.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the position schema used

**Requirement**: mandatory for each contributor.position supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list defined at https://vocabulary.raid.org/contributor.position.schemaUri/scheme*

* ``https://vocabulary.raid.org/contributor.position.schema/305``

**Note**: Controlled list informed by Simon Cox's Project Ontology, OpenAIRE ‘Project’ guidelines, NIH definitions, ARC definitions, and DataCite Metadata Schema 4.4 Appendix 1 Table 5 'Description of contributorType'.

.. _6.3.3-contributor.position.startDate:

6.3.3 contributor.position.startDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: date the contributor began position associated with the project or activity

**Requirement**: mandatory for each contributor.position supplied

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Default**: date record created

**Format**: ``YYYY-MM-DD``

**Example(s)**: ``2025-08-28``; ``2025-08``; ``2025``

**Note**: Only year is required, month and day are optional (but recommended when available).

.. _6.3.4-contributor.position.endDate:

6.3.4 contributor.position.endDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: date the contributor terminated position associated with the project or activity

**Requirement**: recommended if the contributor has left the project

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Example(s)**: ``2025-08-28``; ``2025-08``; ``2025``

**Note**: Only year is required, month and day are optional (but recommended when available).

.. _6.4-contributor.position.leader:

6.4 contributor.leader
----------------------

**Definition**: flag indicating that the contributor as a project leader

**Requirement**: at least one contributor must be flagged as a project leader

**Occurrence**: 0-1

**Allowed values**: boolean

* ``true``
* ``false``

**Note**: More than one contributor can be flagged as a leader if the project is jointly led.

.. _6.5-contributor.position.contact:

6.5 contributor.contact
-----------------------

**Definition**: flag indicating that the contributor as a project contact

**Requirement**: at least one contributor must be flagged as a project contact

**Occurrence**: 0-1

**Allowed values**: boolean

* ``true``
* ``false``

**Note**: More than one contributor can be flagged as a contact.

.. _6.6-contributor.role:

6.6 contributor.role
--------------------

**Definition**: metadata schema sub-block describing a contributor's scientific or scholarly role on a project using the CRediT vocabulary

**Requirement**: recommended

**Occurrence**: 0-n

**Note**: Changes to roles are tracked through version history rather than explicitly declared.

.. _6.6.1-contributor.role.id:

6.6.1 contributor.role.id
^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: a contributor's (person) role(s) on the Project

**Requirement**: mandatory for each contributor.role provided

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from contributor.role.schemaUri, published at https://vocabulary.raid.org/contributor.role.id/scheme*

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

.. _6.6.2-contributor.role.id.schemaUri:

6.6.2 contributor.role.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the role schema used

**Requirement**: mandatory for each contributor.role provided

**Occurrence**: 1

**Allowed values**: *closed controlled list defined at https://vocabulary.raid.org/contributor.role.schemaUri/scheme*

* ``https://credit.niso.org/``

**Constraints**: currently limited to the CRediT vocabulary 
