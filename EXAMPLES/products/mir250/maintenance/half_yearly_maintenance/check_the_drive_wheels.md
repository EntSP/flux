# Check the drive wheels {% tag="check_the_drive_wheels" %}

<image: "mir250\_maintenance\_drive\_wheel.png">

## Purpose

To ensure that the robot is performing optimally. Worn down drive wheels can introduce localization issues, because the robot cannot account for a smaller wheel diameter when calculating the change in position over time relative to map data. When the drive wheels are worn down, the robot cannot accurately calculate how far it has driven since this is based on the wheel rotations. This can cause localization to drift over time, resulting in poor planning performance, irregular driving behavior, and docking issues.

Checking the drive wheel wear regularly also helps to plan replacement of the drive wheels in advance, before localization issues arise.

If your robot has a traction kit installed, it can be difficult to measure the drive wheel precisely. It is recommended to remove the traction kit to obtain a precise measurement. See How to install the MiR250 traction kit and follow the procedure in reverse to remove the traction kit. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/)

Frequency: **half-yearly**

To complete this task, the robot does not need to be powered.

Turn off the robot, and disconnect the battery.

  * When performing maintenance on robots, you risk electrical shock from electrical wires and connectors if internal components are exposed, crushing, collision, or pinching from unexpected movements.

## Procedure

  1. Remove the front and rear compartment covers.

     1. Remove the two screws in the front cover, and remove the cover from the robot. Use a T30 bit.

<image: "front\_unscrew.png"> <image: "front\_remove.png">

     2. Push the two buttons on the rear cover, and remove the cover from the robot.

<image: "rear\_press\_buttons.png"> <image: "rear\_remove.png">

  2. Remove the side compartment covers.

     1. Turn the two screws counterclockwise on the side cover, and remove the cover from the robot. Use a T30 bit.

<image: "side\_unscrew.png">

  3. Measure the diameter of the drive wheel using a vernier caliper or measuring tape to determine the drive wheel wear. Verify that the size is no less than 197.5 mm.

  4. Repeat step 3 for the other drive wheel as well.

See a [video](https://vimeo.com/896452784) of the process on the Mobile Industrial Robots profile on vimeo.com.

## Pass criteria <image: "mmg\_pass.svg">

  * The drive wheels are no less than 197.5 mm in diameter.

## Remediation

{% table %}

 * Issue
 * Remedial action
 ---
 * One or both drive wheels are below the tolerance for replacement.
 * Replace both drive wheels. Drive wheels must always be replaced in pairs. See the guide How to replace the drive wheels on MiR250. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-replace/how-to-replace-the-drive-wheels-on-mir250/). Remember to recalibrate the IMU if replacing the drive wheels. See the guide How to calibrate the IMU. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-calibrate/how-to-calibrate-the-imu/).

---

 * Both drive wheels are within tolerance, but the robot still experiences localization issues.
 * Bad or lost localization can have other causes. Try to adjust the localization if you experience localization issues. See the guide How to use adjust localization and MiR Commissioning Guide. You can find these guides on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-use/how-to-use-adjust-localization/).

{% /table %}