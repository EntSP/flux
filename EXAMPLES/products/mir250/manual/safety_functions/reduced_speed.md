# Reduced speed interface {% tag="reduced_speed" %}

{% notice type="caution" %}
The Reduced speed function is not a safety-rated function. Using this function with a top module and expecting the robot to enter a safe state when the Reduced speed function is active can lead to injury of personnel.

* Do not use the Reduced speed function as a means for safety-related risk reduction.

{% /notice %}

The Reduced speed function makes the robot drive at a reduced speed of 0.3 m/s. This is the same speed used when the robot mutes its Protective fields. Use this function to make the robot slow down when the top module is active or in an unsafe state, but the robot should not stop completely.

{% if $has_two_pins_for_reduced_speed_function %}

The interface uses two input pins where the robot drives at a reduced speed if either input is 0 V.

{% imagegrid %}

{% gridimage image="/images/graphical/safety_system/reduced_speed_input_safeguard_stop_24.webp" alt="Robot is driving at default speed. 24V delivered from the top module." headline="Defualt speed" bodytext="The robot drives at its default speed only when both inputs are 24 V." /%}

{% gridimage image="/images/graphical/safety_system/reduced_speed_input_0_0.webp" alt="Robot is driving at reduced speed. 0V delivered from the top module." headline="Reduced speed" bodytext="If either pin is 0 V, the robot drives at 0.3 m/s." /%}

{% /imagegrid %}

{% else / %}

The interface uses one input pin where the robot drives at a reduced speed when it is 0 V.

{% imagegrid %}

{% gridimage image="/images/graphical/safety_system/reduced_speed_input_600_1350.webp" alt="Robot is driving at default speed. 24V delivered from the top module." headline="Defualt speed" bodytext="The robot drives at its default speed only when the input is 24 V." /%}

{% gridimage image="/images/graphical/safety_system/reduced_speed_input_0_600_1350.webp" alt="Robot is driving at reduced speed. 0V delivered from the top module." headline="Reduced speed" bodytext="If the pin delivers 0 V, the robot drives at 0.3 m/s." /%}

{% /imagegrid %}

{% /if %}

{% partial file="partials/references/text_electrical_interfaces_pins_for_aux_safety.md" /%}