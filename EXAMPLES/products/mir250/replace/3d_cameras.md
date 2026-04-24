---
id: "item-xx"
type: "article"
document_number: 300091
title: "Replace 3D cameras"
status: "published"
version: "1"
language: "en"
firstReleaseDate: "2001-01-01"
updateDate: "2025-07-21"
accessLevel: "public"
tags:
- "mir250"
- "manual"
- "maintenance"
- "hardware"
- "replace"
- "camera"
- "D435"
files: []
products:
- "MiR250"
order_number: 450314
hwVersionRobot: "All"
---

# 3D cameras {% tag="replace_3d_cameras_mir250" %}

<image: "Intel D435\_camera.png">

Failure to use appropriate personal protective equipment (PPE) can result in serious injury.

Determine relevant and necessary PPE based on the task, environment, and experience of personnel. The following is a list of common PPE you must consider:

  * Safety shoes to protect from impact or puncture hazards.

  * Safety glasses and face shield to protect from flying debris or chemical agents.

  * Hard hat to protect from falling or flying objects.

  * Gloves to protect against sharp objects, electrical hazards, chemical agents, and extreme temperatures.

  * Ear plugs or earmuffs to protect from high noise hazards.

  * Dust mask or respirator to protect from inhaling chemical agents or other harmful airborne hazards.

Electrical components can be damaged by electrostatic discharge. Consider moving the robot to an ESD protected area and using ESD protected clothing and tools.

This guide describes how to replace one of the 3D cameras on MiR250 with a revised spacer plate that provides more support for the camera connector. This reduces the likelihood of the connection to the camera getting loose over time.

## Things you will need

  * Loctite 2400 threadlocking adhesive, or other adhesive with same properties—see [Loctite 2400 specifications](https://www.henkel-adhesives.com/dk/en/product/threadlockers/loctite_2400.html)

  * A 0.3 Nm torque wrench with a 5.5 mm hex head

## Kit contents

  * 1 × Intel D435 camera

  * 1 × camera spacer plate

  * 4 × 2 mm nylon screw insulators

  * 2 × M3 lock nuts

  * Large cable ties

## Disconnecting the battery

  1. Push the two buttons on the rear cover, and remove the cover from the robot.

<image: "rear\_press\_buttons.png"> <image: "rear\_remove.png">

  2. Disconnect the battery.

     * Hardware 1.0 only

Turn the Battery lock pin clockwise, and pull the Battery lever down. Confirm that a gap opens between the battery and the battery connector as the handle is pulled down. Turn the Battery lock pin counterclockwise to lock the Battery lever.

<image: "unlock\_battery\_connected.png"> <image: "disconnect\_battery.png">

     * Hardware 2.0 and higher only

Pull the Battery lock pin out while pulling the Battery lever down. Confirm that a gap opens between the battery and the battery connector as the handle is pulled down.

<image: "250\_mkII\_disconnect\_battery.png">

## Removing the front cover

  1. Remove the two screws in the front cover, and remove the cover from the robot. Use a T30 bit.

<image: "front\_unscrew.png"> <image: "front\_remove.png">

## Replacing the camera

  1. Disconnect the USB-C cable from the top of the camera you want to replace. If you have a newer revision of the camera mount, cut the cable tie fixing the cable to the camera spacer plate.

<image: "unplug\_camera\_cable.png">

  2. Unscrew the two lock nuts behind the camera mount, and discard them along with the screw insulators.

<image: "unscrew\_camera.png">

  3. Remove the camera from the robot and discard it.

<image: "remove\_camera.png">

  4. Assemble the new camera. On the two threaded shafts, first slide on two new nylon screw insulators from the kit, and then the camera spacer plate. Make sure that the spacer plate is rotated so the support flange is on the same end as the socket for the USB-C cable and that when mounted on the robot, the support flange is facing inwards.

<image: "assemble\_camera\_1.png"> <image: "assemble\_camera\_2.png">

  5. Place the new camera on to the camera mount on the robot. Make sure to face it so the USB-C socket is facing upwards.

<image: "place\_camera.png">

  6. Apply threadlocking adhesive to the two new lock nuts from the kit.

Loctite and many other threadlocking adhesives are toxic substances that can cause skin, eye, throat, or digestive tract irritation to personnel upon contact, inhalation, or ingestion.

     * Read the safety data sheet for the adhesive product before applying it.

     * Avoid direct contact with the adhesive.

     * Apply the adhesive in a well-ventilated area.

  7. Behind the camera mount, slide on the two remaining screw insulators from the kit, followed by the lock nuts. Tighten the lock nuts to 0.3 Nm.

<image: "screw\_in\_camera.png">

  8. Connect the USB-C camera cable to the top of the camera, and use a cable tie to fix the connector to the support flange. Make sure the cable tie supports the cable, but does not pull it unnecessarily taut. The support is intended to ensure that the cable stays securely connected to the camera.

<image: "plug\_in\_camera\_connector\_1.png"> <image: "Apply\_cable\_tie.png">

  9. Reassemble the robot, and remove the plastic protective film from the camera.

## Testing

To test the new camera, see the guide _How to test if the 3D cameras are working on MiR robots._

## Document history

{% table %}

 * Version
 * Date
 * Description
 ---
 * 1.2
 * 2025-06-17
 * Fixed typos. Updated styling.

---

 * 1.1
 * 2022-02-23
 * Corrected the size for the hex head under Things you need.

---

 * 1.0
 * 2022-02-22
 * First edition.

{% /table %}

how-to\_troubleshooting/PDF/how\_to/replace/\_How to replace the 3D cameras on MiR250 1.0\_en.pdf