Core Metadata Schema Properties
===============================

.. autosummary::
   :toctree: generated

.. _1-Identifier:


1 Identifier block
------------------

1.1 identifier.id
^^^^^^^^^^^^^^^^^

**Definition**: A unique string that identifies a Research Activity Identifier (RAiD); RAiD name

**Requirement**: Mandatory

**Occurence**: 1

**Allowed values**: A RAiD name registered by a RAiD Registration Agency expressed as an actionable URL

**Format**: ``https://raid.org/prefix/suffix``

**Example**: ``https://raid.org/10.12345/abc123``

**Contraints**: RAiD name prefix supplied by the DOI Foundation; RAiD name suffix consisting of alphanumeric, English, ASCII Latin characters

**Note**: RAiD names are valid DOIs and can also be resolved at https://doi.org/.

.. _1.1-identifierSchemeURI:

1.1a identifier.SchemeURI
~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the Identifier scheme used

**Requirement**: Mandatory

**Occurence**: 1

**Allowed values**: *Controlled list*

* ``https://raid.org/``

**Note**: This property declares that the Identifier is a RAiD, resolvable at https://raid.org/.
