# Inspect and test the signal lights {% tag="inspect_and_test_the_signal_lights" %}

<image: "mir250\_base\_robot\_signal lights.png">

## Purpose

To ensure that the signal lights are in good working order, and that nearby personnel can identify the intended movements of the robot and better adjust to its presence in the environment.

Frequency: **weekly**

To complete this task, the battery must be connected, and the robot must be turned on.

When performing maintenance, you risk electrical shock from exposed electrical wires, and crushing, collision, or pinching from unexpected movement.

  * Be careful of exposed electrical wires.

  * Avoid inserting your hands between actuators or other moving parts of the robot.

## Procedure

  1. In the robot interface, verify that the signal lights are enabled.

  2. On the robot, visually inspect all eight signal lights for visible damage and dirt. Clean them with a damp microfiber cloth if necessary.

  3. It is recommended to create a maintenance map with a signal light test mission.

     1. For software version 2.x and 3.x

In the robot interface, go to **Setup > Maps** and set up zones and positions, so that the robot is forced to take both a left and right turn. See the guide How to use zones on a map. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-use/how-to-use-zones-on-a-map/).

     2. For software version 2.x and 3.x

In the robot interface, go to **Setup > Missions** and create a small mission to have the robot move through a Directional zone and make a turn left and right. You can reuse the same mission for both directions and just reverse the direction of the Directional zone.

     3. For MiR Fleet Enterprise 1.0 and higher

In the MiR Fleet interface, go to **Maps** and set up zones and positions, so that the robot is forced to take both a left and right turn—see MiR Fleet Enterprise documentation for more information. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/).

     4. For MiR Fleet Enterprise 1.0 and higher

In the MiR Fleet interface, go to **Missions** and create a small mission to have the robot move through a Directional zone and make a turn left and right. You can reuse the same mission for both directions and just reverse the direction of the Directional zone.

  4. Physically observe the robot perform the left and right turns, and verify that the signal lights in all corners are blinking accordingly.

  5. Delete the changes in the map. Keep the mission for future maintenance.

See a [video](https://vimeo.com/896180656) of the process on the Mobile Industrial Robots profile on vimeo.com.

## Pass criteria <image: "mmg\_pass.svg">

  * All signal lights are in good working condition, clean, and with no visible defects or damages.

  * Front signal lights show a white color while driving, and rear signal light show a red color while driving.

  * The corresponding signal lights blink whenever the robot is making a turn, either left or right.