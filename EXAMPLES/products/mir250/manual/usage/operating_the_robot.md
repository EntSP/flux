# Operating the robot {% tag="operating_the_robot" %}

The robot has three operating modes: Manual mode, Autonomous mode, and Locked mode.

{% partial file="partials/modes/text_switch_between_modes.md" /%}

## Manual mode {% tag="operate_manually" %}

In this mode, you can drive the robot manually using the joystick in the robot interface. Only one person can control the robot manually at a time.

Manual mode is only intended for initial setup, maintenance situations, or deadlocks.

To control the robot manually, you must connect to the robot interface—see {% tagref tag="connect_to_interface" /%}

{% notice type="warning" %}

When driving the robot in Manual mode it is the driver's responsibility to ensure the safety of nearby personnel. Failure to be aware of the risks and operate the robot with caution can result in injury to personnel or damage to equipment.

* Drive carefully to avoid collisions with any personnel or objects when driving the robot in Manual mode.
* Avoid driving the robot manually without a clear visual of the robot.
* Be aware that you can drive the robot into Forbidden zones and Unpreferred zones on the map.
* Be aware that you can make the robot collide with obstacles even if you do not mute the Protective fields. If you mute the Protective fields the robot will not stop at all for detected obstacles.
* Manual mode is only intended for initialization and maintenance situations or for potential deadlocks.

{% /notice %}

To drive the robot in Manual mode, follow these steps:

1. On the robot, turn the Operating mode key to Manual mode (turn it to the right). The robot enters Emergency stop.
2. In the robot interface, select Manual control under the joystick icon

    {% image src="/images/mir_interfaces_3.0/top_bar/select_manual_control_600_1350.webp" alt="Joystick icon" /%}

3. On the robot, press the Resume button. The status lights turn blue, indicating that the robot is in Manual mode.
4. Use the joystick to move the robot. The robot will go back into emergency stop after a short time of inactivity.

## Automatic mode

{% partial file="partials/modes/text_automatic_mode_description.md" /%}

{% partial file="partials/modes/list_automatic_mode_options.md" /%}

## Locked mode{% tag="locked_mode" %}

{% partial file="partials/modes/text_locked_mode_description.md" /%}