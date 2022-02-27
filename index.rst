
===================================
Welcome to umi Online Documentation
===================================

The Urban Modeling Interface (umi) is a multi-year effort, led by the  `Sustainable Design Lab`_  at MIT, to develop an urban modeling platform to evaluate the environmental performance of neighborhoods and cities with respect to operational and embodied energy use, neighborhood walkability, access to daylighting, 
urban food production and district-level energy supply analysis. umi is a design environment for Rhinoceros 3d (Rhino) and includes an application programming interface (API) for researchers and consultants interested in adding additional performance modules and metrics. 
Focus users are urban designers and planners, municipalities, utilities, sustainability consultants and other urban stakeholders. umi files can be generated form scratch in Rhino or via the `UBEM.io`_ web app. UBEM.io also supports the results comparison of multiple umi files.


.. _Sustainable Design Lab:  https://web.mit.edu/sustainabledesignlab/index.html
.. _UBEM.io: http://www.ubem.io/



.. toctree::
   :maxdepth: 3
   :caption: Getting Started

   Requirements <docs/first.md>
   Installation <docs/installation.rst>
   Learn umi <docs/examples/_tutorials.rst>
   
   
.. toctree::
   :maxdepth: 3
   :caption: Model Setup

   docs/starting_an_umi_project.rst
   docs/site-config.rst
   docs/saving-project.rst
   Model Setup - Buildings <docs/model-setup-buildings.rst>
   Template Editor <docs/model-setup-template.rst>
   Context <docs/model-setup-context.rst>

.. toctree::
   :maxdepth: 3
   :caption: Site Analysis Module 

   Floor-Area Ratio <docs/site-stats-far.rst>

   
.. toctree::
   :maxdepth: 3
   :caption: Operational Energy Module

   Overview <docs/energy-module-overview.rst>
   docs/energy-module-advanced.rst

.. toctree::
   :maxdepth: 3
   :caption: Embodied Energy Module

   Life Cycle Introduction <docs/life-cycle-introduction.rst>
   Template Input <docs/life-cycle-templateinput.rst>
   docs/life-cycle-simulation-visualization.rst

   
.. toctree::
   :maxdepth: 3
   :caption: District Energy Module   

   docs/plugins/district-energy.rst
   
.. toctree::
   :maxdepth: 3
   :caption: Urban Agriculture Module   

   docs/plugins/harvest.rst
   

.. toctree::
   :maxdepth: 3
   :caption: Design Accessibility (Walk/Bike)

   docs/design-access-intro.rst
   docs/design-access-setup-model.rst
   docs/design-access-example.rst
 
   
.. toctree::
   :maxdepth: 3
   :caption: Template Editor

   docs/template-info/_template-detail.rst
   docs/template-info/Materials/_materials.rst
   docs/template-info/Constructions/_constructions.rst
   docs/template-info/Schedules/_schedules.rst
   docs/template-info/Zone-Information/_zoneinfo.rst
   docs/template-info/Building-Templates/_bldgtemplates.rst




------------------
Indices and tables
------------------

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
