.. autosummary::
   :toctree: generated

.. _1-identifier:

1 identifier
============

**Definition**: a metadata schema block containing the RAiD name (identifier.id) and associated properties

**Requirement**: mandatory

**Occurrence**: 1

**Example JSON**

.. _1.1-identifier.id:

1.1 identifier.id
-----------------

**Definition**: a unique alphanumeric character string that identifies a Research Activity Identifier (RAiD); RAiD name

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: the RAiD name registered by a RAiD Registration Agency, expressed as an actionable URL

**Format**: ``https://raid.org/prefix/suffix``

**Constraints**: RAiD name prefix supplied by the DOI Foundation; RAiD name suffix consisting of alphanumeric, English, ASCII Latin characters

**Example**: ``https://raid.org/10.12345/abc123``

**Note**: RAiD names are valid DOIs and can also be resolved via https://doi.org/ or https://handle.net/.

.. _1.2-identifier.id.schemaUri:

1.2 identifier.schemaUri
------------------------

**Definition**: the URI of the identifier scheme used to identify RAiDs.

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: *closed controlled list*

* ``https://raid.org/``

**Note**: this property declares that the identifier is a RAiD and resolvable at https://raid.org/.

.. _1.3-identifier.registrationAgency:

1.3 identifier.registrationAgency
---------------------------------

**Definition**: metadata schema sub-block declaring the Registration Agency that minted the RAiD.

**Requirement**: mandatory

**Occurrence**: 1

.. _1.3.1-identifier.registrationAgencyId:

1.3.1 identifier.registrationAgency.id
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the Research Organization Registry (ROR) of the RAiD Registration Agency that minted the RAiD.

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from identifier.registrationAgency.schemaUri*

* ``https://ror.org/038sjwq14`` [The Australian Research Data Commons]
* ``https://ror.org/009vhk114`` [SURF]

**Constraints**: Always set by default to the ROR of the RAiD Registration Agency minting the identifier

**Note**: Registration Agencies must have, acquire, or be assigned RORs; the RAiD Registration Authority maintains the list of Registration Agencies.

.. _1.3.2-identifier.registrationAgencyId.schemaUri:

1.3.2 identifier.registrationAgency.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the identifier scheme that is used to identify RAiD Registration Agencies

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: *closed controlled list*

* ``https://ror.org/``

.. _1.4-identifier.owner:

1.4 identifier.owner
--------------------

**Definition**: a metadata schema sub-block that declares the owner of the RAiD (i.e. the organisation requesting the RAiD).

**Requirement**: mandatory

**Occurrence**: 1

.. _1.4.1-identifier.owner.id:

1.4.1 identifier.owner.id
^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the ROR of the legal entity responsible for the RAiD (i.e. the 'owner' of a RAiD); analogous to a DataCite 'Member', an owner has a legal agreement with their Registration Agency

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: *open controlled list of owners maintained by each Registration Agency, utilising the schema declared at identifier.owner.schemaUri*

**Example values**:

* ``https://ror.org/00rqy9422`` [University of Queensland]
* ``https://ror.org/02stey378`` [University of Notre Dame Australia]
* ``https://ror.org/03pnv4752`` [Queensland University of Technology]

**Constraints**: Always set by default to the organisation requesting the RAiD

**Note**: owners, i.e., Organisations hosting Service Points, must have, acquire, or be assigned RORs; a RAiD minted by a Registration Agency must be associated with an Owner affiliated with that Agency; Registration Agencies must register lists of their Owerns with the RAiD Registration Authority regularly.

.. _1.4.2-identifier.owner.schemaUri:

1.4.2 identifier.owner.schemaUri
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the URI of the identifier scheme that is used to identify RAiD owners

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: *controlled list*

* ``https://ror.org/``

.. _1.4.3-identifier.owner.servicePoint:

1.4.3 identifier.owner.servicePoint
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: the service point (SP) that requested the RAiD. Analogous to a DataCite 'repository'. SPs belong to an owner, RAiD owners can have multiple SPs; yet SPs do not need to be legal entities 

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: *open controlled list of SPs maintained by each Registration Agency*

**Examples**:

* Queensland University of Technology - Research Infrastructure
* RDM@UQ
* UQ Centre for Advanced Imaging
* The University of Notre Dame Australia

**Constraints**: Always set to the SP requesting the RAiD

**Note**: a RAiD minted by a Registration Agency must have a SP associated with an Owner affiliated with that Agency; Registration Agencies must register lists of their Service Points with the RAiD Registration Authority regularly.

.. _1.5-identifier.license:

1.5 identifier.license
----------------------

**Definition**: the licence, or licence waiver, under which the RAiD metadata record associated with this Identifier has been issued.

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: *closed controlled list*

* Creative Commons CC-0

**Note**: all RAiD metadata is available on a 'no rights reserved' basis. 

.. _1.6-identifier.version:

1.6 identifier.version
----------------------

**Definition**: the version number of the RAiD

**Requirement**: mandatory

**Occurrence**: 1

**Allowed values**: system-supplied, auto-incrementing integer

**Default**: The RAiD version number is set automatically by the RAiD Service software when a RAiD is updated. 