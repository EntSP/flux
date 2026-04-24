---
id: "item-xxx"
type: "article"
title: "Contacting technical support"
status: "published"
version: "1.0"
language: "en-us"
firstReleaseDate: "2025-11-04"
updateDate: "2025-11-04"
tags:
- "technical support"
- "help"
- "jira"
accessLevel: "public"
---

# Contacting technical support

If you were not able to remedy any battery issues you are experiencing using this guide, contact technical supportn++see [How to create a technical support ticket](https://supportportal.mobile-industrial-robots.com/documentation/how-to-create/how-to-create-a-technical-support-ticket/).

Before creating a support request, update to the latest recommended software, as this may resolve the issue. It will also enable your robot to generate a more detailed error log.

You must include the following information in your support request:

- A description of what troubleshooting steps you executed and the results in each step.

- The robot serial number. This can be read from the robot's nameplate.

- The battery serial number.

- The chargers you have used to charge the battery on a regular basis and troubleshoot the battery. Include the brand and model.

- A short description of when the battery failed. For example:
  - While using a top module

  - Charging in a charging station

  - Charging with a cable charger

  - After the battery has been in storage or the robot has not been used. Include the length of time the battery has been idle and the battery percentageprior to storage if possible.
- The ambient temperature around the robot or battery approximately.

- The voltage measurement between Host-detect and Power - n++see [Measuring the battery's host voltage](troubleshooting/checking.htm#Measurin). For warranty purposes, include a picture of the reading from the voltmeter and the setup when taking the measurement.

- The voltage measurement between CAN high and Power - n++see [Measuring the CAN bus voltage](troubleshooting/checking.htm#Measurin2). For warranty purposes, include a picture of the reading from the voltmeter and the setup when taking the measurement.

- Which voltmeter you used to take the above two measurements. Include the brand and model.

If possible, attach an error log retrieved from a robot with the problematic battery. It is important that the error log is generated as described in the guide _How to generate an error log_. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/).

To gain access to the robot interface to generate an error log, you have two options:

- ( _MiR250, MiR500, and MiR1000 only_) Connect MiR Cable Charger Lite 48V 3A to the robot while the battery is connected, and wait until the robot turns on. Sign in to the robot interface, download the last generated error log, and generate and download a new one. Include both error logs in your support request.

- If you have a spare battery, you can try to connect this to the robot instead and then turn on the robot. Download the last generated error log, and generate and download a new one. Include both error logs in your support request.

If there is a hardware problem within the robot, you risk shutting down the second battery permanently when you connect it to the robot.

- Check everything in [Troubleshooting the robot](troubleshooting/robot.htm#Low) before connecting another battery to the robot.

Include any reported error codes, images, or videos of the issue.