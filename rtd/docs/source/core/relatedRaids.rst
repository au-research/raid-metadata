.. autosummary::
   :toctree: generated

.. _10-relatedRaid:

10 relatedRaid
==============

**Definition**: Metadata schema block containing related RAiDs and qualifying the relationship.

**Requirement**: Optional

**Occurrence**: 0-n

**Example JSON**

.. _10.1-relatedRaid.id:

10.1 relatedRaid.id
-------------------

**Definition**: Subsidiary or otherwise related RAiD.

**Requirement**: Mandatory for each relatedRaid supplied

**Occurrence**: 0-1

**Allowed values**: RAiD name

.. _10.2-relatedRaid.id.type:

10.2 relatedRaid.type
----------------------

**Definition**: Metadata schema sub-block qualifying the relationship with a related Raid.

**Requirement**: Mandatory for each relatedRaid.id supplied

**Occurrence**: 0-1

.. _10.2.1-relatedRaid.type.id:

10.2.1 relatedRaid.type.id
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Description of the relationship between the activity being registered and the related resource.

**Requirement**: Mandatory for each relatedRaid.type supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list derived from relatedRaid.type.schemaUri*

* Continues
* IsContinuedBy
* IsPartOf
* HasPart
* IsDerivedFrom
* IsSourceOf
* Obsoletes (*for resolving duplicate RAiDs*)
* IsObsoletedBy (*for resolving duplicate RAiDs*)

**Note**: Controlled list is a subset of DataCite Schema v4.4 (Table 8 relatedIdentifierType). All list items appear in the DataCite Schema. 

.. _10.2.2-relatedRaid.type.schemaUri:

10.2.2 relatedRaid.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the relationship schema used.

**Requirement**: Mandatory for each relatedRaid.type.id supplied

**Occurrence**: 0-1

**Allowed values**: *Closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: The Controlled list adapted from DataCite Metadata Schema 4.4 and published on Research Vocabularies Australia is specified for raid.org and used by ARDC registration service. Registration Agencies may implement other controlled vocabularies but must provide a crosswalk. In 'core' elements where variation of controlled vocabularies amongst Registration Agencies occurs, we should return the 'local' term and schema as well as the ‘standardised’ term and schema.