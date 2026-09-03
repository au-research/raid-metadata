Extended metadata schema properties
===================================

.. autosummary::
   :toctree: generated

Overview
--------

'Extended' metadata allows some customisation by Registration Agencies. All properties must be used without variation. Requirements, constraints, and format must be enforced. Controlled lists, however, may be modified, except where a specific property's own Constraints say otherwise; some Extended sub-properties, such as subject.keyword.language.id, remain closed to a single controlled list.

Registration agencies may:

1. Add existing controlled list schemas from other sources, so long as they are human- and machine-readable with a single page per value. 
2. Build new controlled list schemas, so long as they are human- and machine-readable with a single page per value. 

Note that not all existing schemes provide a URI for each term, in which case Registration Agencies will need to build and publish their own lists. 

All non-canonical schemas or controlled lists must be registered with the Registration Authority and published to a vocabulary service.

Contents
--------

.. toctree::

   subjects
   spatialCoverages
