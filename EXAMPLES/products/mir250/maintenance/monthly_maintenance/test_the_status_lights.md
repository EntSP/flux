# Test the status lights {% tag="test_the_status_lights" %}

<image: "mir250\_maintenance\_test\_status\_lights.png">

## Purpose

To ensure that the robot's different states are represented with the correct color.

Frequency: **monthly**

To complete this task, the battery must be connected, and the robot must be turned on.

When performing maintenance, you risk electrical shock from exposed electrical wires, and crushing, collision, or pinching from unexpected movement.

* Be careful of exposed electrical wires.

* Avoid inserting your hands between actuators or other moving parts of the robot.

* Make sure the drive wheels are not in contact with the ground—see [Lifting the robot](../How to lift the robot.htm).

## Procedure

1. Turn on the robot, wait for it to go into Idle state. Verify that the robot's status lights switch to green.

2. Physically block the safety laser scanner view to trigger a Protective stop. Verify that the robot's status lights switch to red. Unblock the safety laser scanner view again.

3. Press an Emergency stop button to trigger an Emergency stop. Verify that the status lights switch to red. Release the Emergency stop button and press the Restart button.

4. Connect to the robot interface and queue a mission. Pause the mission via the robot interface's mission control, and verify that the status lights switch to orange.

5. Follow these steps to switch to Manual mode:

    1. Turn the Operating mode key to Manual mode (turn it to the right).

    2. Select Manual control under the joystick icon in the robot interface.

    3. Press the Restart button on the robot.

6. Verify that the robot's status lights switch to blue.

7. Turn the Operating mode key back to Automatic mode for default operation.

See the manual for your robot application for more information on Manual mode and for an overview of all states or modes and the corresponding colors.

## Pass criteria <image: "mmg\_pass.svg">

* All the tested states and modes result in the expected color.

{% table %}

* State or Mode
* Color

---

* Idle
* Green

---

* Protective stop
* Red

---

* Emergency stop
* Red

---

* Paused
* Orange

---

* Manual mode
* Blue

{% /table %}