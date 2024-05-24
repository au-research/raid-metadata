.. autosummary::
   :toctree: generated

.. _7-relatedObject:

7 relatedObject
===============

**Definition**: a metadata schema block containing inputs, outputs, and process documents related to a RAiD plus associated properties

**Requirement**: recommended

**Occurrence**: 0-n

**Example JSON**

.. _7.1-relatedObject.id:

7.1 relatedObject.id
--------------------

**Definition**: any (a) input or resource used by a project or activity, (b) output or product created by a project or activity, and/or (c) internal process documentation used within a project or activity, that is identified by a persistent identifier (PID).

**Requirement**: mandatory for each relatedObject supplied

**Occurrence**: 1

**Allowed values**: an identifier as specified by relatedObject.schemaUri

.. _7.2-relatedObject.id.schemaUri:

7.2 relatedObject.schemaUri
---------------------------

**Definition**: The URI of the relatedObject identifier schema

**Requirement**: mandatory for each relatedObject.id supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list defined by https://vocabulary.raid.org/relatedObject.schemaUri/218*

* https://arks.org/ 
* http://doi.org/ (*all DOIs, including IGSNs, CrossRef Publication IDs or Grant IDs, DataCite DOIs, instrument DOIs, etc.*)
* http://hdl.handle.net/ (*all non-DOI handles*)
* https://www.isbn-international.org/ 
* https://scicrunch.org/resolver/ (*RRID*)
* https://archive.org/ (*fallback for any Object that has no ID other than a webpage - a snapshot must be taken from archive.org and that link inserted into the RAiD*).

**Note**: Controlled list is a subset of DataCite Metadata Schema 4.4 Appendix 1 Table 8 'Description of relatedIdentiferType'.

.. _7.3-relatedObject.type:

7.3 relatedObject.type
----------------------

**Definition**: a metadata schema sub-block describing a relatedObject's type

**Requirement**: mandatory for each relatedObject supplied

**Occurrence**: 1

.. _7.3.1-relatedObject.type.id:

7.3.1 relatedObject.type.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: a type of input, output, or process document

**Requirement**: mandatory for each relatedObject.type supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from relatedObject.type.schemaUri*

* ``https://vocabulary.raid.org/relatedObject.type.schema/273`` (Audiovisual)
* ``https://vocabulary.raid.org/relatedObject.type.schema/258`` (Book)
* ``https://vocabulary.raid.org/relatedObject.type.schema/271`` (Book Chapter)
* ``https://vocabulary.raid.org/relatedObject.type.schema/256`` (Computational Notebook)
* ``https://vocabulary.raid.org/relatedObject.type.schema/264`` (Conference Paper)
* ``https://vocabulary.raid.org/relatedObject.type.schema/248`` (Conference Poster)
* ``https://vocabulary.raid.org/relatedObject.type.schema/262`` (Conference Proceeding)
* ``https://vocabulary.raid.org/relatedObject.type.schema/255`` (Data Paper)
* ``https://vocabulary.raid.org/relatedObject.type.schema/269`` (Dataset)
* ``https://vocabulary.raid.org/relatedObject.type.schema/253`` (Dissertation)
* ``https://vocabulary.raid.org/relatedObject.type.schema/260`` (Event)
* ``https://vocabulary.raid.org/relatedObject.type.schema/272`` (Funding, including grants or other cash or in-kind awards, but not prizes)
* ``https://vocabulary.raid.org/relatedObject.type.schema/257`` (Image)
* ``https://vocabulary.raid.org/relatedObject.type.schema/266`` (Instrument)
* ``https://vocabulary.raid.org/relatedObject.type.schema/250`` (Journal Article)
* ``https://vocabulary.raid.org/relatedObject.type.schema/267`` (Learning Object)
* ``https://vocabulary.raid.org/relatedObject.type.schema/263`` (Model)
* ``https://vocabulary.raid.org/relatedObject.type.schema/247`` (Output Management Plan)
* ``https://vocabulary.raid.org/relatedObject.type.schema/270`` (Physical Object)
* ``https://vocabulary.raid.org/relatedObject.type.schema/254`` (Preprint)
* ``https://vocabulary.raid.org/relatedObject.type.schema/268`` (Prize, excluding funded awards)
* ``https://vocabulary.raid.org/relatedObject.type.schema/252`` (Report)
* ``https://vocabulary.raid.org/relatedObject.type.schema/274`` (Service)
* ``https://vocabulary.raid.org/relatedObject.type.schema/259`` (Software)
* ``https://vocabulary.raid.org/relatedObject.type.schema/261`` (Sound)
* ``https://vocabulary.raid.org/relatedObject.type.schema/251`` (Standard)
* ``https://vocabulary.raid.org/relatedObject.type.schema/265`` (Text)
* ``https://vocabulary.raid.org/relatedObject.type.schema/249`` (Workflow)

**Note**: Controlled list is a subset of DataCite Metadata Schema 4.4 Appendix 1 Table 7  'Description of resourceTypeGeneral', with 'Instrument', 'Funding', 'Learning Object', ‘Conference Poster’, and 'Prize' added (DataCite Metadata Schema 4.5 also adds ‘Instrument’). COAR Resource Types 3.1 (https://vocabularies.coar-repositories.org/resource_types/) used as source for missing terms where possible. 

.. _7.3.2-relatedObject.type.schemaUri:

7.3.2 relatedObject.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the type schema used

**Requirement**: mandatory for each relatedObject.type.id supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list defined at https://vocabulary.raid.org/relatedObject.type.schemaUri/283*

* ``https://vocabulary.raid.org/relatedObject.type.schema/329``

.. _7.4-relatedObject.category:

7.4 relatedObject.category
--------------------------

**Definition**:  a metadata schema sub-block declaring that a relatedObject is an input, output and/or process document

**Requirement**: mandatory for each relatedObject supplied

**Occurrence**: 1-n

**Note**: A relatedObject may have more than one category (e.g.) a DMP could initially be a process document, yet eventually be published as an output.

.. _7.4.1-relatedObject.category.id:

7.4.1 relatedObject.category.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: a declaration of an object as an input, output, or other

**Requirement**: mandatory for each relatedObject.category supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from relatedObject.category.schemUri*

* ``https://vocabulary.raid.org/relatedObject.category.id/191`` (Input)
* ``https://vocabulary.raid.org/relatedObject.category.id/192`` (Internal process document or artefact)
* ``https://vocabulary.raid.org/relatedObject.category.id/190`` (Output)

.. _7.4.2-relatedObject.type.id.schemaUri:

7.4.2 relatedObject.category.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the category schema used.

**Requirement**: mandatory for each relatedObject.category.id supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list defined at https://vocabulary.raid.org/relatedObject.category.schemaUri/386*

* https://vocabulary.raid.org/relatedObject.category.schema/385