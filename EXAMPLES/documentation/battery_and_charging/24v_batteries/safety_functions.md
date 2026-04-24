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
﻿# Revision 2

To identify your battery version, see [Battery versions](../versions.htm).

## Voltage

**Table 8.1**Voltage limits for revision 2 batteriesDescriptionTrigger

Reaction

ReleaseOvervoltage

Any cell above 4.25 V

Host voltage above 55.25 V

Cannot charge

All cells below 3.997 V

Host voltage below 52.0 V

Undervoltage

Any cell below 3.187 V

Host voltage below 41.4 V

Cannot power robot

All cells above 3.339 V

Host voltage above 43.4 V

Severe overvoltage

Any cell above 4.3 V

Battery unrecoverable

Sever undervoltage

Any cell below 2.1 V

Battery unrecoverable

Cell imbalance protection threshold500 mV differences and all cells are above 3500 mV

Battery unrecoverable

## Overcurrent

When an overcurrent limit is exceeded, it triggers a 60 s counter, and the battery turns off temporarily. After 15 s, the battery is enabled again.

If the same overcurrent limit is triggered three time consecutivly within 60 s since the last trigger, the battery shuts down and requires intervention to recover. Host cycle the battery to bring it back to operational staten++see [Recovery from Power save mode](../battery_states/power_save.htm#Recovery2).

After recovering the battery, revise your MiR application to prevent the current limit from being exceeded again.

You can see how many times the limit has been exceeded under Monitoring > Hardware health > Battery Management System (BMS) > Overcurrent counter.

**Table 8.2**Current limits for revision 2 batteries

Function

Trigger currentDelay

Overcurrent discharge protection 1

112 A

419 ms

Overcurrent discharge protection 2

188 A

20 ms

Overcurrent discharge protection 3

55 A

12 s

Overcurrent discharge protection 4 (non-recoverable fuse blow)

55 A

15 s

Short circuit protection

400 A

90 n++s

Overcurrent charge protection 1

36 A

419 ms

## Temperature

For recommended ambient temperature, see [Electrical voltage, current, and temperature limits](../limits/current_limits.htm).

**Table 8.3**Temperature limits for revision 2 batteriesDescriptionTrigger

Reaction

ReleaseCell discharge over temperature Over 70 n++C

Cannot power robot

Under 60 n++C for 15 s

Cell discharge under temperature

Under -20 n++C

Cannot power robot

Over -15 n++C for 15 s

Cell charge over temperature

Over 55 n++C

Cannot charge

Under 45 n++C for 15 s

Cell charge under temperature

Under 0n++CCannot chargeOver 3 n++C for 15 s

Severe cell over temperature

Over 85 n++C

Battery unrecoverable

Severe cell discharge under temperature

Under -20 n++C while continous 500 mA current

Battery unrecoverable

Severe cell charge under temperature

Under 0 n++C for 5 s while continous 500 mA current

Battery unrecoverable