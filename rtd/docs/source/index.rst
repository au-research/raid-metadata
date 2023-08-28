Research Activity Identifier (RAiD) Metadata Schema
===================================================

A *Research Activity Identifier* (RAiD) is a globally unique, persistent identifier (PID) for research projects or activities. It consists of a unique identifier (a handle) and a metadata envelope. The metadata envelope links various components (e.g., contributors, organisations, grants, instruments, publications, datasets, etc.) to the project, via their own PIDs where available (e.g., ORCiDs, RORs, Crossref Grant IDs, DOIs, etc.). These components are only linked to the project itself; a RAiD does not assert links between components (e.g., contributors to organisations). RAiDs also contain project information not found elsewhere, such as project title, start date, description, and subject, but does not duplicate information found elsewhere. RAiDs can also be linked to one another using arbitrary qualified relationships so that, e.g., subprojects can be created. 

Conventions
-----------

Blocks
^^^^^^

All metadata properties are divided into blocks. Each block contains related properties. 

Property descriptions
^^^^^^^^^^^^^^^^^^^^^

Each property description has a number of elements:

**Definition** briefly defines the property

**Requirement** indicates whether a property is mandatory, recommended, or optional

**Occurance** indicates the number of times a property may occur:

* 0 represents a recommended or optional property that may only occur once
* 0-n represents an optional propterty that may occur multiple times
* 1 represents a required property that may only occur once
* 1-n represents a required propterty that may occur multiple times

**Allowed values** will either indicate a controlled list of values limiting input (as a bulleted list), or rules governing the values (as an italicised statement followed by format and contraints).

**Note** any additional information about the property.


.. note::

   This project is under active development.

Contents
--------

.. toctree::

   core
      identifier
      dates
   extended
