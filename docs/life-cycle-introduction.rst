
Life Cycle
==========

Umi 2.0 introduces the first version of its Life Cycle (LC) module, which currently allows for the calculation of basic embodied environmental impacts associated with construction materials, such as :ref:`Embodied Energy <embodied-energy>` and :ref:`Embodied Carbon <embodied-carbon>`. The purpose of this introductory section is to identify the available metrics and calculations in the current version.

Purpose and metrics
-------------------

Given the contribution of the built environment to GHG emissions and fossil fuel consumption, the search for sustainability in its design mostly focus on the energy impacts of buildings happening due to their operation. However a holistic look to the energy and emissions impacts of buildings and cities needs to take into account those impacts happening in other phases of the life cycle of buildings such as, production, transport, maintenance and disposal of construction materials. These impacts also caused by the production of the urban built environment, although typically smaller than those coming from operation fuel consumption in the building lifetime, become more relevant in the design of high efficiency or net zero urban developments.

Typically these fuel and emission impacts associated with materials are added up in each life cycle phase through Life Cycle Assessment (LCA) methodologies to generate so called “embodied environmental impacts” of a building lifetime. In the current version of umi two embodied metrics are available:

- Embodied Energy (EE): It represents all fuel consumption (Typically from non-renewable sources) which happened through the lifetime of a product (or building), expressed as primary energy (kWh or MJ). The equivalent impact category in an impact assessment method such as `TRACI <https://www.epa.gov/chemical-research/tool-reduction-and-assessment-chemicals-and-other-environmental-impacts-traci>`__ (US EPA) would be Fossil Fuel Depletion. In umi, building results are expressed as kWh of primary energy.

- Embodied Carbon (EC): In a parallel manner to EE, it represents the GHG emissions through the lifetime of the product (or building). The term “embodied carbon” sometimes is used referring exclusively to CO2 emissions and measured in kgCO2, ignoring the effect of other greenhouse gases. In other cases it is used to referring to CO2 emissions equivalent and measured in kgCO2eq, being then an equivalent to the impact category of Global Warming Potential (GWP) in a method such as `TRACI <https://www.epa.gov/chemical-research/tool-reduction-and-assessment-chemicals-and-other-environmental-impacts-traci>`__. In umi, building results are expressed as kgCO2 only. However the results units depend only on the units of the properties introduced in the Template File Editor. If you prefer to use kgCO2eq introduce such values when defining materials and constructions.

Life Cycle calculation in umi
-----------------------------

The Life Cycle module in umi takes as inputs EE/EC data about materials and building massing, and performs a simplified Life Cycle Inventory calculation providing yearly results for both metrics, for the selected lifetime of the building. Note that it is not a complete LCA tool, such as other commercial more complex software suits focused on LCA modeling for products and materials, and it does not include a validated dataset for environmental properties of building components. The umi Life Cycle module focuses on the accounting of materials and geometrical components in a building, generating an approximate “Bill of materials” and allowing for the calculation and visualization of multiple buildings at a time. To know more about the methodology you can find `here <http://www.ibpsa.org/proceedings/BS2013/p_1351.pdf>`__ the conference paper from Building Simulation 2013 in which it was presented.

Depending of the boundaries considered in an LCA, EE and EC can be expressed as Cradle-to-Gate (Only considering production and manufacturing processes), Cradle-to-Site (Also including transportation to the site of use) and as Cradle-to-Grave (Including also use and disposal phases). In umi the three approaches are possible through the use of the following template data inputs:

   - Production EE/EC by kg of material

   - Transport EE/EC and average distances by kg of material

   - Assembly EE/EC by m\ :sup:`2`; of construction

   - Replacement/maintenance rate and yearly schedule

   - Disassembly EE/EC by m\ :sup:`2` of construction

In the calculation umi will use the amount of surfaces for each envelope assembly and estimate amount of interior elements such as floors, structure and partitions to generate results only for the lifecycle of materials. In future versions the Life Cycle module will allow for the automatic inclusion of operational primary energy and carbon in the use phase into the calculations. If you want to do a complete life cycle impacts calculation using the current version, you will have to take yearly results in energy consumption from the Operational Energy module and add them by year to the embodied impacts results. Note that in that case the energy load results generated by the Operational Energy module will have to be converted into primary energy or carbon emissions using the appropriate conversion factors for each fuel type.
