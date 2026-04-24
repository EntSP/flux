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
﻿# Firmware versions

Firmware 1.2.2 introduced significant changes in the battery behavior. [Table 3.1](#Overview) describes the differences between firmwares before and after the 1.2.2 firmware.

You can see which firmware version the battery is using in the robot interface under Monitoring > Hardware health > Power system > Battery Management System (BMS).

{% image src="/images/accessories/batteries_chargers/screenshots/firmware_version.webp" alt="firmware version" /%}

If you have a battery with a firmware version below 1.1.10 and would like to know more about what is different in this firmware, contact MiR Technical Support.

**Table 3.1**
Overview of firmware differencesSubjectFirmware 1.1.10Firmware 1.2.2n++1.2.6

Firmware 2.0.4n++2.1.0

Description

Original firmware.

Firmware 1.2.2 was first introduced in SW 2.13.1, but was removed in 2.13.3.2 due to instability.

Firmware 1.2.6 was introduced in SW 3.5.2 and uses a more reliable update process and solves various issuesn++see the 3.5.2 release note for more information.

Only for the battery version introduced in hardware 2.1 or batteries with Order number 450744.

Storage time15 months at 75% chargen++see [Storage](../storage.htm).40 months at 75% chargen++see [Storage](../storage.htm).

125 months at 75% chargen++see [Storage](../storage.htm).

Power save timeout at 5% battery percentagen++see [Power save](../battery_states/power_save.htm)Four hoursOne hour

One hour

Power save timeout initialization thresholdn++see [Power save](../battery_states/power_save.htm)Charge or discharge current must be less than 150 mA.Charge or discharge current must be less than 500 mA.

Same as FW 1.2.2n++1.2.6.

Battery discharge disables in Low power mode (you can no longer use the Manual brake release) You have four hours after the battery is in Low power mode before the battery disables discharge. This means you have more time where you can release the brakes manuallyn++see [Power save](../battery_states/power_save.htm#Power). You have one hour after the battery is in Low power mode before the battery disables discharge. This means you only have a little time to release the brakes manually, but the battery can be stored for a longer time afterwardn++see [Power save](../battery_states/power_save.htm#Power).

Same as FW 1.2.2n++1.2.6.

MiR Cable Charger Lite 48V 3A compatibilityThere is a risk that MiR Cable Charger Lite 48V 3A shuts down the battery if the charger is not used correctlyn++see [Cable chargers](../cable_chargers/cable_chargers.htm).MiR Cable Charger Lite 48V 3A is fully compatible. We still recommend following the instructions in [Cable chargers](../cable_chargers/cable_chargers.htm).

Same as FW 1.2.2n++1.2.6.

Overcurrent countersn++see [Electrical voltage, current, and temperature limits](../limits/current_limits.htm#Overcurr)The current can exceed the maximum current 10 times before the battery is shut down and unrecoverable.The current can exceed the maximum current 30 times before the battery is shut down and unrecoverable, but every fifth time, you must contact MiR Technical Support to recover the battery.

The current can exceed any limit a maximum of 3 times within 60 seconds.

Voltage, current, and temperature limitsSee [Revision 1](../safety_functions/fw_1.2.2.htm#Cell2).See [Revision 1](../safety_functions/fw_1.2.2.htm#Cell2).

See [Revision 2](../safety_functions/fw_2.0.4.htm#Cell3).