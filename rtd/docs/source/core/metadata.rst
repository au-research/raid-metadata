.. autosummary::
   :toctree: generated

.. _15-metadata:

15 metadata
===========

**Definition**: a metadata schema block containing system-managed record-keeping properties for the RAiD

**Requirement**: mandatory

**Occurrence**: 1

**Example JSON**

.. _15.1-metadata.created:

15.1 metadata.created
----------------------

**Definition**: the date and time the RAiD was created

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: system-supplied, read-only

**Format**: epoch seconds

**Note**: Set automatically by the RAiD Service software when a RAiD is created; not user-editable.

.. _15.2-metadata.updated:

15.2 metadata.updated
----------------------

**Definition**: the date and time the RAiD was last updated

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: system-supplied, read-only

**Format**: epoch seconds

**Note**: Set automatically by the RAiD Service software whenever a RAiD is updated; not user-editable.
