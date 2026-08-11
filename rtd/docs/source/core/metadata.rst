.. autosummary::
   :toctree: generated

.. _2-metadata:

2 metadata
===========

**Definition**: a metadata schema block containing system-managed record-keeping properties for the RAiD

**Requirement**: mandatory

**Occurrence**: 1

**Note**: Every property in this block is set and maintained by the RAiD service. Registration Agencies and users cannot supply or alter these values when creating or updating a RAiD. They are documented because they form part of every RAiD metadata record and are returned when a record is retrieved.

**Example JSON**

.. code-block:: json

   {
     "metadata": {
       "created": 1709607127,
       "updated": 1751505715
     }
   }

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
