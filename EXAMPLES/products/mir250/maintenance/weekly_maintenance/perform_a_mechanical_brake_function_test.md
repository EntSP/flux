# Perform a mechanical brake function test {% tag="perform_a_mechanical_brake_function_test" %}

<image: "mir250\_mech\_brake\_function.png">

## Purpose

To ensure that the brakes are always working correctly when they are needed.

The robot has two brakes on each drive wheel:

  * A mechanical brake that is engaged by power-off controlled directly from the safety PLC by the mechanical brake relays. The relays are monitored by a force-guided feedback signal back to the safety PLC.

The mechanical brakes are always applied during any Protective or Emergency stop.

  * A dynamic brake that is engaged by power-on controlled directly from the safety PLC by the dynamic brake contactors. The dynamic brakes consist of two contactors that can short circuit the motor windings and thereby stop the wheel (permanent magnet motor).

The dynamic brake relay has force-guided feedback signal, which is wired back to the safety PLC. The dynamic brakes are self-checked by this signal whenever they are actuated. If the dynamic brakes do not perform as expected, the robot interface reports a Dynamic brake error.

The dynamic brakes are only applied when the Personnel detection safety function triggers a Protective stop. The mechanical brakes are also applied simultaneously.

Frequency: **weekly**

To complete this task, the battery must be connected, and the robot must be turned on.

When performing maintenance, you risk electrical shock from exposed electrical wires, and crushing, collision, or pinching from unexpected movement.

  * Be careful of exposed electrical wires.

  * Avoid inserting your hands between actuators or other moving parts of the robot.

To perform this maintenance task, the robot must not be raised up on supports. The drive wheels should have contact with the floor surface.

## Procedure

Testing the control function:

  1. Power up the robot.

  2. Verify that the manual brake release is not engaged. The manual brake release switch must be turned counterclockwise—see the manual for your robot application.

<image: "mir250\_brake\_release\_switch\_counterclockwise.png">

  3. Attempt to move or twist the robot by hand. Push it both left and right to test the brakes on both sides.

If you are unable to move the robot in either direction, the brakes are functional. If you are able to produce any movement in the robot, one or both of the mechanical brakes are faulty. Contact MiR Technical Support—see How to create a technical support ticket. You can find this document on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com).

<image: "250\_mech\_brake\_test.png">

  4. Enable the manual brake release by turning the manual brake release switch clockwise.

<image: "switch\_turn\_right.png">

  5. Attempt to move or twist the robot by hand. With the manual brake release enabled, the robot must be able to move freely on both drive wheels. If one or both wheels are still locked, contact MiR Technical Support—see How to create a technical support ticket. You can find this document on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com).

Testing the mechanical brakes:

  1. Verify that the manual brake release is not engaged. The manual brake release switch must be turned counterclockwise.

  2. Turn off the robot, and disconnect the battery in the rear compartment —see [Disconnecting the battery](../How to disconnect the battery.htm).

This is done to isolate the mechanical brakes, and to ensure that the dynamic brakes do not interfere.

  3. Attempt to move or twist the robot by hand. Push it both left and right to test the mechanical brakes in either side. If you are unable to move the robot in either direction, both mechanical brakes are functional. If you are able to produce any movement in the robot, one or both of the mechanical brakes are faulty. Contact MiR Technical Support—see How to create a technical support ticket. You can find this document on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com).

<image: "250\_mech\_brake\_test.png">

## Adjust localization

  1. Adjust the localization of the robot after it has been moved manually. Technically, the robot can have its localization affected by mere millimeters of manual movement. See How to use adjust localization for more information. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/).

See a [video](https://vimeo.com/896178500) of the process on the Mobile Industrial Robots profile on vimeo.com.

## Pass criteria <image: "mmg\_pass.svg">

  * The mechanical brakes' correct function is verified as described.