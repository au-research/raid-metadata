.. autosummary::
   :toctree: generated

.. _2-date:

2 date
======

**Definition**: a metadata schema block containing the start and end date of the RAiD.

**Requirement**: mandatory

**Occurrence**: 1

**Example JSON**

.. _2.1-date.startDate:

2.1 date.startDate
------------------

**Definition**: the project or activity's start date

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: only the year is required, month and day are optional (but recommended when available).

.. _2.2-date.endDate:

2.2 date.endDate
----------------

**Definition**: the project or activity's end date

**Requirement**: recommended

**Occurrence**: 0-1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: only year is required, month and day are optional (but recommended when available). An end date should be supplied when a project concludes. Providing an end date terminates active management of and Registration Agency / owner responsibility for a RAiD. Once a RAiD has an end date, it is archival only.