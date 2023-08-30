.. autosummary::
   :toctree: generated

.. _9-alternateUrls:

9 alternateUrls
===============

**Definition**: Metadata schema block containing alternative URLs for the project.

**Requirement**: Optional

**Occurrence**: 0-n

**Note**: RAiDs should avoid duplicating existing PIDs whenever possible.

**Example JSON**

.. _9.1-alternateUrls.url:

9.1 alternateUrls.url
---------------------

**Definition**: Links allowing visitors to the standardised landing page or user of the API export to access other URLs related to the project or activity.

**Requirement**: Mandatory for each alternateUrls supplied

**Occurrence**: 0-1

**Allowed values**: URL

**Example**: ``https://osf.io/puwgx/`` [Open Science Framework project page]