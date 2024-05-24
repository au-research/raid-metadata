.. autosummary::
   :toctree: generated

.. _13-spatialCoverage:

13 spatialCoverage
==================

**Definition**: metadata schema block containing information about any spatial region(s) or named place(s) targeted by the project

**Requirement**: optional

**Occurrence**: 0-n

**Example JSON**

.. _13.1-spatialCoverage.id:

13.1 spatialCoverage.id
-----------------------

**Definition**: spatial region or named place that is the subject or target of the project or activity. Repeat this property as necessary to indicate different locations. Do not duplicate organisational locations

**Requirement**: mandatory for each spatialCoverage supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list of URIs derived from the schema chosen at spatialCoverage.id.schemaUri*

**Examples**

* ``https://nominatim.openstreetmap.org/ui/details.html?osmtype=R&osmid=1947835&class=boundary`` (Tundzha, Bulgaria, from OpenStreetMap)
* ``https://nominatim.openstreetmap.org/ui/details.html?osmtype=R&osmid=186382&class=boundary`` (Bulgaria, from OpenStreetMap)
* ``https://nominatim.openstreetmap.org/ui/details.html?osmtype=W&osmid=26707240&class=historic`` (Pompeii, Italy, OpenStreetMap)
* ``https://www.geonames.org/264371/athens.html`` (Athens, Greece, from Geonames)
* ``https://www.geonames.org/2161776/katoomba.html`` (Katoomba, NSW, Australia, from Geonames)

.. _13.2-spatialCoverage.schemaUri:

13.2 spatialCoverage.schemaUri
------------------------------

**Definition**: the URI of the geolocation schema used for spatialCoverage

**Requirement**: mandatory for each spatialCoverage supplied

**Occurrence**: 1

**Allowed values**: *open controlled list of URIs defined at https://vocabulary.raid.org/spatialCoverage.schemaUri/167*

* ``https://nominatim.openstreetmap.org/`` (OpenStreetMap )
* ``https://www.geonames.org/`` (Geonames)

**Note**: OpenStreetMap preferred, Geonames allowed; other geoname servers can be nominated by Registration Agencies.

.. _13.3-spatialCoverage.place:

13.3 spatialCoverage.place
--------------------------

**Definition**: metadata schema sub-block containing free-text place names or descriptions plus associated metadata properties

**Requirement**: optional

**Occurrence**: 0-n

.. _13.3.1-spatialCoverage.place.text:

13.3.1 spatialCoverage.place.text
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: free text description of one or more geographic locations that are the subject or target of the project or activity; use to specify or describe a geographic location in a manner not covered by spatialCoverage.id

**Requirement**: optional

**Occurrence**: 0-n

**Allowed values**: free text

**Constraints**: do not duplicate information from spatialCoverage.id above; do not use for organisational locations (which are derived from the organisation's ROR)

.. _13.3.2-spatialCoverage.place.language:

13.3.2 spatialCoverage.place.language
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: metadata schema block declaring the language of spatialCoverage.place.text

**Requirement**: recommended for each spatialCoverage.place.text provided

**Occurrence**: 0-1

**Example JSON**

.. _13.3.2.1-spatialCoverage.place.language.id:

13.3.2.1 spatialCoverage.place.language.id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: language used for spatialCoverage.place.text identified by a code or other identifier

**Requirement**: mandatory for each subject.place.language supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list derived from spatialCoverage.place.language.schemaUri*

**Example**: ``eng``

.. _13.2.2.2-spatialCoverage.place.language.schemaUri:

13.2.2.2 spatialCoverage.place.language.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: the URI of the language identifier schema

**Requirement**: mandatory for each subject.place.language supplied

**Occurrence**: 1

**Allowed values**: *closed controlled list of allowed language schemas defined at https://vocabulary.raid.org/spatialCoverage.place.language.schemaUri/206*

* ``https://www.iso.org/standard/74575.html`` (ISO 639:2023 Code for individual languages and language groups (Set 3))

**Constraints**: currently limited to ISO 639:2023 (Set 3)