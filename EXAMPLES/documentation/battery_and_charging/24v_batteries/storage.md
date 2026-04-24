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
﻿# Storage

The battery should be stored in an area at room temperature with a non-condensing relative air humidity and no direct sunlight. Temperatures and humidity below or above the specifications will shorten the service life of the batteryn++see [Storage temperature](#Storage1).

Charge the battery before storage, disengage the manual brake release, and disconnect the battery from the robot to preserve the service life of the battery.

The best state to store the battery at is when it is 80% charged. [Table 5.1](#Time) provides best practice values for storage time depending on the battery percentage. The storage time of the batteries depends on which firmware they are runningn++see [Firmware versions](firmware/FW_versions.htm).

**Table 5.1**
The maximum allowed storage time of the battery when disconnected from the robot

Battery

percentage

Maximum storage time

FW 1.1.10

FW 1.2.2n++1.2.6

FW 2.0.4n++2.1.0

75%15 months40 months

125 months

50%10 months24 months

85 months

25%5 months14 months

45 months

5%2.5 months3 months

12 months

0%

1 day to 1.5 month1When the robot first shuts down due to low power, the storage time is 1.5 months. You can still use the battery to power the robot briefly or to release the brakes, but this will reduce the storage time. Preventative measures against this have been introduced in firmware 1.2.2n++see Firmware versions.

14 weeks

6 months

If you store the battery at 0% for longer than the maximum storage time, the battery enters Deep sleep. To recover the battery, see [Recovery from Deep sleep](battery_states/deep_sleep.htm#Recovery).

If you cannot turn on the robot after connecting a battery that has been in storage, you can check if the battery is in Power save mode or Deep sleep by going through [Battery modes and troubleshooting them](troubleshooting/battery.htm#Operable).

## Storage temperature

The storage temperature affects the storage time of the battery. It is best to keep the battery at a temperature between 10 n++C and +20 n++C. [Table 5.2](#Approxim) quantifies the approximate affect of temperature on the storage time of the battery.

**Table 5.2**
Approximate temperature affect on storage timeTemperature rangeReduction of storage time10 n++C n++ 25 n++C0% (no change)25 n++C n++ 35 n++C20%35 n++C n++ 45 n++C80%45 n++C n++ 60 n++C95%