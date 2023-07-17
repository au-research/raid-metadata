Research Activity Identifier (RAiD) Metadata Schema
===================================================

A *Research Activity Identifier* (RAiD) is a globally unique, persistent identifier (PID) for research projects or activities. It consists of a unique identifier (a handle) and a metadata envelope. The metadata envelope links various components (e.g., contributors, organisations, grants, instruments, publications, datasets, etc.) to the project, via their own PIDs where available (e.g., ORCiDs, RORs, Crossref Grant IDs, DOIs, etc.). These components are only linked to the project itself; a RAiD does not assert links between components (e.g., contributors to organisations). RAiDs also contain project information not found elsewhere, such as project title, start date, description, and subject, but does not duplicate information found elsewhere. RAiDs can also be linked to one another using arbitrary qualified relationships so that, e.g., subprojects can be created. 

.. note::

   This project is under active development.

Contents
--------

.. toctree::

   core
   extended
