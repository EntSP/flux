# Check the control panel {% tag="check_the_control_panel" %}

<image: "mir250\_test\_control\_panel.png">

## Purpose

To verify that the control panel buttons function as expected, and that the robot can switch operating modes using the Operating mode key.

Frequency: **quarterly**

To complete this task, the battery must be connected, and the robot must be turned on.

When performing maintenance, you risk electrical shock from exposed electrical wires, and crushing, collision, or pinching from unexpected movement.

  * Be careful of exposed electrical wires.

  * Avoid inserting your hands between actuators or other moving parts of the robot.

  * Make sure the drive wheels are not in contact with the ground—see [Lifting the robot](../How to lift the robot.htm).

## Procedures

If the robot is turned on:

  1. Press the Manual stop button (left), and verify that the robot stops the task it is currently performing, and that it enters Manual stop. Manual stop brings the robot into the same state as a Protective stop where it can only be brought to an operational state by pressing the Restart button.

  2. Press the Restart button (middle), and verify that the robot is brought out of Manual stop, as engaged in the previous step.

  3. Test the Restart button with the Operating mode key:

     1. Turn the Operating mode key to one of the two other operating positions.

     2. Press the Restart button (middle), verify that the robot confirms the new mode.

     3. Turn the key to the last position.

     4. Press the Restart button again, and verify that the robot confirms the new mode.

     5. Turn the Operating mode key to Autonomous mode (left) and press the Restart button (middle) again, verify that the robot confirms the new mode.

  4. Press and hold the Power button (right) for 3 seconds. Verify that the robot turns off.

  5. Once the robot has turned off, press the Power button (right) again. Verify that the robot turns on.

If the robot is turned off:

  1. Press and hold the Power button (right) for 3 seconds. Verify that the robot turns on.

  2. Once the robot has turned on, it will go into a stopped state. Press the Restart button (middle) to clear this state.

  3. Press the Manual stop button (left) and verify that the robot stops the task it is currently performing, and that it enters Manual stop.

  4. Press the Restart button (middle) and verify that the robot is brought out of Manual stop.

  5. Press and hold the Power button (right) for 3 seconds. Verify that the robot turns off.

## Pass criteria <image: "mmg\_pass.svg">

  * All buttons on the control panel work and perform the expected action.

  * The Operating key works as intended, and the robot switches between modes when the key is being turned.

## Remediation

{% table %}

 * Issue
 * Remedial action
 ---
 * One or more buttons are not working.

{% /table %}

  * Make sure that the robot is not set to Locked mode (Operating mode key is in middle position).
  * The affected button should be replaced. See the guide How to replace the control panel interfaces on MiR250. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-replace/how-to-replace-the-control-panel-interfaces-on-mir250/).

Operating mode key is unable to switch modes. |  The control panel should be replaced. See the guide How to replace the control panel interfaces on MiR250. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-replace/how-to-replace-the-control-panel-interfaces-on-mir250/).