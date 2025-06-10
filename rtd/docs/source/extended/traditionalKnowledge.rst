.. autosummary::
   :toctree: generated

.. _14-traditionalKnowledge:

14 traditionalKnowledge
=======================

**Definition**: metadata schema block containing information about Traditional Knowledge / Biocultural Labels and Notices

**Requirement**: optional

**Occurrence**: 0-n

**Example JSON**

.. _14.1-traditionalKnowledge.id:

14.1.1 traditionalKnowledge.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: identifier (URI) linking to a verified source for Traditional Knowledge (TK) or Biocultural (BC) Labels or Notices pertaining to a project or activity

**Requirement**: optional

**Occurrence**: 0-n

**Allowed values**: *identifier defined by traditionalKnowledge.schemaUri*

**Examples**:

* https://localcontextshub.org/projects/03818172-23c1-4dd1-a662-f11aa07cccda/ (`Island Sustainability Project 2025`, a Project in Local Contexts Hub) 

**Note**: Currently only Local Contexts Hub Projects are allowed as a source for validated TK/BC Labels and Notices.

.. _14.1.2-traditionalKnowledgeLabel.schemaUri:

14.1.2 traditionalKnowledge.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the Traditional Knowledge or Biocultural label identifier schema

**Requirement**: mandatory for each traditionalKnowledgeLabel supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list of URIs defined at https://vocabulary.raid.org/traditionalKnowledgeLabel.schemaUri/160*

* https://localcontextshub.org/projects/ (Local Contexts Hub Projects)

**Note**: Currently only Local Contexts Hub is supported for validated TK/BC Labels and Notices. 
