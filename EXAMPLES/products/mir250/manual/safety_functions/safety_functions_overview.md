# Safety functions overview {% tag="safety_functions_overview" %}

This section lists all safety functions and their associated triggering event, reaction, reliability, and how it is realized.

The following terms are used in the table:

* **PFHd** : The Probability of dangerous Failures per Hour as defined in EN ISO 13849-1:2015
* **PL** : Performance Level as defined in EN ISO 13849-1:2015
* **Architecture** : As defined in EN ISO 13849-1:2015

{% table %}

* Function name
* Description
* PFHd, PL, and architecture

{% if $safety_function_emergency_stop.active %}

---

* Emergency stop
*   **Triggering event** : Pressing an Emergency stop button connected to the robot—see {% tagref tag="emergency_stop" /%}.

    **Reaction** : Category 0 stop (IEC 60204-1) and mechanical spring-applied brakes engage. The robot enters Emergency stop.

    **Reset function** : Release all Emergency stop buttons, and press the Restart button on the robot.

    **Active** : Always.

*   **PFHd:** {% $safety_function_emergency_stop.pfhd %}

    **PL:** {% $safety_function_emergency_stop.pl %}

    **Architecture:** {% $safety_function_emergency_stop.architecture %}

{% /if %}

{% if $safety_function_overspeed_detection.active %}

---

* Overspeed
*   **Triggering event** : The speed of the robot exceeding the defined values in {% tagref tag="overspeed_detection" /%}.

    **Reaction** : Category 0 stop (IEC 60204-1) and mechanical spring-applied brakes engage. The robot enters Protective stop.

    **Reset function** : Press the Restart button on the robot.

    **Active** : Always.

*   **PFHd:** {% $safety_function_overspeed_detection.pfhd %}

    **PL:** {% $safety_function_overspeed_detection.pl %}

    **Architecture:** {% $safety_function_overspeed_detection.architecture %}

{% /if %}

{% if $safety_function_field_switching.active %}

---

* Field switching

*   **Triggering event** : Activate the relevant Protective field according to the robot's speed and state—see {% tagref tag="field_switching_and_personnel_detection" /%}.

    **Reaction** : A predefined Protective field is selected.

    **Reset function** : Continuous function. No action required.

    **Active** : Always.

*   **PFHd:** {% $safety_function_field_switching.pfhd %}

    **PL:** {% $safety_function_field_switching.pl %}

    **Architecture:** {% $safety_function_field_switching.architecture %}

{% /if %}

{% if $safety_function_personnel_detection.active %}

---

