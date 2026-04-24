# Emergency stop{% tag="emergency_stop" %}

{% if $has_estop_box %}
The robot is delivered with an Emergency stop box that you connect to the Auxiliary emergency stop interface—see {% tagref tag="unpack_the_robot" /%}. When you press the button, the robot enters Emergency stop—see {% tagref tag="types_of_stop" /%}.
{% else / %}
{% partial file="partials/safety/text_estop_button_triggers_estop.md" /%}
{% /if %}

You can connect a circuit of any number of Emergency stop buttons to the Auxiliary emergency stop interface. These are intended for Emergency stop buttons on the connected top module. When the circuit is closed, the robot can operate. When the circuit breaks, the robot enters Emergency stop.

If you do not connect a closed circuit from your top module, you must connect a dummy plug or Emergency stop box that connects the appropriate pins in Auxiliary emergency stop interface to close the circuit.

To see which pins in the electrical interface support this function, see {% tagref tag="electrical_interfaces_auxiliary_emergency_stop" /%}

{% imagegrid %}
{% gridimage image="/images/graphical/safety_system/estop_released.webp" alt="Emergency stop button released" headline="Emergency stop button released" bodytext="If the input pins deliver 24 V to the robot, it can operate." /%}
{% gridimage image="/images/graphical/safety_system/estop_pressed.webp" alt="Emergency stop button pushed" headline="Emergency stop button pushed" bodytext="When you push a connected Emergency stop button, both pins deliver 0 V, and the robot enters Emergency stop." /%}
{% /imagegrid %}

{% partial file="partials/safety/warning_only_use_emergency_stop_buttons_for_emergencies.md" /%}