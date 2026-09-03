.. autosummary::
   :toctree: generated

.. _3-date:

3 date
======

**Definition**: a metadata schema block containing the start and end date of the RAiD

**Requirement**: mandatory

**Occurrence**: 1

**Example JSON**

.. code-block:: json

   {
     "date": {
       "startDate": "2024-03-01",
       "endDate": "2027-02-28"
     }
   }

.. _3.1-date.startDate:

3.1 date.startDate
------------------

**Definition**: the project or activity's start date

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Default**: date record created

**Format**: ``YYYY-MM-DD``

**Example(s)**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: Only the year is required, month and day are optional (but recommended when available).

.. _3.2-date.endDate:

3.2 date.endDate
----------------

**Definition**: the project or activity's end date

**Requirement**: recommended if a project has concluded

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Example(s)**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: Only year is required, month and day are optional (but recommended when available). An end date should be supplied when a project concludes. Providing an end date terminates active management of, and Registration Agency / Identifier Owner responsibility for, a RAiD. Once a RAiD has an end date, it should be considered archival only.
