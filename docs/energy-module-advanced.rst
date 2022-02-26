.. _energy-module-advanced:

Shoebox Model
=============

The Shoebox model is based on the EnergyPlus "ZoneHVAC:IdealLoadsAirSystem" component. It models a core zone and a
perimeter zone. Mechanical Ventilation and Natural Ventilation are modelled using the
"DesignSpecification:OutdoorAir" and the "ZoneVentilation:WindandStackOpenArea" components.


Advanced settings under the Building tab
________________________________________

These settings adjust the parameters for the shoebox model used for the energy simulations. 

=======================  =====================  =================================================================================================================
Variable                 Default Value          Explanation
=======================  =====================  =================================================================================================================
Core depth (m)            3                     The depth of the shoebox core zone.
Room width (m)            3                     The width of the shoebox.
Perimeter offset (m)      3                     The depth of the shoebox perimeter zone.
envr                      0.1                   The external sensor spacing for the annual solar radiation incidence analysis that determines shoebox location.
fdist                     0.01                  The internal sensor spacing for the annual solar radiation incidence analysis that determines shoebox location.
=======================  =====================  =================================================================================================================

Larger values of envr and fdist reduce accuracy but speed up simulations, especially with large numbers of buildings. Radiation sensor generation and anlaysis tends to be the biggest bottleneck in running large models. However, modifying fdist and envr is not reccomended.

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


Accessing the Shoebox IDFs
__________________________

If you want to access the idfs created for each shoebox, go to c/umi/temp/energy after simulation. Under two filename subdirectories, open the eplus folder. From there you will find "group#" folders, with as many groups as there are templates. Each group has a number of sample folders under it. The samples are based on the number of shoeboxes required by the radiation mapping. You can navigate to an individual sample and open up the .idf file from there and simulate in the standard EP-launch. If you want to process the resulting data, you can use the command “UmiExportShoeboxWeights” in the Rhino command line. This command creates a .json file that maps each shoebox file back to the original model. The weights can be used to extrapolate the individual idf results out to the full model results if repeated across all samples and groups. 
