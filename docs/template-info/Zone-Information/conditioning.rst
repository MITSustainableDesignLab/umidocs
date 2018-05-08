
.. _tabZoneInfoConditioning:

Conditioning
============

.. csv-table::
   :file: ../../tables/conditioning.csv
   :header-rows: 1
   :widths: 20,50,15,15
   :name: conditioning


.. index:: Heating
.. _cond_heating:

Heating
```````

This checkbox field defines whether or not this component is available to operate. If this field is unchecked, the :ref:`cond_h_schedule` field will be forced to the generic schedule name *Off*.

.. index:: Heating setpoint
.. _cond_h_setpoint:

Heating setpoint
````````````````

The temperature below which zone heating is turned on.

.. index:: Heating schedule
.. _cond_h_schedule:

Heating schedule
````````````````

Schedule for when the heating system is available. Winter only enables the heating system when the outdoor temperature is less than 5 °C.

.. todo:: to confirm

.. index:: Heating limit type
.. _cond_h_limit_type:

Heating limit type
``````````````````

The input must be either **LimitFlowRate**, **LimitCapacity**, **LimitFlowRateAndCapacity** or **NoLimit**. LimitFlowRate means that the heating supply air flow rate will be limited to the value specified in the input field :ref:`cond_h_max_flow`. LimitCapacity means that the sensible heating capacity will be limited to the value specified in the :ref:`cond_h_max_cap` field. LimitFlowRateAndCapacity means that both flow rate and capacity will be limited. NoLimit (the default) means that there will not be any limit on the heating supply air flow rate or capacity and the subsequent two fields will be ignored.

.. index:: Max heating capacity
.. _cond_h_max_cap:

Max heating capacity
````````````````````

The maximum allowed sensible heating capacity in Watts if Heating Limit is set to LimitCapacity or LimitFlowRateAndCapacity. If blank, there is no limit. If Heating Limit is set to NoLimit or LimitFlowRate, this field is ignored.

.. index:: Max heat flow
.. _cond_h_max_flow:

Max heat flow
`````````````

The maximum heating supply air flow rate in cubic meters per second if heating limit is set to LimitFlowRate or LimitFlowRateAndCapacity. This field is ignored if heating limit is set to NoLimit or LimitCapacity. If blank, there is no limit.

.. index:: Heating CoP
.. _cond_h_cop:

Heating CoP
```````````

Efficiency of heating system. This value is used in deriving total heating energy use by dividing the heating load by the heating efficiency.

.. index:: Cooling
.. _cond_cooling:

Cooling
```````

.. index:: Cooling setpoint
.. _cond_c_setpoint:

Cooling setpoint
````````````````

.. index:: Cooling schedule
.. _cond_c_schedule:

Cooling schedule
````````````````

Schedule for when the cooling system is available. Summer only enables the cooling system when the outdoor temperature is greater than 8 °C below the cooling setpoint.

.. todo:: to confirm

.. index:: Cooling limit type
.. _cond_c_limit_type:

Cooling limit type
``````````````````

The input must be either **LimitFlowRate**, **LimitCapacity**, **LimitFlowRateAndCapacity** or **NoLimit**. LimitFlowrate means that the cooling supply air flow rate will be limited to the value specified :ref:`cond_c_max_flow` field. LimitCapacity means that the total cooling capacity will be limited to the value specified in the :ref:`cond_c_max_cap` field. LimitFlowRateAndCapacity means that both flow rate and capacity will be limited. NoLimit (the default) means that there will not be any limit on the cooling supply air flow rate or capacity and the subsequent two fields will be ignored.

.. index:: Max cooling capacity
.. _cond_c_max_cap:

Max cooling capacity
````````````````````

.. index:: Max cool flow
.. _cond_c_max_flow:

Max cool flow
`````````````

The maximum cooling supply air flow rate in cubic meters per second if Cooling Limit is set to LimitFlowRate or LimitFlowRateAndCapacity. This field is ignored if cooling limit is set to NoLimit or LimitCapacity. If blank, there is no limit. If Cooling Limit is set to NoLimit, this field is ignored. This field is required if Outdoor Air Control Type is TemperatureEconomizer in order to establish an upper limit on outdoor air flow when the economizer is active.

.. index:: Cooling CoP
.. _cond_c_cop:

Cooling CoP
```````````

Performance factor of cooling system. This value is used in deriving the total cooling energy use by dividing the cooling load by the COP.

.. index:: Mechanical ventilation
.. _cond_mech_vent:

Mechanical ventilation
``````````````````````

.. index:: Mechanical ventilation schedule
.. _cond_mv_schedule:

Mechanical ventilation schedule
```````````````````````````````

.. index:: Min fresh air per area
.. _cond_min_freshair_area:

Min fresh air per area
``````````````````````

The design outdoor air volume flow rate per square meter of floor area (units are m3/s-m2). This input is used if Outdoor Air Method is Flow/Area, Sum or Maximum. The default value for this field is 0.

.. Note::

   Umi uses by default the *Sum* method which means that the flows calculated from the fields :ref:`cond_min_freshair_pers`, :ref:`cond_min_freshair_area`, Outdoor Air Flow per Zone, and Air Changes per Hour (using the associated conversions to m3/s for each field) will be added to obtain the zone outdoor air flow rate.

.. index:: Min fresh air per person
.. _cond_min_freshair_pers:

Min fresh air per person
````````````````````````

Outdoor fresh air supply relative to current occupancy.

.. index:: Economizer type
.. _cond_econ_type:

Economizer type
```````````````

This field specifies if there is an outdoor air economizer. The choices are: NoEconomizer, DifferentialDryBulb, or DifferentialEnthalpy. The default is NoEconomizer. DifferentialDryBulb and DifferentialEnthalpy mean that the economizer will increase the outdoor air flow rate above the minimum outdoor air flow (see fields Design Specification Outdoor Air Object Name and Demand Controlled Ventilation Type) when there is a cooling load and the outdoor air temperature or enthalpy is below the zone exhaust air temperature or enthalpy. The DifferentialDryBulb and DifferentialEnthalpy options require that the :ref:`cond_c_max_flow` be specified which will be used as the limit for maximum outdoor air flow rate.

.. index:: Heat recovery type
.. _cond_hr_type:

Heat recovery type
``````````````````

Select from None, Sensible, or Enthalpy. None means that there is no heat recovery. Sensible means that there is sensible heat recovery whenever the zone exhaust air temperature is more favorable than the outdoor air temperature. Enthalpy means that there is latent and sensible heat recovery whenever the zone exhaust air enthalpy is more favorable than the outdoor air enthalpy. The default is None.

.. index:: Heat recovery efficiency (latent)
.. _cond_hr_eff_latent:

Heat recovery efficiency (latent)
`````````````````````````````````

The latent heat recovery effectiveness, where effectiveness is defined as the change in supply humidity ratio divided by the difference in entering supply and relief air humidity ratios. The default is 0.65.

.. index:: Heat recovery efficiency (sensible)
.. _cond_hr_eff_sensible:

Heat recovery efficiency (sensible)
```````````````````````````````````

The sensible heat recovery effectiveness, where effectiveness is defined as the change in supply temperature divided by the difference in entering supply and relief air temperatures. The default is 0.70.
