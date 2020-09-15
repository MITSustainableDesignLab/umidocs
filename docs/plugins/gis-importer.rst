.. _gis-importer:

UMI GIS Importer
================

.. admonition:: Authorship

   9/15/20 `Zach Berzolla <https://www.researchgate.net/profile/Zach_Berzolla>`_ (MIT).

Function
--------

Takes the input non-geometric data from the configuration file and the geometry from the shapefile or CityGML file and
joins them to create UMI buildings for simulation.

Inputs
------

- An UMI project with appropriate weather file (.epw) and template library loaded
- A configuration file, as specified in UBEM.IO document
- A shapefile or CityGML file, cleaned so that each building has a unique ID

Shapefiles
..........

There are often multiple polylines that outline a single building in shapefiles. These polylines are joined together to
create a single base plane. The program checks to ensure these planes are closed and planar. When there are fully
enclosed courtyards in a building shapefile (e.g. all four sides are contained within the outer footprint of the
building, sometimes called a void), the courtyard polyline is subtracted from the footprint polyline so that the
courtyard is excluded. This is then turned into a single base plane. In either case, the base plane is extruded to the
height provided by the configuration file, creating 2.5D geometry. This geometry is then combined with the appropriate
information from the configuration file and assigned to an UMI building and imported into Rhino.


CityGML
.......

CityGML data is provided in 2.5D (LoD1) or 3D (LoD2). In both cases, the data includes points for all corners of the
geometry so the full volume can be created directly, no extrusion necessary. There are slight nuances in the format of
points for LoD1 and LoD2 files, but otherwise the structure is the same. A height value is also provided; this is used
for calculation of the floor-to-floor height for UMI. Once the points from the CityGML file have been read in, polyline
curves are created to form planes for each surface of the geometry. If these planes are closed and planar, they are
joined together to create closed BREPs. The BREPs are then joined with the appropriate information from the
configuration file and imported into UMI as an UMI building or shading object. Errors most often occur when complicated
geometry such as towers are modeled as they are often non-planar, however this is a data error and should not be in the
original file.

Outputs
-------

UMI buildings and shading objects from the input data, complete with template field, window-to-wall ratio,
floor-to-floor height, and any other relevant information.