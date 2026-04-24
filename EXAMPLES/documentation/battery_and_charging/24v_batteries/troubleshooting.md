---
id: "item-xxx"
type: "article"
title: ""
status: "published"
version: "1"
language: "en-us"
firstReleaseDate: "2025-11-04"
updateDate: "2025-11-04"
accessLevel: "public"
---
﻿# Troubleshooting

If you are not able to turn on your robot, there may be an issue with the battery. In many cases, you can determine and troubleshoot what is wrong by observing the Power button when you try to turn on the robotn++see [Battery modes](../battery_states/battery_states.htm).

If you are unable to charge the battery, check that the battery is within the charging temperature limits, and you are using the cable chargers as described in [Cable chargers](../cable_chargers/cable_chargers.htm).

If you are unable to troubleshoot the issue using the descriptions provided in [Battery modes](../battery_states/battery_states.htm), MiR offers a MiR Battery Service Tool (order number 140001) to help you diagnose and troubleshoot issues. You can order this kit from MiR. The tool is not entirely compatible with batteries with firmware 2.0.4 and may diagnose the issue incorrectly.

If you do not have access to a MiR 48V Battery Service Tool, or the tool was not able to detect the issue, troubleshoot the issue manually using this section. You should also troubleshoot the battery if you see any of the following behavior:

- You are unable to charge the battery, neither via the robot's charging interface or when it is connected directly to the robot. This is best to try with a MiR Cable Charger Lite 48V 3A, to ensure that the battery is not in Power save mode or Deep sleep.

- When you connect a charger to the robot while the battery is connected, the Manual stop button flickers.

- When you connect a charger to the robot while the battery is connected, the Power button flickers, does not light up at all, or turns off again after 30 seconds.

- The Manual stop button flashes every 15 seconds.

Before troubleshooting the battery, if you have used an adapter cable, check that the adapter cable is correct as described in [Faulty adapter cable for MiR500 and MiR1000](../adapter_cable/faulty.htm#Faulty2) and that you have not misused it as described in [Foreseeable misuse](../adapter_cable/misuse.htm#Foreseea).

## Overview

To troubleshoot the battery the first step is to determine what mode the battery is in by measuring the host voltage. To determine what mode or state the battery is in, see [Checking the battery](checking.htm#Checking). Once determined, you can continue troubleshooting either the robot or the battery:

- If the battery is in a state where it should be able to charge and power the robot, you must troubleshoot possible issues in the robot or its top module as described in [Troubleshooting the robot](robot.htm#Low).

- If the battery is in a state where it cannot be charged or power the robot, you must first determine if you can recover the battery to a working state, and then whether the issue was caused by leaving the battery unused and depleted for too long, or if there is an issue in the robot or the top module that has affected the battery. This is described in [Battery modes and troubleshooting them](battery.htm).

For a graphical overview of the troubleshooting process see [Figure 9.1](#Overview). There are more detailed descriptions of exactly how to execute each of the steps in the following sections.

**Figure 9.1**Overview of the troubleshooting process

{% image src="/images/accessories/batteries_chargers/troubleshooting/fault_tree_2_txt_en.svg" alt="fault tree 2 txt en" /%}