.. autosummary::
   :toctree: generated

.. _8-alternateIdentifier:

8 alternateIdentifier
=====================

**Definition**: Metadata schema block containing alternative local or global identifiers.

**Requirement**: Optional

**Occurrence**: 0-n

**Note**: RAiDs should avoid duplicating existing PIDs whenever possible.

**Example JSON**

.. _8.1-alternateIdentifier.id:

8.1 alternateIdentifier.id
--------------------------

**Definition**: An identifier other than the primary Identifier applied to the Project. This identifier may be any alphanumeric string that is unique within its domain of issue, for example a local identifier. The AlternateIdentifier represents an additional identifier for the same instance of the Project or Activity.

**Requirement**: Mandatory for each alternateIdentifier supplied

**Occurrence**: 0-1

**Allowed values**: Free text

**Example**: '123456ABC'

.. _8.2-alternateIdentifier.type:

8.2 alternateIdentifier.type
----------------------------

**Definition**: Free text description of the type of alternateIdentifier supplied.

**Requirement**: Mandatory for each alternateIdentifier.id supplied

**Occurrence**: 0-1

**Allowed values**: Free text

**Example**: 'A local project ID in Elsevier Pure'