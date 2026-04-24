# Power connection {% tag="power_connection" %}

The robot's battery power source is connected to the robot with a main battery connector.

Before connecting or disconnecting the robot from its battery power source, always disconnect the robot from all charging devices.

Use the Battery lever to connect or disconnect the main battery connector behind the lever.

{% image src=$image_battery_connection  alt="Battery connection" /%}

{% if equals($location_battery_lever_compartment ,"rear compartment") %}
The Battery lever is in the rear compartment—see {% tagref tag="access_internal_parts" /%}.
{% else equals($location_battery_lever_compartment ,"power interface compartment") / %}
The Battery lever is in the power interface compartment—see {% tagref tag="access_internal_parts" /%}.
{% else equals($location_battery_lever_compartment ,"left compartment") / %}
The Battery lever is in the left compartment—see {% tagref tag="access_internal_parts" /%}.
{% /if %}

{% if $is_forklift%}
Each battery also has its own connector. Before using the main battery connector, you must connect the three separate battery connectors—see {% tagref tag="connect_batteries" /%}
{% /if%}

Disconnect the robot from power to prevent unnecessary discharge, risk of electrocution, and risk of short circuiting.

## When to connect power

{% partial file="partials/power/list_connect_to_power.md" /%}

## When to disconnect power

{% partial file="partials/power/list_disconnect_from_power.md" /%}