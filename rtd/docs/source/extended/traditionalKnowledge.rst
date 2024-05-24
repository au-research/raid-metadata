.. autosummary::
   :toctree: generated

.. _13-traditionalKnowledgeLabel:

13 traditionalKnowledgeLabel
============================

**Definition**: metadata schema block containing information about Traditional Knowledge or Biocultural labels

**Requirement**: optional

**Occurrence**: 0-n

**Example JSON**

**Note**: The Traditional Knowledge (TK) and Biocultural (BC) Labels are tools for Indigenous communities and local organizations. Developed through sustained partnership and testing within Indigenous communities across multiple countries, the Labels allow communities to express local and specific conditions for sharing and engaging in future research and relationships in ways that are consistent with already existing community rules, governance, and protocols for using, sharing, and circulating knowledge and data. Labels can be applied to websites, publications, datasets, museum exhibitions, items in a collection, genetic samples, and more. Communities can customize and apply their TK and BC Labels using the Local Contexts Hub. *Labels should only be used by or in conjunction with Indigenous communities and local organizations*. Institutions and researchers should use 'Notices' instead. See https://localcontexts.org/labels/about-the-labels/ for more information.

.. _13.1-traditionalKnowledgeLabel.id:

13.1 traditionalKnowledgeLabel.id
---------------------------------

**Definition**: identifier (URI) for a Traditional Knowledge or Biocultural label pertaining to a project or activity

**Requirement**: optional

**Occurrence**: 0-n

**Allowed values**: *closed controlled list of URIs derived from traditionalKnowledgeLabel.schemaUri*

**Examples**:

* https://localcontexts.org/label/tk-attribution/ (Local Contexts TK Label 'TK Atribution (TK A)')
* https://localcontexts.org/label/bc-provenance/ (Local Contexts BC Label 'BC Provenance (BC P))''

**Note**: TraditionalKnowledgeLabel.id may be omitted if a project wishes to specify only the scheme used, and not the range of labels used.

.. _13.2-traditionalKnowledgeLabel.schemaUri:

13.2 traditionalKnowledgeLabel.schemaUri
----------------------------------------

**Definition**: the URI of the Traditional Knowledge or Biocultural label identifier schema

**Requirement**: mandatory for each traditionalKnowledgeLabel supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list of URIs defined at https://vocabulary.raid.org/traditionalKnowledgeLabel.schemaUri/160*

* https://localcontexts.org/labels/traditional-knowledge-labels/ (Traditional Knowledge labels)
* https://localcontexts.org/labels/biocultural-labels/ (Biocultural labels)

**Note**: Users may select a traditionalKnowledgeLabel.schemaUri without specifying a traditionalKnowlegeLabel.id, if a project only wants to declare only the schema used without specifying what labels may be used. 

.. _14-traditionalKnowledgeNotice:

14 traditionalKnowledgeNotice
=============================

**Definition**: metadata schema block containing information about Traditional Knowledge Notices

**Requirement**: optional

**Occurrence**: 0-n

**Example JSON**

**Note**: The Notices are tools for institutions and researchers to identify Indigenous collections and data and recognize Indigenous rights and interests. The Notices were developed to create pathways for partnership, collaboration, and support of Indigenous cultural authority. Notices can be applied to websites, publications, datasets, museum exhibitions, items in a collection, genetic samples, and more. Institutions and researchers can generate Notices using the Local Contexts Hub. See https://localcontexts.org/notices/about-the-notices// for more information.

.. _14.1-traditionalKnowledgeNotice.id:

14.1 traditionalKnowledgeNotice.id
----------------------------------

**Definition**: identifier (URI) for a Traditional Knowledge Notice pertaining to a project or activity

**Requirement**: optional

**Occurrence**: 0-n

**Allowed values**: *closed controlled list of URIs derived from traditionalKnowledgeNotice.schemaUri*

* ``https://localcontexts.org/notice/attribution-incomplete/``
* ``https://localcontexts.org/notice/authorization/``
* ``https://localcontexts.org/notice/bc-notice/``
* ``https://localcontexts.org/notice/belonging/``
* ``https://localcontexts.org/notice/caring/``
* ``https://localcontexts.org/notice/gender-aware/``
* ``https://localcontexts.org/notice/leave-undisturbed/``
* ``https://localcontexts.org/notice/open-to-collaborate/``
* ``https://localcontexts.org/notice/safety/``
* ``https://localcontexts.org/notice/tk-notice/``
* ``https://localcontexts.org/notice/viewing/``
* ``https://localcontexts.org/notice/withholding/``

**Note**: TraditionalKnowledgeNotice.id may be omitted if a project wishes to specify only the scheme used, and not the range of notices used.

.. _14.2-traditionalKnowledgeNotice.schemaUri:

14.2 traditionalKnowledgeNotice.schemaUri
-----------------------------------------

**Definition**: the URI of the Traditional Knowledge or Biocultural label identifier schema

**Requirement**: mandatory for each traditionalKnowledgeNotice supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list of URIs defined at https://vocabulary.raid.org/traditionalKnowledgeNotice.schemaUri/287*

* ``https://localcontexts.org/notice/open-to-collaborate/``
* ``https://localcontexts.org/notices/cc-notices/``
* ``https://localcontexts.org/notices/disclosure-notices/``

**Note**: Users may select a traditionalKnowledgeNotice.schemaUri without specifying a traditionalKnowlegeNotice.id, if a project only wants to declare only the schema used without specifying what notices may be used. 