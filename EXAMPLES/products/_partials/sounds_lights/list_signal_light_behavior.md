The signal lights indicate the following robot behavior:

* When the robot turns, the signal lights on the side the robot is turning to flash white.

* When the Protective fields are muted, all signal lights flash. This is accompanied by auditory warning sounds.

* When the robot is at standstill for longer than 10 seconds the signal lights turn off.

* When the robot begins moving after being at standstill, the signal lights turn on 2 seconds before the robot moves. This is accompanied by auditory warning sounds.

    {% if $has_optional_motion_warning %}
    This behavior was introduced in software 3.6.0 and MiR Fleet Enterprise 1.2.0. You can disable this behavior in the robot interface under **System > Settings > Features > Motion warning**.
    {% /if %}