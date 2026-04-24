# General safety precautions {% tag="general_safety_precautions" %}

{% partial file="partials/safety/warning_drive_over_feet_wear_safety_shoes.md" /%}

{% partial file="partials/safety/warning_drive_into_ladder_scaffolding.md" /%}

{% notice type="warning" %}

Personnel standing next to the robot when the Protective fields are muted risk being injured by an impact.

* Ensure that docking areas are clearly marked as operating hazard zones with visible tape or similar marking and that all personnel are instructed not to stand in the hazard zone when the robot is docking.

{% /notice %}

{% partial file="partials/sensors/warning_robot_detection_limitations_voids_overhangs_glass.md" /%}

{% partial file="partials/service_maintenance/caution_remove_covers_exposes_parts.md" /%}

{% partial file="partials/wi-fi/warning_multiple_radio_modules.md" /%}

{% notice type="warning" %}
The robot risks damage and mechanical failure if  it is used to transport anything other than safely commissioned loads. Nearby equipment and personnel risk damage or injury respectively if payloads fall from the robot.

* Only use the robot to transport safely commissioned loads.
{% /notice %}

{% notice type="warning" %}
If a load is  positioned incorrectly, the load may fall off causing serious injury to personnel and damage to the robot and to equipment.

* Ensure that every load is positioned correctly. During commissioning, determine correct and safe methods of loading. 
* Ensure that loads are securely fastened.
* Conduct a brake test while the robot is transporting a full load.

{% /notice %}

{% if $is_shelf_lift %}

{% notice type="warning" %}
Personnel standing in the blind spot of the robot when it is pivoting with a shelf risk being struck and injured.

* Ensure that all nearby personnel are instructed not to stand close to the robot when it is pivoting. 
* Inform personnel that the signal lights indicate when the robot is intending to turn or pivot—see {% tagref tag="light_indicator_and_speaker" /%} 
{% /notice %}

{% /if %}

{% if $is_forklift %}

{% notice type="warning" %}

The hydraulic fluid used in the pistons is an Aspiration toxicant: Category 1, H304 and may be fatal if swallowed or enters airways.
Use extreme caution when handling hydraulic fluid.

* If accidentally swallowed: Immediately call a poison center or doctor. Do not induce vomiting.

{% /notice %}

{% notice type="warning" %}

If the robot transports a pallet or load that does not meet MiR specifications, the load may become unstable and collide with personnel or equipment causing injury or damage respectively.

* Ensure the robot only transports pallets that meet MiR specifications and match the currently applied SICK configuration file—see {% tagref tag="payload_distribution" /%}

{% /notice %}

{% notice type="warning" %}

If the robot operates in environments with fine dust particles, it can damage the seals of the hydraulic pistons, causing oil leaks. Oil leaks can create a slippery surface for the robot and damage safety-related components. This can cause the robot to collide with personnel or equipment causing injury or damage.

* Never operate the robot in environments with fine dust particles.

{% /notice %}

{% notice type="warning" %}

Personnel risk their feet or hands being crushed beneath a pallet if they are placed beneath the pallet when the robot lowers it.

* Ensure that docking positions are clearly marked as operating hazard zones with visible tape or similar marking and that all personnel are instructed not to stand close to the robot when it is placing a pallet.
* All personnel must be instructed to wear safety shoes near an operating robot.

{% /notice %}

{% notice type="warning" %}

Personnel risk serious hand injuries if they reach in between the robot and a pallet when the robot is picking up the pallet.

* Ensure that docking positions are clearly marked as operating hazard zones with visible tape or similar marking and that all personnel are instructed not to stand close to the robot when it is picking up a pallet.

{% /notice %}

{% notice type="warning" %}

Driving over sills, gaps, or holes in the floor causes the robot to become unstable, and any load may thereby fall off causing serious injury to personnel and damage to the robot and to equipment.

* Never drive over sills, gaps, or holes in the floor.

{% /notice %}

{% /if %}

{% if $has_optional_motion_warning %}
{% notice type="caution" %}

If the robot starts up unexpectedly, there is a risk of injury to nearby personnel or damage to equipment.

* Inform personnel that robot flashes its signal lights and emits warning sounds before is starts moving after being at standstill for longer than 10 seconds.
* Adjust the volume of the warning sounds if they cannot be heard—see {% tagref tag="light_indicator_and_speaker" /%}.
* Do not disable the Motion warning feature in the robot settings. This will also void certification for the following standards: ISO 3691-4, UL3100, and RIA 15.08

{% /notice %}
{% /if %}

{% notice type="caution" %}

This equipment is not intended for use in residential environments and may not provide adequate protection to radio reception in such environments.

* Do not use the robot in residential environments.

{% /notice %}

{% partial file="partials/training/caution_risk_of_fire_abc_training.md" /%}

{% partial file="partials/safety/caution_operating_hazard_zone_engage_emergency_stop.md" /%}

{% partial file="partials/sensors/notice_cannot_detect_forklift_forks_reliably.md" /%}