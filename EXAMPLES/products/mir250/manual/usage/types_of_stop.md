# Types of stop {% tag="types_of_stop" %}

## Normal stop

The robot is in Normal stop when you press the Stop button on the control panel, a mission action stops the robot, or you toggle the robot into Paused state. All moving parts are still connected to a power supply.

## Protective stop

The robot enters Protective stop automatically to ensure the safety of nearby personnel.

When the robot is in Protective stop, the status lights of the robot turn red, and you are not able to move the robot or send it on missions until you bring the robot out of the Protective stop. The following cases describe the various Protective stops and how to bring the robot out of them:

{% if $is_deckload %}

* **Switching between Manual mode and Automatic mode**

    After turning the Operating mode key to switch operating modes, the robot enters Protective stop, and the Restart button flashes. Press the Restart button to bring the robot out of Protective stop.

* **The robot finishes the startup process**

    The Restart button will flash after startup. Press the flashing Restart button to bring the robot out of Protective stop.

* **A safety laser scanner detects an object in its active Protective field**

    Remove the object from the active Protective field—see {% tagref tag="field_switching_and_personnel_detection" /%}. The robot will resume its operating state after two seconds.

* **The safety system detects a fault, or the motor control system detects a discrepancy**

    To bring the robot out of Protective stop, resolve the fault causing the error. Use information regarding the error from the robot interface to determine the fault. Go to **Monitoring > Hardware health** to find specific information on what caused the issue. For further guidance, see the troubleshooting guides to help troubleshoot the issue. You can find these guides on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/). Press the Restart button to bring the robot out of Protective stop.

{% else $is_forklift / %}

* **A safety laser scanner detects an object in its active Protective field**

    Remove the object from the active Protective field—see {% tagref tag="field_switching_and_personnel_detection" /%}. The robot will resume its operating state after two seconds.

* **The safety system detects a fault, or the motor control system detects a discrepancy**

    To bring the robot out of Protective stop, resolve the fault causing the error. Use information regarding the error from the robot interface to determine the fault. Go to **Monitoring > Hardware health** to find specific information on what caused the issue. For further guidance, see the troubleshooting guides to help troubleshoot the issue. You can find these guides on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/). Press the Restart button to bring the robot out of Protective stop.

* **The tiller is put into Home position or Safety stop position**

    The robot goes into Protective stop when the tiller is put into Home position or Safety stop position—see {% tagref tag="operate_manually" /%}. Press the Restart button to bring the robot out of Protective stop.

{% /if %}

## Emergency stop

The robot enters Emergency stop when an Emergency stop button has been pressed physically. When you press an Emergency stop button, internal mosfets are switched off so all moving parts of the robot do not receive power.

When the robot is in Emergency stop, the status lights of the robot turn red, and you are not able to move the robot or send it on missions until you bring the robot out of the Emergency stop. To do this, you must release the Emergency stop button and then press the flashing Restart button.

{% partial file="partials/safety/warning_only_use_emergency_stop_buttons_for_emergencies.md" /%}