.. autosummary::
   :toctree: generated

.. _13-traditionalKnowledgeLabel:

13 traditionalKnowledgeLabel
============================

**Definition**: metadata schema block containing information about Traditional Knowledge or Biocultural labels

**Requirement**: optional

**Occurrence**: 0-n

**Example JSON**

.. _13.1-traditionalKnowledgeLabel.id:

13.1 traditionalKnowledgeLabel.id
---------------------------------

**Definition**: identifier (URI) for a Traditional Knowledge or Biocultural label pertaining to a project or activity

**Requirement**: optional

**Occurrence**: 0-n

**Allowed values**: *closed controlled list of URIs derived from traditionalKnowledgeLabel.id.schemaUri*

**Examples**:

* https://localcontexts.org/label/tk-attribution/ (Local Contexts TK Label 'TK Atribution (TK A)')
* https://localcontexts.org/label/bc-provenance/ (Local Contexts BC Label 'BC Provenance (BC P))''

**Note**: traditionalKnowledgeLabel.id may be omitted if a project wishes to specify only the scheme used, and not the range of labels used.

.. _13.2-traditionalKnowledgeLabel.schemaUri:

13.2 traditionalKnowledgeLabel.schemaUri
----------------------------------------

**Definition**: the URI of the Traditional Knowledge or Biocultural label identifier schema

**Requirement**: mandatory for each traditionalKnowledgeLabel.id supplied

**Occurrence**: 0-1

**Allowed values**: *open controlled list of URIs*

* https://localcontexts.org/labels/traditional-knowledge-labels/
* https://localcontexts.org/labels/biocultural-labels/

**Note**: users may select a traditionalKnowledgeLabel.schemaUri without specifying a traditionalKnowlegeLabel.id, if a project only wants to declare only the schema used without specifying what labels may be used. 