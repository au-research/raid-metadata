.. autosummary::
   :toctree: generated

.. _2-metadata:

2 metadata
===========

**Definition**: a metadata schema block containing system-managed record-keeping properties for the RAiD

**Requirement**: mandatory

**Occurrence**: 1

**Example JSON**

.. _2.1-metadata.created:

2.1 metadata.created
----------------------

**Definition**: the date and time the RAiD was created

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: system-supplied, read-only

**Format**: epoch seconds

**Note**: Set automatically by the RAiD Service software when a RAiD is created; not user-editable.

.. _2.2-metadata.updated:

2.2 metadata.updated
----------------------

**Definition**: the date and time the RAiD was last updated

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: system-supplied, read-only

**Format**: epoch seconds

**Note**: Set automatically by the RAiD Service software whenever a RAiD is updated; not user-editable.
