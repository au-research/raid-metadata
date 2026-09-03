.. autosummary::
   :toctree: generated

.. _9-alternateIdentifier:

9 alternateIdentifier
=====================

**Definition**: a metadata schema block containing alternative local or global identifiers for the project or activity associated with the RAiD

**Requirement**: optional

**Occurrence**: 0-n

**Example JSON**

.. code-block:: json

   {
     "alternateIdentifier": [
       {
         "id": "UTAS-IMAS-2024-0412",
         "type": "Institutional research management system project ID"
       }
     ]
   }

.. _9.1-alternateIdentifier.id:

9.1 alternateIdentifier.id
--------------------------

**Definition**: an identifier other than the RAiD applied to the project or activity

**Requirement**: mandatory for each alternateIdentifier supplied

**Occurrence**: 1

**Allowed values**: free text

**Example(s)**: '123456ABC'

**Note**: An alternateIdentifer.id may be any alphanumeric string that is unique within its domain of issue, for example a local identifier unique to an organisation. The alternateIdentifier.id represents an additional identifier for the same instance of the project or activity; its referent is identical to that of the RAiD.

.. _9.2-alternateIdentifier.type:

9.2 alternateIdentifier.type
----------------------------

**Definition**: free text description of the type of alternateIdentifier supplied

**Requirement**: mandatory for each alternateIdentifier supplied

**Occurrence**: 1

**Allowed values**: free text

**Example(s)**: 'A local project ID in the university CRIS'
