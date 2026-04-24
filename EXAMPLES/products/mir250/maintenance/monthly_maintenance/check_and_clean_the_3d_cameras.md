# Check and clean the 3D cameras {% tag="check_and_clean_the_3d_cameras" %}

<image: "mir250\_maintenance\_inspect\_3D\_cameras.png">

## Purpose

To ensure that the robot's obstacle detection capability is functioning optimally. Any scratches, damages, or dirt on the 3D camera lenses may be interpreted as non-existent obstacles, which will impede the robot's ability to move properly.

Frequency: **monthly**

To complete this task, the battery must be connected, and the robot must be turned on.

When performing maintenance, you risk electrical shock from exposed electrical wires, and crushing, collision, or pinching from unexpected movement.

  * Be careful of exposed electrical wires.

  * Avoid inserting your hands between actuators or other moving parts of the robot.

  * Make sure the drive wheels are not in contact with the ground—see [Lifting the robot](../How to lift the robot.htm).

## Procedure

  1. Visually inspect the 3D cameras for any visual defects, such as cracks and scratches. Use a flashlight to better be able to see dust and potential scratches on the glossy surface of the 3D cameras.

  2. Wipe off the lens surface of the 3D cameras with a microfibre cloth to remove any dust or debris.

Do not use paper-based material, such as tissues, to clean the safety laser scanners, as these can scratch the 3D camera lens surface.

  3. Open the robot interface, and navigate to **Monitoring > Hardware health**.

<image: "maintenance\_hw\_health\_cameras.png">

  4. For each 3D camera, open **Connection** , and ensure that the data frequency is around 15 Hz.

<image: "maintenance\_hw\_health\_cameras\_freq.png">

  5. Open the active map under **Setup > Maps**, and verify that the 3D cameras detect objects. See the guide How to test if the 3D cameras are working on MiR robots for more information. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-test/how-to-test-if-the-3d-cameras-are-working-on-mir-robots/).

See a [video](https://vimeo.com/896175303) of the process on the Mobile Industrial Robots profile on vimeo.com.

## Pass criteria <image: "mmg\_pass.svg">

  * The 3D camera lenses are clean.

  * The 3D cameras have no scratches or damages.

  * Hardware health within the robot interface shows no warnings or errors for the 3D cameras.

  * The 3D cameras detect objects as intended.

## Remediation

{% table %}

 * Issue
 * Remedial action
 ---
 * The 3D camera lenses are scratched or damaged to a degree that impacts robot performance.
 * Replace the 3D cameras. See the guide How to replace the 3D cameras on MiR250. You can find  this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-replace/how-to-replace-the-3d-cameras-on-mir250/).

---

 * The 3D cameras detect objects, but not in the positions that are expected.

{% /table %}

  * The serial numbers of the 3D cameras may have been swapped in connection with a replacement. Verify that the 3D cameras are set correctly to left and right with the corresponding serial numbers in the robot interface under **System > Settings > 3D cameras**.
  * The following remedial actions can be attempted, but it is recommended to contact MiR Technical Support first.
    * Try to update the 3D camera firmware. See the guide How to update the D435 3D camera firmware. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-update/how-to-update-the-d435-3d-camera-firmware/).
    * Try to recalibrate the 3D camera. See the guide How to calibrate a D435 3D camera. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-calibrate/how-to-calibrate-a-d435-3d-camera/).

The 3D cameras exhibit other non-intended behavior. |  See the guide Troubleshoot 3D cameras not working. You can find this guide on [MiR Support Portal.](https://supportportal.mobile-industrial-robots.com/documentation/troubleshooting/troubleshoot-3d-cameras-not-working/)