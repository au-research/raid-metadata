Core Metadata Schema Properties
=============================

.. autosummary::
   :toctree: generated

.. _1-Identifier:


1 Identifier block
------------------

*All metadata properties are divided into blocks. Each block contains related properties.*

1.1 Identifier.id
^^^^^^^^^^^^^^^^^

Definition: **A unique string that identifies a Research Activity Identifier (RAiD); RAiD name**

Occurence: **1**

Requirement: **Mandatory**

Schema-block: **Core-v1**

Allowed values: 

*A RAiD name registered by a RAiD Registration Agency*

Format: ``https://raid.org/prefix/suffix``

Contraints: RAiD name suffix must consist of alphanumeric, English, ASCII Latin characters

.. _1a-identifierSchemeURI:

1.1a identifier.SchemeURI
~~~~~~~~~~~~~~~~~~~~~~~~~

Definition: **The URI of the Identifier scheme used**

Occurence: **1**

Requirement: **Mandatory**

Schema-block: **Core-v1**

Allowed values: 

* <https://raid.org/> 

Note: This property declares that the Identifier is a RAiD, resolvable at <https://raid.org/>.
