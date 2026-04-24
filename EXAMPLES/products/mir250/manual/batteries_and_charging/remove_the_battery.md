# Remove battery {% tag="remove_battery" %}

{% if $has_fast_swap %}
To be able to remove the battery, you must first enable the fast swap-option in your robot—see {% tagref tag="enable_fast_swap" /%}.
{% /if %}

To remove a battery, follow these steps:

{% if $is_deckload %}

1. Disconnect the battery—see {% tagref tag="power_connection" /%}.
2. Pull out the battery while supporting it underneath with the other hand.

   {% image src=$image_battery_remove alt="The battery being pulled out of the robot"  /%}

{% else $is_forklift / %}

1.  Remove the left rear cover—see {% tagref tag="access_internal_parts" /%}.
2.  Open the top compartment.
3.  Open the left front hatch.
4.  Lift off the left front hatch from the hinges.

    {% image src="/images/mir1200_pallet_jack/access/lift_off_front_comp_door.webp" alt="Front compartment hatch removed"  /%}

5.  Disconnect the battery.
6.  Remove the battery locking clip. Use a T20 bit.

    {% image src="/images/mir1200_pallet_jack/battery_charging/remove_battery_bracket.webp" alt="Battery locking clip being removed"  /%}

7.  Pull out the battery while supporting it underneath with the other hand.

    {% image src="/images/mir1200_pallet_jack/battery_charging/remove_battery.webp" alt="The battery being pulled out of the robot"  /%}

{% /if %}
