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

**Definition**: An identifier other than the primary Identifier applied to the Project. This identifier may be any alphanumeric string that is unique within its domain of issue. May be used for local identifiers. The AlternateIdentifier should be an additional identifier for the same instance of the Project or Activity.

**Requirement**: Mandatory for each alternateIdentifiers supplied

**Occurrence**: 0-1

**Allowed values**: Free text

**Example**: '123456ABC'

.. _8.1.1-alternateIdentifiers.id.type:

8.1.1 alternateIdentifiers.id.type
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The type of alternateIdentifiers supplied.

**Requirement**: Mandatory for each alternateIdentifiers.id supplied

**Occurrence**: 0-1

**Allowed values**: Free text

**Example**: 'A local project ID in Elsevier Pure'