# Check safety laser scanner contamination {% tag="check_safety_laser_scanner_contamination" %}

<image: "SICK\_SD\_contamination\_measurement.png">

## Purpose

To preemptively assess the level of contamination accumulating on the safety laser scanners. The actual contamination level of the safety laser scanners can be viewed using SICK's safety designer software.

Frequency: **monthly**

To complete this task, the battery must be connected, and the robot must be turned on.

When performing maintenance, you risk electrical shock from exposed electrical wires, and crushing, collision, or pinching from unexpected movement.

  * Be careful of exposed electrical wires.

  * Avoid inserting your hands between actuators or other moving parts of the robot.

  * Make sure the drive wheels are not in contact with the ground—see [Lifting the robot](../How to lift the robot.htm).

## Procedure

You must have a PC with the latest version of SICK safety designer installed. You can download this software from SICK's website.

  1. Connect the computer to the robot. Use an Ethernet cable or an access point dongle.

  2. Open SICK Safety Designer.

  3. Select **Connect**.

  4. Double click on a safety laser scanner from the SICK Safety Designer home page to open it.

<image: "SICK\_SD\_home.png">

  5. Navigate to **Diagnostics > Contamination measurement** to view the measured contamination and see a visual representation of where on the scanner contamination is detected.

  6. If contamination is approaching the limit for contamination warning, clean the safety laser scanner as described in [Inspect and clean the safety laser scanners](../Weekly tasks/wm_inspect_laser_scanners.htm).

## Pass criteria <image: "mmg\_pass.svg">

  * Contamination should be below 40%, but ideally as low as possible.