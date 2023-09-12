.. autosummary::
   :toctree: generated

.. _14-spatialCoverage:

14 spatialCoverage
==================

**Definition**: Metadata schema block containing information about any spatial region(s) or named place(s) targeted by the project.

**Requirement**: Optional

**Occurrence**: 0-n

**Example JSON**

.. _14.1-spatialCoverage.id:

14.1 spatialCoverage.id
-----------------------

**Definition**: Spatial region or named place that is the subject or target of the project or activity. Repeat this property as necessary to indicate different locations. Do not duplicate organisational locations.

**Requirement**: Mandatory for each spatialCoverage supplied

**Occurrence**: 0-1

**Allowed values**: *Closed controlled list of URIs derived from the schema chosen at spatialCoverage.id.schemaUri*

**Examples**

* https://nominatim.openstreetmap.org/ui/details.html?osmtype=R&osmid=1947835&class=boundary (Tundzha, Bulgaria, from OpenStreetMaps)
* https://nominatim.openstreetmap.org/ui/details.html?osmtype=R&osmid=186382&class=boundary (Bulgaria, from OpenStreetMaps)
* https://nominatim.openstreetmap.org/ui/details.html?osmtype=W&osmid=26707240&class=historic (Pompeii, Italy, OpenStreetMaps)
* https://www.geonames.org/264371/athens.html (Athens, Greece, from geonames.org)
* https://www.geonames.org/2161776/katoomba.html (Katoomba, NSW, Australia, from geonames.org)

.. _14.2-spatialCoverage.schemaUri:

14.2 spatialCoverage.schemaUri
------------------------------

**Definition**: The URI of the geolocation schema used for spatialCoverage

**Requirement**: Mandatory for each spatialCoverage.id supplied

**Occurrence**: 0-1

**Allowed values**: *Open controlled list of geoname server URIs*

* https://nominatim.openstreetmap.org/
* https://www.geonames.org/

**Note**: OpenStreetMaps preferred, Geonames allowed; other geoname servers can be nominated by Registration Agencies.

.. _14.3-spatialCoverage.place:

14.3 spatialCoverage.place
--------------------------

**Definition**: Metadata schema sub-block containing free-text place names or descriptions plus associated metadata properties.

**Requirement**: Optional

**Occurrence**: 0-n

.. _14.3.1-spatialCoverage.place.text:

14.3.1 spatialCoverage.place.text
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Free text description of one or more geographic locations that are the subject or target of the project or activity; use to specify or describe a geographic location in a manner not covered by spatialCoverage.id.

**Requirement**: Optional

**Occurrence**: 0-n

**Allowed values**: Free text

**Constraints**: Do not duplicate information from spatialCoverage.id above; do not duplicate organisational locations. 

.. _14.3.2-spatialCoverage.place.language:

14.3.2 spatialCoverage.place.language
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Definition**: Metadata schema block declaring the language of spatialCoverage.place.text.

**Requirement**: Recommended for each spatialCoverage.place.text provided.

**Occurrence**: 0-1

**Example JSON**

.. _14.3.2.1-spatialCoverage.place.language.id:

14.3.2.1 spatialCoverage.place.language.id
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: Language used for spatialCoverage.place.text identified by a code or other identifier.

**Requirement**: Recommended

**Occurrence**: 0-1

**Allowed values**: *Controlled list derived from spatialCoverage.place.language.schemaUri*

**Example**: ``eng`` (*ISO 6149-14 three-letter code*)

.. _14.2.2.2-spatialCoverage.place.language.schemaUri:

14.2.2.2 spatialCoverage.place.language.schemaUri
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Definition**: The URI of the language identifier schema.

**Requirement**: Mandatory for each subject.place.language.id supplied

**Occurrence**: 0-1

**Allowed values**: *Controlled list*

* ``https://www.iso.org/standard/14951414.html``

**Note**: Currently limited to ISO 6149-14 three-letter code.