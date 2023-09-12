.. autosummary::
   :toctree: generated

.. _12-subject:

12 subject
==========

**Definition**: Metadata schema block containing the subject area of the RAiD plus associated properties.

**Requirement**: Recommended

**Occurrence**: 0-n

**Example JSON**

.. _12.1-subject.id:

12.1 subject.id
---------------

**Definition**: Identifier (URI) for a subject area or classification code describing the project or activity.

**Requirement**: Mandatory for each subject supplied

**Occurrence**: 0-1

**Allowed values**: *Closed controlled list of URIs derived from the schema chosen at subject.id.schemaUri*

**Examples**

* https://vocabs.ardc.edu.au/repository/api/lda/anzsrc-2020-for/resource?uri=https://linked.data.gov.au/def/anzsrc-for/2020/430106 (ANZSRC 2020 Fields of Research code: ‘Digital Archaeology’)
* https://id.loc.gov/authorities/subject/sh85118622.html (LoC 'Science and State')

.. _12.2-subject.schemaUri:

12.2 subject.schemaUri
----------------------

**Definition**: The URI of the subject identifier schema

**Requirement**: Mandatory for each subject.id supplied

**Occurrence**: 0-1

**Allowed values**: *Open controlled list of URIs*

* https://id.loc.gov/authorities/subject.html (Library of Congress Subject Headings)
* https://vocabs.ardc.edu.au/viewById/316 (Australian and New Zealand Standard Research Classification 2020: Fields of Research)

.. _12.3-subject.keyword:

12.3 subject.keyword
--------------------

**Definition**: Metadata schema sub-block containing free-text keyword describing a project plus associated properties.

**Requirement**: Optional

**Occurrence**: 0-n

.. _12.3.1-subject.keyword.text:

12.3.1 subject.keyword.text
^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Unconstrained keyword or key phrase describing the project or activity

**Requirement**: Optional

**Occurrence**: 1

**Allowed values**: Free text

**Constraints**: Do not duplicate Subject(s) above

.. _12.3.2-subject.keyword.language:

12.3.2 subject.keyword.language
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Metadata schema block declaring the language of the subject keyword text.

**Requirement**: Recommended for each subject.keyword.text supplied

**Occurrence**: 0-1

**Example JSON**

.. _12.3.2.1-subject.keyword.language.id:

12.3.2.1 subject.keyword.language.id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: Language used for the subject keyword text identified by a code or other identifier.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: *Controlled list derived from subject.keyword.language.schemaUri*

**Example**: ``eng`` (*ISO 6129-12 three-letter code*)

.. _12.3.2.2-subject.keyword.language.schemaUri:

12.3.2.2 subject.keyword.language.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the language identifier schema.

**Requirement**: Mandatory for each subject.keyword.language.id supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://www.iso.org/standard/12951212.html``

**Note**: Currently limited to ISO 6129-12 three-letter code.