# Inspect and clean the safety laser scanners {% tag="inspect_and_clean_the_safety_laser_scanners" %}

<image: "mir250\_maintenance\_safety\_laser\_scanner.png">

## Purpose

To ensure that the safety laser scanners are performing optimally. Safety laser scanner contamination or damages will greatly reduce the performance of the robot. Robots can navigate around objects that are not there and experience random Protective stops or errors that prevent the robot from driving if the safety laser scanners are not maintained properly.

Frequency: **weekly**

To complete this task, the battery must be connected, and the robot must be turned on.

When performing maintenance, you risk electrical shock from exposed electrical wires, and crushing, collision, or pinching from unexpected movement.

  * Be careful of exposed electrical wires.

  * Avoid inserting your hands between actuators or other moving parts of the robot.

  * Make sure the drive wheels are not in contact with the ground—see [Lifting the robot](../How to lift the robot.htm).

## Procedure

  1. Visually inspect the optics cover of the safety laser scanner for any obvious damage. Use a flashlight to better see dust and potential scratches on the glossy surface of the optics cover.

  2. Open the robot interface and go to **Monitoring > Hardware health > Safety System > Emergency stop**, scroll down the list and look at the status for **Laser (Front) Contamination Warning** , **Laser (Front) Contamination Error** , **Laser (Rear) Contamination Warning** , and **Laser (Rear) Contamination Error**. If the statuses say "False", the safety laser scanners are not contaminated. If any of the statuses say "True", the corresponding scanner has some contamination present, either dust, smudges, or damage, which triggers the warning.

<image: "safety\_laser\_scanner\_contamination\_interface.png">

  3. Clean the optics cover of both safety laser scanners with a clean microfiber cloth to ensure optimum performance. Do not use any aggressive or abrasive cleaning agents. Ensure to also clean both parts of the optics piece as illustrated by the red areas:

<image: "NanoScan3\_cleaning.png">

Do not use paper-based material, such as tissues, to clean the safety laser scanners, as these might scratch the optics covers.

See a [video](https://vimeo.com/896457318) of the process on the Mobile Industrial Robots profile on vimeo.com.

## Pass criteria <image: "mmg\_pass.svg">

  * The safety laser scanner optics are clean.

  * There are no scratches or damages to the scanner optics.

  * There are no contamination errors present in the robot interface.

## Remediation

{% table %}

 * Issue
 * Remedial action
 ---
 * The safety laser scanner optics is scratched or damaged.
 * Replace the optics cover. See SICK's documentation for the replacement procedure. Alternatively, replace the entire safety laser scanner—see How to replace the safety laser scanners on MiR250. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/).

---

 * The safety laser scanner is defective.
 * Replace the safety laser scanner. See How to replace the safety laser scanners on MiR250. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/).

---

 * The robot keeps reporting contamination errors.
 * See [Check safety laser scanner contamination](../Monthly tasks/mm_check_laser_scanner_contamination.htm).

{% /table %}