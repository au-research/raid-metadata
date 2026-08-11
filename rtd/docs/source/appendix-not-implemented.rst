.. autosummary::
   :toctree: generated

.. _appendix-not-implemented:

Appendix: schema components not yet implemented
===============================================

This appendix is **non-normative**. It describes metadata components that have been approved for the RAiD Metadata Schema, or that are published in the RAiD controlled lists, but that the RAiD service does not currently accept. They are recorded here so that Registration Agencies can plan for them, and so that the numbered sections of this documentation describe only what is implemented.

Nothing in this appendix should be used in a RAiD metadata record. Components are moved into the numbered sections when the RAiD service begins accepting them.

.. _appendix-relatedObject.schemaUri:

Additional relatedObject identifier schemes
-------------------------------------------

The controlled list at https://vocabulary.raid.org/relatedObject.schemaUri/scheme publishes six identifier schemes. Two of these, DOI and Web Archive, are accepted by the RAiD service and are documented at :ref:`8.2-relatedObject.id.schemaUri`. The remaining four are published in the controlled list but are not currently accepted:

* ``https://hdl.handle.net/`` (*all non-DOI handles*)
* ``https://scicrunch.org/resolver/`` (*RRID*)
* ``https://arks.org/`` (*Archival Resource Keys*)
* ``https://www.isbn-international.org/`` (*ISBN*)

Validation for Handle and RRID has been built but is not yet released to production. Validation for ARK is planned. No validation work has been scheduled for ISBN.

**Note**: an earlier version of this documentation listed ``https://n2t.net/ark:`` for ARK and ``http://hdl.handle.net/`` for Handle. The forms published in the controlled list, and shown above, are the correct ones.

.. _appendix-traditionalKnowledge:

traditionalKnowledge
--------------------

**Definition**: metadata schema block containing information about Traditional Knowledge (TK) / Biocultural (BC) Labels and Notices

**Requirement**: optional

**Occurrence**: 0-n

**Note**: This metadata block is not implemented in the RAiD service. No RAiD metadata record currently contains a traditionalKnowledge block. It is documented here because the block has been approved for the schema and its identifier schema is published in the RAiD controlled lists.

.. _appendix-traditionalKnowledge.id:

traditionalKnowledge.id
^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: identifier (URI) linking to a verified source for TK or BC Labels or Notices pertaining to a project or activity

**Requirement**: optional

**Occurrence**: 0-1

**Allowed values**: *identifier defined by traditionalKnowledge.schemaUri*

**Examples**:

* https://localcontextshub.org/projects/03818172-23c1-4dd1-a662-f11aa07cccda/ (`Island Sustainability Project 2025`, a Project in Local Contexts Hub)

**Note**: Only Local Contexts Hub Projects are intended as a source for validated TK/BC Labels and Notices.

.. _appendix-traditionalKnowledge.schemaUri:

traditionalKnowledge.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the TK/BC label identifier schema

**Requirement**: mandatory for each traditionalKnowledge supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list of URIs defined at https://vocabulary.raid.org/traditionalKnowledgeLabel.schemaUri/scheme*

* ``https://localcontexts.org/labels/traditional-knowledge-labels/`` (Local Contexts Hub)

**Note**: Only Local Contexts Hub is intended as a source for validated TK/BC Labels and Notices. Earlier versions of this documentation gave the schema URI as ``https://localcontextshub.org/projects/``; the value shown above is the one published in the controlled list.
