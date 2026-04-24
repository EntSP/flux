# Check hardware health status {% tag="check_hardware_health_status" %}

<image: "hardware\_health\_monthly\_maintenance.png">

## Purpose

Regularly checking hardware health status contributes to discovering potential errors or warnings before they become problems that can result in unexpected and prolonged downtime.

Frequency: **monthly**

## Procedure

  1. In the robot interface, go to **Monitoring > Hardware health**.

  2. Verify that there are no red or yellow markings. Any errors or warnings will show at the top level of the different hardware categories.

Note that warnings related to "Node ID 03: Right motor" and "Node ID 04: Left motor" showing **CAN node has disconnected** is normal whenever the robot is in either Protective stop or Emergency stop.

  3. If you see an error or warning, navigate to the source by opening the corresponding menus.

  4. Note down any potential errors or warnings, and take the appropriate actions.

## Pass criteria <image: "mmg\_pass.svg">

  * No errors present in hardware health.

  * No warnings present in hardware health.