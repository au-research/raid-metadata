.. autosummary::
   :toctree: generated

.. _1-Identifier:

1 Identifier
------------

**Definition**: Metadata schema block containing the RAiD name (identifier.id) and associated properties.

**Example JSON**

.. _1.1-identifier.id:

1.1 identifier.id
^^^^^^^^^^^^^^^^^

**Definition**: A unique string that identifies a Research Activity Identifier (RAiD); RAiD name.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: A RAiD name registered by a RAiD Registration Agency expressed as an actionable URL.

**Format**: ``https://raid.org/prefix/suffix``

**Example**: ``https://raid.org/10.12345/abc123``

**Constraints**: RAiD name prefix supplied by the DOI Foundation; RAiD name suffix consisting of alphanumeric, English, ASCII Latin characters

**Note**: RAiD names are valid DOIs and can also be resolved at https://doi.org/ or https://handle.net/.

.. _1.1.1-identifier.id.schemaURI:

1.1.1 identifier.id.schemaURI
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the Identifier scheme used to identify RAiDs.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Controlled list*

* ``https://raid.org/``

**Note**: This property declares that the Identifier is a RAiD, declaring it resolvable at https://raid.org/; this property is set as a default in all installations of the RAiD Service software.

.. _1.2-identifier.registrationAgencyId:

1.2 identifier.registrationAgencyId
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The Research Organization Registry (ROR) of the RAiD Registration Agency that minted the RAiD.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Controlled list*

* ``https://ror.org/038sjwq14`` [The Australian Research Data Commons]
* ``https://ror.org/009vhk114`` [SURF]

**Note**: Registration Agencies must have, acquire, or be assigned RORs. The Registration Agency identifier must be set as a default in each installation of the RAiD Service software. The Registration Authority maintains the list of Registration Agencies.

.. _1.2.1-identifier.registrationAgencyId.schemaURI:

1.2.1 identifier.registrationAgencyId.schemaURI
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the Identifier scheme used to identify RAiD Registration Agencies.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Controlled list*

* ``https://ror.org/``

**Note**: This property is set as a default in all installations of the RAiD Service software.

.. _1.3-identifier.owner:

1.3 identifier.owner
^^^^^^^^^^^^^^^^^^^^

**Definition**: The Research Organization Registry (ROR) of the legal entity responsible for the RAiD; the ‘Owner’ of a RAiD. Analogous to a DataCite 'Member', the Owner has a legal agreement with its Registration Agency.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Controlled list of Owners maintained by each Registration Agency*

**Example values**:

* ``https://ror.org/00rqy9422`` [University of Queensland]
* ``https://ror.org/02stey378`` [University of Notre Dame Austraila]
* ``https://ror.org/03pnv4752`` [Queensland University of Technology]

**Note**: Owners, i.e., Organisations hosting Service Points, must have, acquire, or be assigned RORs. A RAiD minted by a Registration Agency must be associated with an Owner affiliated with that Agency.

.. _1.3.1-identifier.owner.schemaURI:

1.3.1 identifier.owner.schemaURI
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the Identifier scheme used to identify RAiD Owners.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Controlled list*

* ``https://ror.org/``

**Note**: This property is set as a default in all installations of the RAiD Service software.

.. _1.4-identifier.servicePoint:

1.4 identifier.servicePoint
^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The Service Point (SP) that requested the RAiD. Analogous to a DataCite ‘Repository’. RAiD Owners can have multiple SPs, and SPs do not need to be legal entities.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Controlled list of Service Points maintained by each Registration Agency*

**Examples**:

* Queensland University of Technology - Research Infrastructure
* RDM@UQ
* UQ Centre for Advanced Imaging
* The University of Notre Dame Australia

**Note**: A RAiD minted by a Registration Agency must have a SP associated with an Owner affiliated with that Agency.

.. _1.5-identifier.license:

1.5 identifier.license
^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The licence under which the RAiD Metadata Record associated with this Identifier has been issued.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: *Controlled list*

* Creative Commons CC-0

**Note**: All RAiD metadata is available on a 'no rights reserved' basis. 

.. _1.6-identifier.version:

1.6 identifier.version
^^^^^^^^^^^^^^^^^^^^^^

**Definition**: The version number of the RAiD.

**Requirement**: Mandatory

**Occurrence**: 1

**Allowed values**: Auto-incrementing integer

**Note**: The RAiD version number is set automatically by the RAiD Service software as a RAiD is updated. 
