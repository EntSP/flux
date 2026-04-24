# Safeguarded stop interface {% tag="safeguarded_stop" %}

The Safeguarded stop function brings the robot into Protective stop when the top module safety device sends the appropriate signal. Use this function to enable the top module safety device to trigger a Protective stop.

This function uses two input pins where both pins must receive 24 V for the robot to be able to operate. If either or both pins receive 0 V, the robot is brought into Protective stop. The robot can be brought out of Protective stop again if both pins receive 24 V again.

If the input pins are unequally set for more than three seconds, the safety PLC registers this as an error in the system and needs to be reset before the robot can operate again. To do this, you must restart the robot.

{% imagegrid %}

{% gridimage image="/images/graphical/safety_system/reduced_speed_input_safeguard_stop_24.webp" alt="Robot is operating and 24V is delivered from top module." headline="Signal to enable operation" bodytext="If both pins deliver 24 V to the robot, it can operate." /%}

{% gridimage image="/images/graphical/safety_system/safeguard_stop_0.webp" alt="Robot is in Protective stop and 0V is delivered from top module." headline="Signal to enter Protective stop" bodytext="If both of the pins deliver 0 V, the robot enters Protective stop." /%}

{% /imagegrid %}

{% partial file="partials/references/text_electrical_interfaces_pins_for_aux_safety.md" /%}