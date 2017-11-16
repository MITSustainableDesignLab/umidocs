
Life Cycle - Data Inputs
========================

Embodied energy and carbon calculations in umi are based on a set of environmental parameters defined in the Template Library File (TLF). The TLF does not only include life cycle data inputs, but many others used in different modules within umi. This user guide only focuses on describing in detail those data inputs required for the Life Cycle module, within Material, Construction, Structure and Building definitions. To know more about the TLF and its management through the Template File Editor you can go to the :ref:`template-editor` section of this user guide. In order to learn about the definition of thermal properties you can go to the :ref:`energy-module-overview` section of the user guide.

Life Cycle data in Opaque/Glazing Materials
```````````````````````````````````````````

All life cycle related inputs within Material components are located in the “Environmental” section. They characterize, for each opaque or glazing entry, the Production, Transport and Maintenance life cycle impacts in terms of Embodied Energy and Carbon.

.. figure:: ./assets/life-cycle-templateinput-d9f7gk68.png
   :scale: 100 %
   :align: center

The first section (1) has two fields: “Embodied Carbon” and “Embodied Energy”. These refer to the impacts in production and manufacture of a kg of the material in question, measured in a Cradle-to-Gate manner. The units selected are the most typical ones in existing databases: MJ/kg for primary energy and kgCO2/kg for carbon. A common and validated reference for these values is the `Inventory of Carbon and Energy (ICE) <http://www.ghgprotocol.org/Third-Party-Databases/Bath-ICE>`__ developed by the university of Bath.
