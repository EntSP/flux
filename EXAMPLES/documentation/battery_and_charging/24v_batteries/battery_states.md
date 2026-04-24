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
﻿# Power save

If the battery has been unused for a length of time dependent on various factors, it enters Power save mode. In this mode, the battery consumes minimal power making it ideal for long-time storage. In this mode, the battery cannot power the robot.

With firmware version 1.1.10, in the worst case, the battery can be left in Power save mode for one day before entering Deep sleep.

With firmware version 1.2.2 and higher, the battery can be left in Power save mode for at least 4.5 months before entering Deep sleep.

When you press the Power button and the battery is in this mode, the Power button does not light up, and the robot remains off.

For MiR500 and MiR1000, the Power button lights up blue when the robot is off. When the robot enters Power save mode, all lights in the control panel turn off.

{% image src="/images/accessories/batteries_chargers/states/buttons_deep_sleep.webp" alt="buttons deep sleep" /%}

## Entering Power save mode

There are three different ways the battery can enter Power save mode:

- If the battery is connected to a robot, and the robot is kept powered off, the battery enters Power save mode within a short period (typically 1-4 hours).

- When the robot is turned off manually (or automatically due to low power), the battery enters Power save mode within a longer period (typically after a week).

- If the robots has turned off multiple times due to low power because you keep turning it back on, eventually the battery will switch to entering Power save mode within a short period (typically 1-4 hours)

## Recovery from Power save mode

There are two Power save mode stages. The battery is in the first stage if the host voltage is above 36.4 V (FW 1.1.10), 42.3 V (FW 1.2.2n++1.2.6), or 41.4 V (FW 2.0.4n++2.1.0), and it is in the second stage if it is below these values.

The recovery procedure depends on which stage the battery is in:

- If the battery is in the first stage, host cycle the battery to bring it back to Low power or Operational mode. To do this, disconnect the battery for 30 seconds, reconnect the battery, wait 30 seconds, then turn on the robot.

Alternatively, connect a 48V cable charger directly to the battery using an adapter cablen++see [Adapter cable](../adapter_cable/adapter_cable.htm) n++, or connect a MiR Cable Charger Lite 48V 3A to the charging interfacen++see [Cable chargers](../cable_chargers/cable_chargers.htm).

- If the battery is in the second stage, connect a 48V cable charger directly to the battery using an adapter cable, or connect a MiR Cable Charger Lite 48V 3A to the charging interfacen++see [Cable chargers](../cable_chargers/cable_chargers.htm).

If you are unable to recover the battery by connecting a cable charger directly to the battery, it is possible the battery has entered Deep sleep. Use a MiR Cable Charger Lite 48V 3A to recover the batteryn++see [Recovery from Deep sleep](deep_sleep.htm#Recovery).