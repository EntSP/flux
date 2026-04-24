# Test the Emergency stop buttons {% tag="test_the_emergency_stop_buttons" %}

<image: "mir250\_maintenance\_test\_emergency\_stop\_button.png">

## Purpose

To ensure that the Emergency stop button(s) on the robot are in good working order for when they are needed.

Frequency: **quarterly**

To complete this task, the battery must be connected, and the robot must be turned on.

When performing maintenance, you risk electrical shock from exposed electrical wires, and crushing, collision, or pinching from unexpected movement.

  * Be careful of exposed electrical wires.

  * Avoid inserting your hands between actuators or other moving parts of the robot.

  * Make sure the drive wheels are not in contact with the ground—see [Lifting the robot](../How to lift the robot.htm).

MiR250 has no integrated Emergency stop buttons, but only an Auxiliary Emergency stop. This maintenance task will vary depending on the design of any custom top modules that are used with MiR250. MiR top modules MiR Hook 250 and MiR Shelf Carrier 250 have fixed integrated Emergency stop buttons.

## Procedure

  1. Verify that the robot is not in Protective or Emergency stop.

  2. Press an Emergency stop button. Verify that the robot enters Emergency stop state.

  3. Release the Emergency stop button by twisting it and pulling it out.

  4. Press the Restart button on the control panel to dismiss the Emergency stop state.

  5. Repeat steps 1–4 for any other Emergency stop buttons on the robot or buttons that are integrated into the top module mounted to the robot. Remember to release and dismiss the previous Emergency stop before moving on to the next one.

See a [video](https://vimeo.com/896165099) of the process on the Mobile Industrial Robots profile on vimeo.com.

## Pass criteria <image: "mmg\_pass.svg">

  * All Emergency stop buttons work as intended and are able to bring the robot into Emergency stop state.

## Remediation

{% table %}

 * Issue
 * Remedial action
 ---
 * One or more Emergency stop buttons are not working.
 * The Emergency stop button should be replaced immediately. The robot should not be used until the Emergency stop button has been replaced. A new Auxiliary Emergency stop unit can be ordered from MiR.

{% /table %}