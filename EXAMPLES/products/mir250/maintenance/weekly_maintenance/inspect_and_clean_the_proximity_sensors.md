# Inspect and clean the proximity sensors {% tag="inspect_and_clean_the_proximity_sensors" %}

<image: "mir250\_maintenance\_proximity\_scanners.png">

## Purpose

The proximity sensors are disabled by default. This maintenance task is only relevant if you have enabled the proximity sensors in the robot interface. See MiR250, MiR600, and MiR1350 Technical Guide for more information. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/).

Inspecting and cleaning the proximity sensors is necessary in order to ensure optimal performance of the sensors. Dust and debris may interfere with the infrared light from the sensors.

Frequency: **weekly**

To complete this task, the robot does not need to be powered.

Turn off the robot, and disconnect the battery.

  * When performing maintenance on robots, you risk electrical shock from electrical wires and connectors if internal components are exposed, crushing, collision, or pinching from unexpected movements.

## Procedure

  1. Inspect the proximity sensors by looking up from beneath and verify that the sensors are clean.

  2. If necessary, use a cotton swab to clean the proximity sensors. MiR250 has eight proximity sensor modules, each having three infrared sensors inside. Ensure that all sensors are cleaned thoroughly.

## Pass criteria <image: "mmg\_pass.svg">

  * All sensors are clean and that there are no visible dust or debris present.

## Remediation

{% table %}

 * Issue
 * Remedial action
 ---
 * Proximity sensors detecting nonexistent obstacles despite being clean.
 * Recalibrate the proximity sensors. See How to calibrate the proximity sensors. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/).

{% /table %}