.. autosummary::
   :toctree: generated

.. _8-alternateIdentifier:

8 alternateIdentifier
=====================

**Definition**: a metadata schema block containing alternative local or global identifiers.

**Requirement**: optional

**Occurrence**: 0-n

**Note**: RAiDs should avoid duplicating existing PIDs whenever possible.

**Example JSON**

.. _8.1-alternateIdentifier.id:

8.1 alternateIdentifier.id
--------------------------

**Definition**: an identifier other than the primary identifier applied to the project or activity. This identifier may be any alphanumeric string that is unique within its domain of issue, for example a local identifier. The AlternateIdentifier represents an additional identifier for the same instance of the project or activity.

**Requirement**: mandatory for each alternateIdentifier supplied

**Occurrence**: 0-1

**Allowed values**: free text

**Example**: '123456ABC'

.. _8.2-alternateIdentifier.type:

8.2 alternateIdentifier.type
----------------------------

**Definition**: free text description of the type of alternateIdentifier supplied.

**Requirement**: mandatory for each alternateIdentifier.id supplied

**Occurrence**: 0-1

**Allowed values**: free text

**Example**: 'a local project ID in Elsevier Pure'