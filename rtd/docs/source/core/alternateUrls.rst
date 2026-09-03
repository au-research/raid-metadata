.. autosummary::
   :toctree: generated

.. _10-alternateUrl:

10 alternateUrl
===============

**Definition**: a metadata schema block containing alternative URLs for the project

**Requirement**: optional

**Occurrence**: 0-n

**Example JSON**

.. code-block:: json

   {
     "alternateUrl": [
       {
         "url": "https://imas.utas.edu.au/projects/kelpwatch"
       }
     ]
   }

.. _10.1-alternateUrl.url:

10.1 alternateUrl.url
---------------------

**Definition**: a link to another website related to the project or activity

**Requirement**: mandatory for each alternateUrl supplied

**Occurrence**: 1

**Allowed values**: URL

**Note**: An alternateURL can be used to point to any other project website, whether standalone, organisational, or in a platform such as Open Science Framework.

**Example(s)**: ``https://osf.io/puwgx/`` (an Open Science Framework project page)
