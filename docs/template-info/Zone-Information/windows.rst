
Windows
=======

.. csv-table::
   :file: ../../tables/windows.csv
   :header-rows: 1
   :widths: 20,50,15,15

.. index:: Type
.. _windows_type:

Type
````

.. index:: Construction
.. _windows_construction:

Construction
````````````

.. index:: Operable area
.. _windows_operable_area:

Operable area
`````````````

.. index:: Shading is used
.. _windows_shading_used:

Shading is used
```````````````

.. index:: Shading system availability schedule
.. _windows_shading_schedule:

Shading system availability schedule
````````````````````````````````````

.. index:: Shading system setpoint
.. _windows_shading_setpoint:

Shading system setpoint
```````````````````````

.. index:: Shading system transmittance
.. _windows_shading_transmittance:

Shading system transmittance
````````````````````````````

.. index:: Shading system type
.. _windows_shading_type:

Shading system type
```````````````````

.. index:: Zone mixing
.. _windows_zone_mixing:

Zone mixing
```````````

ZoneMixing is intended to allow simplified treatment of air exchange between zones. Note that this statement only affects the energy balance of the “receiving” zone and that this statement will not produce any effect on the “source” zone. More advanced mixing calculations are possible using the AirflowNetwork model for multi-zone airflow with or without HVAC system operation.

.. index:: Zone mixing availability schedule
.. _windows_zone_mixing_schedule:

Zone mixing availability schedule
`````````````````````````````````

This field is the name of the schedule (:ref:`Schedules Tab`) that modifies the maximum design volume flow rate
parameter (see next field). This fraction between 0.0 and 1.0 modifies the design level parameter.

.. index:: Zone mixing delta temperature
.. _windows_zone_mixing_schedule_delta_t:

Zone mixing delta temperature
`````````````````````````````

This number controls when mixing air from the source zone is sent to the receiving zone. This parameter is a temperature and is expressed in units of Celsius. If this field is positive, the temperature of the zone from which the air is being drawn (source zone) must be “Delta Temperature” warmer than the receiving zone air or else no mixing occurs. If this field is negative, the temperature of the source zone must be “Delta Temperature” cooler than the receiving zone air or else no mixing occurs. If this parameter is zero, mixing occurs regardless of the relative zone temperatures.

.. index:: Zone mixing flow rate
.. _windows_zone_mixing_flowrate:

Zone mixing flow rate
`````````````````````

This factor (m3/s-m2) is used, along with the Zone Area to determine the maximum Design Volume Flow Rate as described in the Design Volume Flow Rate field.

.. index:: Virtual partition
.. _windows_virtual_partition:

Virtual partition
`````````````````

.. index:: Airflow network discharge coefficient
.. _windows_airflow_network_disch_coef:

Airflow network discharge coefficient
`````````````````````````````````````

.. index:: Airflow network temperature setpoint
.. _windows_airflow_network_setpoint:

Airflow network temperature setpoint
````````````````````````````````````

.. index:: Airflow network window availability
.. _windows_airflow_network_availability:

Airflow network window availability
```````````````````````````````````
