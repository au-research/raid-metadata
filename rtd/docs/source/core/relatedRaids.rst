.. autosummary::
   :toctree: generated

.. _10-relatedRaid:

10 relatedRaid
==============

**Definition**: a metadata schema block containing related RAiDs and qualifying the relationship

**Requirement**: optional

**Occurrence**: 0-n

**Example JSON**

.. _10.1-relatedRaid.id:

10.1 relatedRaid.id
-------------------

**Definition**: a subsidiary or otherwise related RAiD

**Requirement**: mandatory for each relatedRaid supplied

**Occurrence**: 1

**Allowed values**: RAiD name

.. _10.2-relatedRaid.id.type:

10.2 relatedRaid.type
----------------------

**Definition**: a metadata schema sub-block qualifying the relationship with a related Raid

**Requirement**: mandatory for each relatedRaid supplied

**Occurrence**: 1

.. _10.2.1-relatedRaid.type.id:

10.2.1 relatedRaid.type.id
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: a description of the relationship between the activity being registered and the related resource

**Requirement**: mandatory for each relatedRaid.type supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from relatedRaid.type.schemaUri*

* ``https://vocabulary.raid.org/relatedRaid.type.schema/204`` (Continues)
* ``https://vocabulary.raid.org/relatedRaid.type.schema/203`` (IsContinuedBy)
* ``https://vocabulary.raid.org/relatedRaid.type.schema/201`` (HasPart)
* ``https://vocabulary.raid.org/relatedRaid.type.schema/202`` (IsPartOf)
* ``https://vocabulary.raid.org/relatedRaid.type.schema/199`` (IsSourceOf)
* ``https://vocabulary.raid.org/relatedRaid.type.schema/200`` (IsDerivedFrom)
* ``https://vocabulary.raid.org/relatedRaid.type.schema/198`` (Obsoletes, for resolving duplicate RAiDs)
* ``https://vocabulary.raid.org/relatedRaid.type.schema/205`` (IsObsoletedBy, for resolving duplicate RAiDs)

**Note**: Controlled list is a subset of DataCite Schema v4.4 Table 8 'Description of relatedIdentifierType'. All list items appear in the DataCite Schema. 

.. _10.2.2-relatedRaid.type.schemaUri:

10.2.2 relatedRaid.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the relationship schema used

**Requirement**: mandatory for each relatedRaid.type supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list defined at https://vocabulary.raid.org/relatedRaid.type.schemaUri/285*

* https://vocabulary.raid.org/relatedRaid.type.schema/367