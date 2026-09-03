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

**Note**: Set automatically by the RAiD Service software when a RAiD is created; not user-editable. Epoch seconds are the number of seconds that have passed since 00:00:00 UTC on 1 January 1970, excluding leap seconds, formally defined by the `POSIX.1 Time Standard (IEEE Std 1003.1) <https://pubs.opengroup.org/onlinepubs/9699919799/>`__. Epoch seconds can be converted into a human-readable date and time using free online tools such as `EpochConverter <https://www.epochconverter.com/>`__.

.. _2.2-metadata.updated:

2.2 metadata.updated
----------------------

**Definition**: the date and time the RAiD was last updated

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: system-supplied, read-only

**Format**: epoch seconds

**Note**: Set automatically by the RAiD Service software whenever a RAiD is updated; not user-editable. Epoch seconds are the number of seconds that have passed since 00:00:00 UTC on 1 January 1970, excluding leap seconds, formally defined by the `POSIX.1 Time Standard (IEEE Std 1003.1) <https://pubs.opengroup.org/onlinepubs/9699919799/>`__. Epoch seconds can be converted into a human-readable date and time using free online tools such as `EpochConverter <https://www.epochconverter.com/>`__.
