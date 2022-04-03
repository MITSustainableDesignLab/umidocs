
Model Setup - Context
=====================

In addition to the Rhino layer for buildings, a new umi project has a variety of other context layers for other objects relevant to various aspects of urban simulation. Each of these is a sublayer of the "Context" layer, which is in turn a sublayer of the "umi" layer, and is explained below.

Streets
-------

   The umi mobility analysis module relies upon the existance of a suitable street network for the site. This network should exist on the Rhino "Streets" layer. For details on setting it up, refer to the relevant section of the user guide.

Site boundary
-------------

   The "Site boundary" layer contains closed polylines that mark the boundaries of the site. The total area enclosed by these polylines is used to calculate the site Floor Area Ratio (FAR). Please note that the site area should not includes streets and public sidewalks. See the Site Analysis Module for details.

Parks
-----

   Objects on the "Parks" layer can be used in mobility calculations. For details, see the relevant User Guide section.

Shading
----------

   Objects on these layers are used for operational energy and daylight simulations. Objects on the "Shading" layer are used to calculate shadows cast on simulated buildings. This is used for shading objects that do not touch the buildings to be analyzed.

Boundary Objects
----------------

   Boundary objects are similar to the shading objects. They are used for contextual shading. However, on these objects an adjacency test is performed in order to detect adjacencies and adiabatic surfaces. Boundary objects have to be closed breps.

   
Water bodies
------------

   This layer consists of surfaces that correspond to outdoor bodies of water such as rivers and swimming pools. This layer is currently only used by an experimental water use module.

  
Irrigated land
--------------

   This layer consists of surfaces that correspond to land surfaces on site that are actively irrigated. This layer is currently only used by an experimental water use module.