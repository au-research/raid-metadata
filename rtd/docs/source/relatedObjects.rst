.. autosummary::
   :toctree: generated

.. _7-relatedObjects:

7 relatedObjects
================

**Definition**: Metadata schema block containing inputs, outputs, and process documents related to a RAiD plus associated properties.

**Requirement**: Recommended

**Occurrence**: 0-n

**Example JSON**

.. _7.1-relatedObjects.id:

7.1 relatedObjects.id
---------------------

**Definition**: Any (a) input or resource used by a project or activity, (b) output or product created b a project or activity, or (c) internal process documentation used within a project or activity, identified by a PID.

**Requirement**: Mandatory for each relatedObject supplied

**Occurrence**: 0-1

**Allowed values**: PID of any type listed at 7.1.1

.. _7.1.1-relatedObjects.id.schemaURI:

7.1.1 relatedObjects.id.schemaURI
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the relatedObject identifier schema.

**Requirement**: Mandatory for each relatedObjects.id supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* https://arks.org/ 
* http://doi.org/ (*includes IGSNs, CrossRef Publication IDs or Grant IDs, DataCite DOIs, instrument DOIs, etc*)
* http://hdl.handle.net/
* https://www.isbn-international.org/ (IBSN)
* https://scicrunch.org/resolver/ (RRID)
* https://archive.org/ (*fallback for any Object that has no ID other than a webpage - a snapshot must be taken from archive.org and that link inserted into the RAiD*).

**Note**: Controlled list shared across all Registration Agencies. Controlled list is a subset of DataCite Metadata Schema 4.4 Appendix 1 Table 8 'relatedIdentiferType'.

.. _7.2-relatedObjects.type:

7.2 relatedObjects.type
-----------------------

**Definition**: Metadata schema sub-block describing a relatedObject's type.

**Requirement**: Mandatory for each relatedObject supplied

**Occurrence**: 0-1

.. _7.2.1-relatedObjects.type.id:

7.2.1 relatedObjects.type.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Type of input, output, or process document.

**Requirement**: Mandatory for each relatedObjects.type supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* Audiovisual
* Book
* BookChapter
* Computational Notebook
* Conference Paper
* Conference Poster
* Conference Proceeding
* DataPaper
* Dataset
* Dissertation
* Educational Material
* Event
* Funding (includes ‘grant’ or other cash or in-kind awards)
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

**Note**: Controlled list is a subset of DataCite Metadata Schema 4.4 Appendix 1 Table 7  'resourceTypeGeneral', with 'Instrument', 'Funding', ‘Educational Material’, ‘Conference Poster’, and 'Prize' added (DataCite Metadata Schema 4.5 also adds ‘Instrument’).

.. _7.2.1.1-relatedObjects.type.id.schemaURI:

7.2.1.1 relatedObjects.type.id.schemaURI
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the type schema used.

**Requirement**: Mandatory for each relatedObjects.type.id supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: The Controlled list adapted from DataCite Metadata Schema 4.4 is specified for raid.org and used by ARDC registration service. Registration Agencies may implement other controlled vocabularies but must provide a crosswalk. In 'core' elements where variation of controlled vocabularies amongst Registration Agencies occurs, we should return the 'local' term and schema as well as the ‘standardised’ term and schema.

.. _7.3-relatedObjects.categories:

7.3 relatedObjects.categories
-----------------------------

**Definition**: Metadata schema sub-block declaring that a relatedObject is an input, output, and/or process document.

**Requirement**: Mandatory for each relatedObject supplied

**Occurrence**: 0-n

**Note**: A relatedObject may have more than one category, e.g., it a DMP could initially be a process document, but eventually be published as an output.

.. _7.3.1-relatedObjects.categories.id:

7.3.1 relatedObjects.categories.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Declaration of an object as an input, output, or other.

**Requirement**: Mandatory for each relatedObject.categories supplied.

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* Input
* Output
* Internal process document or artefact

**Note**: Controlled list developed for RAiD.

.. _7.3.1.1-relatedObjects.type.id.schemaURI:

7.3.1.1 relatedObjects.categories.id.schemaURI
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the category schema used.

**Requirement**: Mandatory for each relatedObjects.category.id supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* [URI of RAiD vocab on RVA (to be created)]

**Note**: Registration Agencies may implement other controlled vocabularies but must provide a crosswalk. In 'core' elements where variation of controlled vocabularies amongst Registration Agencies occurs, we should return the 'local' term and schema as well as the ‘standardised’ term and schema.