* Personnel detection
*   **Triggering event** : Safety laser scanners detecting an unexpected object in the active Protective field—see {% tagref tag="field_switching_and_personnel_detection" /%}. The robot enters Protective stop.

    **Reaction** : The robot will stop within the active Protective field if the payload, CoM, mass inertia moment, and friction coefficient are within specifications.

    **Reset function** : Resumes automatically after 2 s of cleared Protective field.

    **Active** : Always. Unless Protective fields are muted—see [Muted Protective fields](personnel_detection.htm#muted_fields). Muting enables Speed monitoring.

*   **PFHd:** {% $safety_function_personnel_detection.pfhd %}

    **PL:** {% $safety_function_personnel_detection.pl %}

    **Architecture:** {% $safety_function_personnel_detection.architecture %}

{% /if %}

{% if $safety_function_speed_monitor.active %}

---

* Speed monitor
*   **Triggering event** : The speed of either drive wheel exceeds 0.3 m/s while the Protective fields are muted.

    **Reaction** : Category 0 stop (IEC 60204-1) and mechanical spring-applied brakes engage. The robot enters Protective stop.

    **Reset function** : Press the Restart button on the robot.

    **Active** : When Protective fields are muted.

*   **PFHd:** {% $safety_function_speed_monitor.pfhd %}

    **PL:** {% $safety_function_speed_monitor.pl %}

    **Architecture:** {% $safety_function_speed_monitor.architecture %}

{% /if %}

{% if $safety_function_safeguard_stop.active %}

---

* Safeguard stop

*   **Triggering event** : External device delivering 0 V to the Safeguard stop input pins—see {% tagref tag="safeguarded_stop" /%}.

    **Reaction** : Category 0 stop (IEC 60204-1) and mechanical spring-applied brakes engage. The robot enters Protective stop.

    **Reset function** : Resumes when external signals are active (24 V).

    **Active** : Always.

*   S**PFHd:** {% $safety_function_safeguard_stop.pfhd %}

    **PL:** {% $safety_function_safeguard_stop.pl %}

    **Architecture:** {% $safety_function_safeguard_stop.architecture %}

{% /if %}

{% if $safety_function_locomotion.active %}

---

* Locomotion

* **Triggering event** : The speed of the robot exceeding 0.1 m/s—see {% tagref tag="locomotion" /%}.

    **Reaction** : Locomotion pins deliver 0 V.

    **Reset function** : Inapplicable.

    **Active** : Always.

* **PFHd:** {% $safety_function_locomotion.pfhd %}

    **PL:** {% $safety_function_locomotion.pl %}

    **Architecture:** {% $safety_function_locomotion.architecture %}

{% /if %}

{% if $safety_function_mode_selection.active %}

---

* Mode selection

* **Triggering event** : Changing the operating mode of the robot by turning the Operating mode key—see {% tagref tag="control_panel" /%}.

    **Reaction** : Category 0 stop (IEC 60204-1) and mechanical spring-applied brakes engage. The robot enters Protective stop.

    **Reset function** : Press the Restart button on the robot.

    **Active** : Always.

* **PFHd:** {% $safety_function_mode_selection.pfhd %}

    **PL:** {% $safety_function_mode_selection.pl %}

    **Architecture:** {% $safety_function_mode_selection.architecture %}

{% /if %}

{% if $safety_function_system_emergency_stop.active %}

---

* System emergency stop

* **Triggering event** : External device delivering 0 V to the System emergency stop input pins—{% tagref tag="system_emergency_stop_interface" /%}.

    **Reaction** : Category 0 stop (IEC 60204-1) and mechanical spring-applied brakes engage. The robot enters Emergency stop.

    **Reset function** : When external signals are active (24 V), press the Restart button on the robot.

    **Active** : Always.

* **PFHd:** {% $safety_function_system_emergency_stop.pfhd %}

    **PL:** {% $safety_function_system_emergency_stop.pl %}

    **Architecture:** {% $safety_function_system_emergency_stop.architecture %}

{% /if %}

{% if $safety_function_manual_stop.active %}

---

* Manual stop

* **Triggering event** : Pressing the Manual stop button on the control panel—see {% tagref tag="control_panel" /%}.

    **Reaction** : Category 0 stop (IEC 60204-1) and mechanical spring-applied brakes engage. The robot enters Manual stop.

    **Reset function** : Press the Restart button on the robot.

    **Active** : Always.

* **PFHd:** {% $safety_function_manual_stop.pfhd %}

    **PL:** {% $safety_function_manual_stop.pl %}

    **Architecture:** {% $safety_function_manual_stop.architecture %}

{% /if %}

{% if $safety_function_manual_restart.active %}

---

* Manual restart

* **Triggering event** : Pressing the Restart button on the control panel—see {% tagref tag="control_panel" /%}.

    **Reaction** : Re-enables the robot by releasing it from the Category 0 stop (IEC 60204-1) and by disengaging mechanical spring-applied brakes.

    **Reset function** : N/A.

    **Active** : After triggering of Emergency stop, Overspeed, Speed monitor, Mode selection, Manual stop, or after a hardware fault.

* **PFHd:** {% $safety_function_manual_restart.pfhd %}

    **PL:** {% $safety_function_manual_restart.pl %}

    **Architecture:** {% $safety_function_manual_restart.architecture %}

{% /if %}

{% if $safety_function_manual_brake_release.active %}

---

* Manual brake release

* **Triggering event** : Turning the Manual brake release switch on the robot—see {% tagref tag="manual_brake_release_switch" /%}.

    **Reaction** : Category 0 stop (IEC 60204). The robot enters Protective stop.

    **Reset function** : Press the Restart button on the robot.

    **Active** : Always.

* **PFHd:** {% $safety_function_manual_brake_release.pfhd %}

    **PL:** {% $safety_function_manual_brake_release.pl %}

    **Architecture:** {% $safety_function_manual_brake_release.architecture %}

{% /if %}

{% if $safety_function_pallet_lift_position_monitor.active %}

---

* Pallet lift position monitor

* **Triggering event** : The pallet lift delivering 0 V to the Reduced speed input pin and Shelf mode pin indicating respectively that the lift is raised and there is no shelf. The speed of the robot exceeds 0.3 m/s.

    **Reaction** : Category 0 stop (IEC 60204) and mechanical spring-applied brakes engage. The robot enters Protective stop.

    **Reset function** : Press the Restart button on the robot.

    **Active** : When the pallet lift is not in lowest position.

* **PFHd:** {% $safety_function_pallet_lift_position_monitor.pfhd %}

    **PL:** {% $safety_function_pallet_lift_position_monitor.pl %}

    **Architecture:** {% $safety_function_pallet_lift_position_monitor.architecture %}

{% /if %}

{% if $safety_function_shelf_lift_position_monitor.active %}

---

* Shelf lift position monitor

* **Triggering event** : The shelf lift delivering 24 V to Shelf mode pin and the lift changes position.

    **Reaction** : When the lift is raised, the shelf-specific fields are used. When the lift is lowered, the standard fields are used.

    **Reset function** : Continuous function. No action required.

    **Active** : When the shelf lift is in highest position.

* **PFHd:** {% $safety_function_shelf_lift_position_monitor.pfhd %}

    **PL:** {% $safety_function_shelf_lift_position_monitor.pl %}

    **Architecture:** {% $safety_function_shelf_lift_position_monitor.architecture %}

{% /if %}

{% if $safety_function_shelf_detection.active %}

---

* Shelf detection

* **Triggering event** :  When the shelf lift is raised, the safety laser scanners do not detect the shelf legs in the expected positions, and the robot drives over the 0.3 m/s limit.

    **Reaction** : Category 0 stop (IEC 60204) and mechanical spring-applied brakes engage. The robot enters Protective stop.

    **Reset function** : Press the Restart button on the robot.

    **Active** : When the shelf lift is in highest position and a shelf is not detected by the safety laser scanners.

* **PFHd:** {% $safety_function_shelf_detection.pfhd %}

    **PL:** {% $safety_function_shelf_detection.pl %}

    **Architecture:** {% $safety_function_shelf_detection.architecture %}

{% /if %}

{% if $safety_function_pin_position_monitor.active %}

---

* Pin position monitor

* **Triggering event** : Shelf carrier pins in middle position while the speed exceeds 0.3 m/s.

    **Reaction** : Category 0 stop (IEC 60204) and mechanical spring-applied brakes engage. The robot enters Protective stop. The power to the shelf carrier pin motor is cut off.

    **Reset function** : Continuous function. No action required.

    **Active** : Always.

* **PFHd:** {% $safety_function_pin_position_monitor.pfhd %}

    **PL:** {% $safety_function_pin_position_monitor.pl %}

    **Architecture:** {% $safety_function_pin_position_monitor.architecture %}

{% /if %}


{% /table %}
