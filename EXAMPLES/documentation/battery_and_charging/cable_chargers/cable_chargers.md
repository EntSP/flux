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
﻿# Cable charger

The most efficient way to charge MiR robots is with MiR charging stations. Cable chargers are intended as a backup solution as they charge significantly slower than charging stations, and because they can only charge the robot's battery to 80n++90%.

When you use any of the cable chargers, make sure to:

- **Always** connect the charger to the power source before connecting the charger to the robot.

{% image src="/images/accessories/batteries_chargers/chargers/power_charger_before_robot_correct.webp" alt="power charger before robot correct" /%}

- **Always** check that the charger LED is on before connecting the charger to the robot.

{% image src="/images/accessories/batteries_chargers/chargers/wait_light.jpg" alt="wait light" /%}

- **Always** check that the battery is connected to the robot before connecting the charger to the robot.

The image shows a Battery lever used for MiR250. To connect the battery on another type of robot, see the user guide or integrator manual for your robot.

{% image src="/images/accessories/batteries_chargers/chargers/connect_battery_first.jpg" alt="connect battery first" /%}{% image src="/images/accessories/batteries_chargers/chargers/connect_battery.jpg" alt="connect battery" /%}

- **Always** wait 30 seconds between connecting and disconnecting the battery and vice-versa.

{% image src="/images/accessories/batteries_chargers/chargers/wait_30.jpg" alt="wait 30" /%}

- **Always** check that the charger is charging the robot. You can see this by checking the LED on the charger as described in the following sections for each charger.

{% image src="/images/accessories/batteries_chargers/chargers/charging.jpg" alt="charging" /%}

- **Never** operate the Battery disconnect switch or Battery disconnect lever while the robot is connected to a cable charger or charging station.

{% image src="/images/accessories/batteries_chargers/chargers/toggle_battery.jpg" alt="toggle battery" /%}

- **If relevant**, ensure the battery is within the temperature limits for chargingn++see [Electrical voltage, current, and temperature limits](../limits/current_limits.htm). Monitor the measured battery temperature under Temperature 1 and Temperature 2.

{% image src="/images/mir_interfaces_3.0/3-Monitoring/3-Hardware_health/battery_temperature_charging.webp" alt="battery temperature charging" /%}

Additionally, each cable charger is designed for certain uses and should be handled differentlyn++see [Table 6.1](#Capabili). Using the wrong cable charger can damage the robot or battery. Make sure to read the following sections before using any of the cable chargers.

**Table 6.1**Capabilities of the cable chargers

Charger typeCharge through charging interface1For MiR250, MiR500, and MiR1000 only.Charge battery directly via adapter cableBattery recovery from Deep sleepMiR Cable Charger Lite 48V 3AYes, see [Charging through the robot](3A.htm#Charging).Avoid if possible. If used, make sure to follow [Charging the battery directly](3A.htm#Charging2) exactly.Avoid if possible. If used, make sure to follow [Charging through the robot](3A.htm#Charging) exactly.MiR Battery Charger 48V 12AYes, unless battery is in Power save or Deep sleepn++see [Charging through the robot](12A.htm#Charging3).Yes, unless battery is in Deep sleepn++see [Charging the battery directly](12A.htm#Charging4).No

Battery Charger, 48V 650W 13.5A (Made to comply with Korean standards.)

Yes, unless battery is in Power save or Deep sleepn++see [Charging through the robot](12A.htm#Charging3).Yes, unless battery is in Deep sleepn++see [Charging the battery directly](12A.htm#Charging4).No

Battery Charger, 48V 1200W 13.5A (Made to comply with Japanese standards.)

Yes, unless battery is in Power save or Deep sleepn++see [Charging through the robot](12A.htm#Charging3).Yes, unless battery is in Deep sleepn++see [Charging the battery directly](12A.htm#Charging4).NoMiR Battery Charger 48V 20A (deprecated)Avoid if possible. If used, make sure to follow [Charging through the robot](12A.htm#Charging3) exactly. Cannot be used if the battery is in Power save or Deep sleep.Avoid if possible. If used, make sure to follow [Charging the battery directly](12A.htm#Charging4) exactly. Cannot be used if the battery is in Deep sleep.No