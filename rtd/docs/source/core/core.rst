Core Metadata Schema Properties
===============================

.. autosummary::
   :toctree: generated

Overview
--------

'Core' metadata is shared across Registration Agencies. All properties must be used without variation. Requirements, constraints, and format must be enforced. Controlled lists must either be used without changes or, if they are modified or a different list chosen, a crosswalk must be provided to the canonical values. If a Registration Agency modifies a controlled list, the web application and API should return both the local and canonical values. Any modified controlled lists must be published using a vocabulary service. Modifications must be reported to and approved by the Registration Authority.

Contents
--------

.. toctree::

   identifier
   dates
   titles
   descriptions
   contributors
   organisations
   relatedObjects
   alternateIdentifiers
   alternateUrls
   relatedRaids
   access


