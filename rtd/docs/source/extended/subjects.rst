.. autosummary::
   :toctree: generated

.. _12-subjects:

12 subjects
==============

**Definition**: Metadata schema block containing the subject area of the RAiD plus associated properties.

**Requirement**: Recommended

**Occurrence**: 0-n

**Example JSON**

.. _12.1-subjects.id:

12.1 subjects.id
----------------

**Definition**: Identifier (URI) for a subject area or classification code describing the project or activity.

**Requirement**: Mandatory for each subject supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list of URIs derived from subjects.id.schemaUri*

**Examples**

* https://vocabs.ardc.edu.au/repository/api/lda/anzsrc-2020-for/resource?uri=https://linked.data.gov.au/def/anzsrc-for/2020/430106 (ANZSRC 2020 Fields of Research code: ‘Digital Archaeology’)
* https://id.loc.gov/authorities/subjects/sh85118622.html (LoC 'Science and State')

.. _12.1.1-subjects.id.schemaUri:

12.1.1 subjects.id.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The URI of the subject identifier schema

**Requirement**: Mandatory for each subjects.id supplied

**Occurrence**: 0-1

**Allowed values**: *Open controlled list of URIs*

* https://id.loc.gov/authorities/subjects.html (Library of Congress Subject Headings)
* https://vocabs.ardc.edu.au/viewById/316 (Australian and New Zealand Standard Research Classification 2020: Fields of Research)

**Note**: Registration agencies may add new subject schemas, so long as they are human and machine-readable with a single page per subject area. Note that not all schemes provide a URI for each term (in which case Registration Agencies will need to build and publish their own vocabulary). Schemas must be registered with the Registraiton Authority.

.. _12.2-subjects.keywords:

12.2 subjects.keywords
----------------------

**Definition**: Metadata schema sub-block containing free-text keywords describing a project plus associated properties.

**Requirement**: Optional

**Occurance**: 0-n

.. _12.2.1-subjects.keywords.text:

12.2.1 subjects.keywords.text
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Unconstrained keyword or key phrase describing the project or activity

**Requirement**: Optional

**Occurance**: 1

**Allowed values**: Free text

**Constraints**: Do not duplicate Subject(s) above

12.2.2 subjects.keywords.language
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Metadata schema block declaring the language of the subject keyword text.

**Requirement**: Recommended

**Occurrence**: 0-1

**Example JSON**

.. _12.2.2.1-subjects.keywords.language.id:

12.2.2.1 subjects.keywords.language.id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: Language used for the subject keyword text identified by a code or other identifier.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: *Controlled list from language schema*

**Example**: ``eng`` (*ISO 6129-12 three-letter code*)

**Note**: Currently limited to ISO 6129-12 three-letter code.

.. _12.2.2.2-subjects.keywords.language.schemaUri:

12.2.2.2 subjects.keywords.language.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the language identifier schema.

**Requirement**: Mandatory for each subject.keywords.language supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://www.iso.org/standard/12951212.html``

**Note**: Controlled list shared across all Registration Agencies. No crosswalk; queries return language code and scheme URI.  
