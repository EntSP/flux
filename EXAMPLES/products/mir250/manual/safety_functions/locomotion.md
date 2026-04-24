# Locomotion interface {% tag="locomotion" %}

The Locomotion function indicates to the top module safety device when the robot is moving. Use this function to ensure that the top module is not powered while the robot is driving.

This function uses two output pins, where both pins deliver 0 VÂ when the robot is driving and 24 V when the robot is stopped. You can use this interface to make your top module behave differently depending on whether the robot is driving or not.

The interface is intended to be used to program the top module to go into a safe state when the robot is driving. For example, by engaging the brakes in any actuators that may result in injury to personnel.

{% imagegrid %}

{% gridimage image="/images/graphical/safety_system/locomotion_0.webp" alt="Robot is driving so 0 V is sent from the robot" headline="Robot is driving" bodytext="When the robot is driving, the safety PLC sends a 0 V signal to the top module through the Auxiliary safety function interface." /%}

{% gridimage image="/images/graphical/safety_system/locomotion_24.webp" alt="Robot is at standstill and 24V is sent to the top module" headline="Robot is at standstill" bodytext="When the robot is stopped, the signal becomes 24 V." /%}

{% /imagegrid %}

{% partial file="partials/references/text_electrical_interfaces_pins_for_aux_safety.md" /%}