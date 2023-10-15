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

**Occurrence**: 0-1

**Allowed values**: an identifier specified by relatedObject.schemaUri

.. _7.2-relatedObject.id.schemaUri:

7.2 relatedObject.schemaUri
---------------------------

**Definition**: The URI of the relatedObject identifier schema

**Requirement**: mandatory for each relatedObject.id supplied

**Occurrence**: 0-1

**Allowed values**: *closed controlled list*

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

**Occurrence**: 0-1

.. _7.3.1-relatedObject.type.id:

7.3.1 relatedObject.type.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: a type of input, output, or process document

**Requirement**: mandatory for each relatedObject.type supplied

**Occurrence**: 0-1

**Allowed values**: *closed controlled list derived from relatedObject.type.schemaUri*

* Audiovisual
* Book
* Book Chapter
* Computational Notebook
* Conference Paper
* Conference Poster
* Conference Proceeding
* Data Paper
* Dataset
* Dissertation
* Learning Object
* Event
* Funding (includes 'grant' or other cash or in-kind awards)
* Image
* Instrument
* Journal Article
* Model
* Output Management Plan
* Physical Object
* Preprint
* Prize
* Report
* Service
* Software
* Sound
* Standard
* Text
* Workflow

**Note**: Controlled list is a subset of DataCite Metadata Schema 4.4 Appendix 1 Table 7  'Description of resourceTypeGeneral', with 'Instrument', 'Funding', 'Learning Object', ‘Conference Poster’, and 'Prize' added (DataCite Metadata Schema 4.5 also adds ‘Instrument’). COAR Resource Types 3.1 (https://vocabularies.coar-repositories.org/resource_types/) used as source for missing terms where possible. 

.. _7.3.2-relatedObject.type.schemaUri:

7.3.2 relatedObject.type.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the type schema used

**Requirement**: mandatory for each relatedObject.type.id supplied

**Occurrence**: 0-1

**Allowed values**: *closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]

.. _7.4-relatedObject.category:

7.4 relatedObject.category
--------------------------

**Definition**:  a metadata schema sub-block declaring that a relatedObject is an input, output and/or process document

**Requirement**: mandatory for each relatedObject supplied

**Occurrence**: 0-n

**Note**: a relatedObject may have more than one category (e.g.) a DMP could initially be a process document, yet eventually be published as an output.

.. _7.4.1-relatedObject.category.id:

7.4.1 relatedObject.category.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: a declaration of an object as an input, output, or other

**Requirement**: mandatory for each relatedObject.category supplied

**Occurrence**: 0-1

**Allowed values**: *closed controlled list derived from relatedObject.category.schemUri*

* Input
* Output
* Internal process document or artefact

.. _7.4.2-relatedObject.type.id.schemaUri:

7.4.2 relatedObject.category.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the category schema used.

**Requirement**: mandatory for each relatedObject.category.id supplied

**Occurrence**: 0-1

**Allowed values**: *closed controlled list*

* [URI of RAiD vocab on RVA (to be created)]