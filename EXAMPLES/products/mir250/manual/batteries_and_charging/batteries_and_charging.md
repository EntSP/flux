# Battery and charging

{% if equals($number_of_batteries, 1) %}
The robot is powered by a 48V lithium-ion battery that can be charged inside the robot with a MiR cable charger or 48V charging station.
{% else / %}
The robot is powered by {% $number_of_batteries %} 48V lithium-ion batteries that can be charged inside the robot with a MiR cable charger or 48V charging station.
{% /if %}

Instructions for charging depend on the charger type and are described in the guides included with each charger.

{% partial file="partials/power/warning_battery_handling.md"/ %}

{% partial file="partials/references/info_battery_data_sheet.md" /%}

{% notice type="notice" %}

Using charging stations incorrectly, failing to maintain charging pads, or driving the robot in areas outside of approved specifications can damage the charging modules on the robot and charging stations.

* Do not drive the robot into a charging station manually.
* Ensure the charging pads are clean and free of oxidation—see {% tagref tag="maintenance_and_handling" /%}.
* Do not drive the robot over any gaps or sills.

{% /notice %}

{% partial file="partials/references/info_battery48v_technical_guide.md"/ %}