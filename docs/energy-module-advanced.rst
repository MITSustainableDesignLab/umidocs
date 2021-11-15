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

Deep Dive
________
If you want to access the idfs created for each shoebox, go to c/umi/temp/energy after simulation. Under two filename subdirectories, open the eplus folder. From there you will find "group#" folders, with as many groups as there are templates. Each group has a number of sample folders under it. The samples are based on the number of shoeboxes required by the radiation mapping. You can navigate to an individual sample and open up the .idf file from there and simulate in the standard EP-launch. If you want to process the resulting data, you can use the command “UmiExportShoeboxWeights” in the Rhino command line. This command creates a .json file that maps each shoebox file back to the original model. The weights can be used to extrapolate the individual idf results out to the full model results if repeated across all samples and groups. 
