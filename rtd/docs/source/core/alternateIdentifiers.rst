.. autosummary::
   :toctree: generated

.. _8-alternateIdentifiers:

8 alternateIdentifiers
======================

**Definition**: Metadata schema block containing alternative local or global identifiers.

**Requirement**: Optional

**Occurrence**: 0-n

**Note**: RAiDs should avoid duplicating existing PIDs whenever possible.

**Example JSON**

.. _8.1-alternateIdentifiers.id:

8.1 alternateIdentifiers.id
---------------------------

**Definition**: An identifier other than the primary Identifier applied to the Project. This identifier may be any alphanumeric string that is unique within its domain of issue, for example a local identifier. The AlternateIdentifier represents an additional identifier for the same instance of the Project or Activity.

**Requirement**: Mandatory for each alternateIdentifiers supplied

**Occurrence**: 0-1

**Allowed values**: Free text

**Example**: '123456ABC'

.. _8.2-alternateIdentifiers.type:

8.2 alternateIdentifiers.type
-----------------------------

**Definition**: Free text description of the type of alternateIdentifiers supplied.

**Requirement**: Mandatory for each alternateIdentifiers.id supplied

**Occurrence**: 0-1

**Allowed values**: Free text

**Example**: 'A local project ID in Elsevier Pure'