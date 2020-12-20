.. _energy-module-advanced:

Shoebox Model
=============

The Shoebox model is based on the EnergyPlus "ZoneHVAC:IdealLoadsAirSystem" component. It models a core zone and a
perimeter zone. Mechanical Ventilation and Natural Ventilation are modelled using the
"DesignSpecification:OutdoorAir" and the "ZoneVentilation:WindandStackOpenArea" components.

End uses
________

End uses are reported using EnergyPlus Meters for each shoebox and multiplied by a weighting factor. A mapping of the
EnergyPlus meters to (=>) the UMI Results name are shown in the following table.

=====================================================  ======================
EnergyPlus Variable                                    UMI Output
=====================================================  ======================
Zone Lights Electric Energy                            SDL/Lighting
Zone Electric Equipment Electric Energy                SDL/Equipment
Zone Ideal Loads Supply Air Total Heating Energy       SDL/Heating
Zone Ideal Loads Supply Air Total Cooling Energy       SDL/Cooling
Water Use Equipment Heating Energy                     SDL/Domestic Hot Water
Zone Windows Total Transmitted Solar Radiation Energy  SDL/Window Radiation
=====================================================  ======================
