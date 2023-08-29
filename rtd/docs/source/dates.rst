.. autosummary::
   :toctree: generated

.. _2-Dates:

2 Dates
-------

**Definition**: Metadata schema block containing the start and end dates of the RAiD.

**Example JSON**

.. _2.1-dates.startDate:

2.1 dates.startDate
^^^^^^^^^^^^^^^^^^^

**Definition**: Project or activity start date.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: Only year is required, month and day are optional (but recommended when available).

.. _2.2-dates.endDate:

2.1 dates.endDate
^^^^^^^^^^^^^^^^^^^

**Definition**: Project or activity end date.

**Requirement**: Recommended

**Occurrence**: 1

**Allowed values**: ISO 8601 standard date

**Format**: ``YYYY-MM-DD``

**Examples**: ``2023-08-28``; ``2023-08``; ``2023``

**Note**: Only year is required, month and day are optional (but recommended when available). An end date should be supplied when a project concludes. Providing an end date terminates active management of and Registration Agency / Owner responsibility for a RAiD; once a RAiD has an end date, it is archival only.