
.. _tabZoneInfoVentilation:

Ventilation
===========

.. csv-table::
   :file: ../../tables/ventilation.csv
   :header-rows: 1
   :widths: 20,50,15,15

.. index:: Infiltration
.. _vent_infiltration:

Infiltration
````````````

This field is the name of the schedule that modifies the maximum design volume flow rate (see Design Flow Rate Calculation Method field and related subsequent fields). This fraction between 0.0 and 1.0 is noted as in the above equation.

.. index:: Infiltration rate
.. _vent_infiltration_rate:

Infiltration rate
`````````````````

.. index:: Natural ventilation
.. _vent_nat:

Natural ventilation
```````````````````

Natural ventilation is assumed to be air movement/exchange as a result of openings in the building façade and will not consume any fan energy. For this model, the ventilation air flow rate is a function of wind speed and thermal stack effect, along with the area of the opening being modeled. This object can be used alone or in combination with :ref:`vent_schduled`. This model is intended for simplified ventilation calculations as opposed to the more detailed ventilation investigations that can be performed with Energy+'s AirflowNetwork model. Using the “Wind and Stack with Open Area” model, the natural ventilation flow rate can be controlled by a multiplier fraction schedule applied to the user-defined :ref:`windows_operable_area` and through the specification of minimum, maximum and delta temperatures. The temperatures are taken as single constant values for the entire simulation.

.. Note::

   Note that if :ref:`vent_nat` is used in combination with :ref:`vent_schduled`, the resulting ventilation rate for the zone will simply be the summation of the flow rates specified by the ventilation objects.

.. index:: Nat vent min outdoor air temp
.. _vent_nat_min_outdoor_temp:

Natural ventilation minimum outdoor air temperature
```````````````````````````````````````````````````

This is the outdoor temperature (in Celsius) below which ventilation is shut off. The minimum value for this field is -100.0°C and the maximum value is 100.0°C. The default value is -100.0°C if the field is left blank. This lower temperature limit is intended to avoid overcooling a space, which could result in a heating load.

.. index:: Natural ventilation maximum outdoor air temperature
.. _vent_nat_max_outdoor_temp:

Natural ventilation maximum outdoor air temperature
```````````````````````````````````````````````````

This is the outdoor temperature (in Celsius) above which ventilation is shut off. The minimum value for this field is -100.0°C and the maximum value is 100.0°C. The default value is 100.0°C if the field is left blank. This upper temperature limit is intended to avoid overheating a space, which could result in a cooling load.

.. index:: Natural ventilation maximum relative humidity
.. _vent_nat_max_rh:

Natural ventilation maximum relative humidity
`````````````````````````````````````````````

Defines the dehumidifying relative humidity setpoint, expressed as a percentage (0-100), for each timestep of the simulation.

.. Note::

   The default value for the Minimum Relative Humidity is 20C.

.. index:: Natural ventilation schedule
.. _vent_nat_schedule:

Natural ventilation schedule
````````````````````````````

This field is the name of the schedule (:ref:`schedule`) which ultimately modifies the Opening Area value (see previous field). In its current implementation, any value greater than 0 will consider, value above The schedule values must be any positive number between 0 and 1 as a fraction. 

.. index:: Natural ventilation zone temperature setpoint
.. _vent_nat_zone_temp_setpoint:

Natural ventilation zone temperature setpoint
`````````````````````````````````````````````

.. index:: Scheduled ventilation
.. _vent_schduled:

Scheduled ventilation
`````````````````````

Ventilation is the purposeful flow of air from the outdoor environment directly into a thermal zone in order to provide some amount of non-mechanical cooling. Scheduled Ventilation is intended to model “simple” ventilation as opposed to the more detailed ventilation investigations that can be performed with the AirflowNetwork model or with air systems that have outdoor air mixers. Zone ventilation can be controlled by a :ref:`vent_scheduled_schedule` and through the specification of :ref:`vent_scheduled_setpoint`, maximum and delta temperatures as described below. Note that maximum and delta temperatures are not supported yet in the Template Editor.

.. Note::

   Natural ventilation is assumed as a result of openings in the building façade and will not consume any fan energy. Values for fan pressure and efficiency for natural ventilation are ignored. The conditions of the air entering the space are assumed to be equivalent to outside air conditions.

.. index:: Scheduled ventilation ACH
.. _vent_scheduled_ach:

Scheduled ventilation ACH
`````````````````````````

This factor, along with the Zone Volume, will be used to determine the Design Flow Rate.

.. index:: Scheduled ventilation schedule
.. _vent_scheduled_schedule:

Scheduled ventilation schedule
``````````````````````````````

This field is the name of the schedule (:ref:`Schedules Tab`) that modifies the maximum design volume flow rate. This fraction is between 0.0 and 1.0.

.. index:: Scheduled ventilation setpoint
.. _vent_scheduled_setpoint:

Scheduled ventilation setpoint
``````````````````````````````

This is the indoor temperature (in Celsius) below which ventilation is shutoff. The minimum value for this field is -100.0°C and the maximum value is 100.0°C. The default value is -100.0°C if the field is left blank. This lower temperature limit is intended to avoid overcooling a space and thus result in a heating load. For example, if the user specifies a minimum temperature of 20°C, ventilation is assumed to be available if the zone air temperature is above 20°C. If the zone air temperature drops below 20°C, then ventilation is automatically turned off.

.. Note::

   Since the Template Editor does not support changing the values of the Maximum Indoor Temperature, the value will be left blank meaning that the default value is 100.0°C.


.. index:: Buoyancy
.. _vent_buoyancy:

Buoyancy
````````

.. index:: Wind
.. _vent_wind:

Wind
````

.. index:: Afn
.. _vent_afn:

Afn
```
