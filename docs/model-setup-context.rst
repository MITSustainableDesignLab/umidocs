
Model Setup - Context
=====================

In addition to the Rhino layer for buildings, a new umi project has a variety of other context layers for other objects relevant to various aspects of urban simulation. Each of these is a sublayer of the "Context" layer, which is in turn a sublayer of the "umi" layer, and is explained below.

1. Streets
----------

   The umi mobility analysis module relies upon the existance of a suitable street network for the site. This network should exist on the Rhino "Streets" layer. For details on setting it up, refer to the relevant section of the user guide.

2. Ground
---------

   The "Ground" layer contains user-specified, site-level ground objects. These objects are used to establish the site area for the purposes of calculating the site Floor Area Ratio (FAR). See :ref:`site-stats-far` for details.

3. Parks
--------

   Objects on the "Parks" layer can be used in mobility calculations. For details, see the relevant User Guide section.

4. Shading/Trees
----------------

   Objects on these layers are used for operational energy simulations. Objects on the "Shading" layer are used to calculate shadows cast on simulated buildings. This is used for shading objects that do not touch the buildings to be analyzed.

5. Boundary Objects
-------------------

   Boundary objects are similar to the shading objects. They are used for contextual shading. However, on these objects an adjacency test is performed in order to detect adjacencies and adiabatic surfaces. Boundary objects have to be closed breps.
