---
id: "item-0006"
type: "product_note"
title: "MiR250 hardware version 2.0"
status: "published"
version: "1"
language: "en"
firstReleaseDate: "2024-07-30"
updateDate: "2024-07-30"
accessLevel: "public"
tags:
- "mir250"
- "manual"
- "maintenance"
- "hardware"
files: []
products:
- "MiR250"
- "MiR250 Shelf Carrier"
---


# Hardware version 2.0 {% tag="Hardware_version_2-0_mir250" %}

{% table %}

 * Date
 * 2023-07-06
 ---
 * Label
 * Hardware release

---

 * Product
 * MiR250 hardware version 2.0

---

 * Released by
 * Odin Skovsted

{% /table %}

## Description

We are now releasing a new hardware version of MiR250 that improves the quality and reliability of the MiR250 platform. Hardware version 2.0 replaces the existing MiR250 hardware version 1.0 robots.

Going forward, all base robot variants will be shipped as MiR250 hardware version 2.0. MiR250 Hook and MiR250 Shelf Carrier variants will first ship as hardware version 2.0 within the next months.

MiR250 hardware version 2.0 robots are supported only on software version 2.14.2 or higher and are incompatible with any software version below 2.14.2. If you purchase MiR250 hardware version 2.0 and want to add it to MiR Fleet, you must update your fleet to software 2.14.2 or higher.

The hardware update includes the following changes:

  * The router is replaced with an Ethernet switch—see Ethernet switch.

  * The corner of the robot with the control panel is improved.

  * The main cable harness is improved.

  * The motor controller carrier board is updated with a new version.

  * The STO and SS1 contactors are replaced with a version better designed for their installation in MiR250.

  * The Ethernet cable connecting the power board to the switch is moved out of the cable harness, making it easier to replace.

  * The safety PLC uses a new safety configuration file that is more user-friendly. The new files are not backwards compatible, and hardware version 2.0 does not support older configuration files.

  * For the standard MiR250 (100016) and the MiR250 ESD variant (100018), the new safety configuration file has updated default Protective fields. Furthermore, the password for the SICK Safety System that enables modifications to the SICK configuration is no longer included with the robot. The password will be provided by MiR Technical Support upon request. See _How to create a technical support ticket_ on MiR Support Portal.

  * The default safety configuration on the MiR250 Dynamic (100023) and the MiR250 ESD Dynamic (100025) is identical to the one on the standard MiR250 robot (100016). This change has been made to ensure the robots fully meet international safety standards when shipped from MiR. The default safety configuration can be replaced with a Dynamic if required.

The above changes have the following behavioral impact on the robot:

  * The robot does not and cannot broadcast a Wi-Fi connection you can use to connect to its internal network—see Ethernet switch.

  * You must use an Ethernet cable or an access point dongle to connect to the robot directly—see Connect with an Ethernet cable or an access point dongle.

  * There is a longer response time before the robot is brought out of Protective stop (same as with MiR600 and MiR1350).

  * The robot may lose its map localization if moved by hand using manual brake release. Re-localization must be done manually via the navigation software (same as with MiR600 and MiR1350).

  * The new default Protective fields for MiR250 standard base robot and the MiR250 ESD variant may mean changes to when obstacles will trigger a Protective stop. Furthermore, the robots will be slower at performing turns in narrow corridors.

  * For MiR250 Dynamic (100023) and MiR250 ESD Dynamic (100025), the new default safety configuration significantly changes the behavior and performance of the robots compared to hardware version 1.0. By replacing the robot's default safety configuration with the Dynamic configuration (also available on the robot), the behavior will change to match hardware version 1.0.

  * MiR250 hardware version 1.0 is not upgradeable to the new version 2.0.

## How to identify MiR250 hardware version 2.0

The order number for all MiR250 robots and compatible top applications remain the same, but the product and model serial numbers, and item numbers are changed. The identification label on MiR250 displays the hardware version of the robot—see [ID label locations](https://supportportal.mobile-industrial-robots.com/documentation/product-label-locations/id-label-locations) on MiR Support Portal. The hardware version is not visible in the robot interface.

The serial and item numbers of robot applications for MiR250 hardware version 2.0 are changed to those in the following tables.

The product serial number and item number are on the identification label and identify the MiR product. Each robot and each top module have an individual product serial number and item number.

The model serial number is on the nameplate and identifies the complete MiR robot application, covering both the base robot and the top module if one is mounted.

{% table %}

 * Model type
 * HW 2.0 product serial number
 * HW 2.0 item number
 ---
 * MiR250
 * 2060xxxxx
 * 800263

---

 * MiR250 with traction kit
 * 2061xxxxx
 * 800264

---

 * Model type
 * HW 2.0 model serial number

{% /table %}
---|---
MiR250 | 1025xxxxx
MiR250 Dynamic | 1026xxxxx
MiR250 ESD | 1027xxxxx
MiR250 Dynamic ESD | 1028xxxxx
MiR250 Shelf Carrier | 1029xxxxx
MiR250 Shelf Carrier ESD | 1030xxxxx
MiR250 Hook | 1031xxxxx

## Ethernet switch

MiR250 hardware version 2.0 is installed with an Ethernet switch instead of the previously used router.

We have made this change to easier comply with standards in specific markets and to make the connection between the robots and the company Wi‑Fi more stable.

When robots broadcast their own Wi‑Fi, it can interfere with the the company Wi‑Fi, especially if multiple robots are in the same area. This can lead to disturbances in the communication between the robots and MiR Fleet, which can cause slowdowns and stoppages. The new Ethernet switch does not broadcast its own Wi‑Fi, so it cannot interfere with the company Wi‑Fi.

The Ethernet Switch is located next to the battery in the same place as the router was located, and it has the same dimensions as the router.

## Connect with an Ethernet cable or an access point dongle

Because of the new Ethernet switch, you will not be able to connect wirelessly to a robot until it is connected to the Wi‑Fi on site.

Instead, you connect to the robot using either an Ethernet cable or an access point dongle via the RJ45 Ethernet port in the rear compartment next to the Battery lever.

<image: "ethernet\_port.png">

Once connected, you can configure the robot's settings and connect it to a wireless network in exactly the same way as before.

MiR offers a MiR Access Point that is compliant for use in North America, the EU, and some countries accepting EAC. Outside these areas, you need to use your own access point that is approved for use in your region. If you choose to use an access point, you must ensure that the robot is disconnected from the wireless network before attaching the access point to remain compliant.

If you are using an access point dongle, connect your device to the access point. MiR Access Point has the following SSID format: **MiR\_3042XXXXX**. Use the password shipped with the access point to connect.