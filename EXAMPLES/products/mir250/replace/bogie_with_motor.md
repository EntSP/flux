---
id: "item-xx"
type: "article"
document_number: 300092
title: "Replace bogie with motor"
status: "review"
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
- "bogie"
- "motor"
- "oil"
files: []
products:
- "MiR250"
order_number: "450312 (right side bogie) and 450346 (left side bogie)"
hwVersionRobot: "All"
---

# Bogie with motor {% tag="replace_bogie_with_motor_mir250" %}


<image: "motor\_and\_bogie.png">

Failure to use appropriate personal protective equipment (PPE) can result in serious injury.

Determine relevant and necessary PPE based on the task, environment, and experience of personnel. The following is a list of common PPE you must consider:

  * Safety shoes to protect from impact or puncture hazards.

  * Safety glasses and face shield to protect from flying debris or chemical agents.

  * Hard hat to protect from falling or flying objects.

  * Gloves to protect against sharp objects, electrical hazards, chemical agents, and extreme temperatures.

  * Ear plugs or earmuffs to protect from high noise hazards.

  * Dust mask or respirator to protect from inhaling chemical agents or other harmful airborne hazards.

Electrical components can be damaged by electrostatic discharge. Consider moving the robot to an ESD protected area and using ESD protected clothing and tools.

The spare part for this robot is heavy. Before performing the replacement, make the necessary arrangements to ensure a safe work environment.

## Things you will need

  * A new motor and bogie for MiR250

  * Support blocks to keep the robot lifted

  * A lever or lift jack to lift the robot

  * A piece of cloth

  * Circlip pliers

  * A T10 screwdriver

  * A 10 mm wrench

  * A 3 mm hex key

  * A torque wrench ranging from 1.7–15 Nm with the following exchangeable bits:

    * PZ1

    * T30

    * T45

## Before replacing the bogie with motor

Note down the total distance the robot has driven. You can find this in the robot interface on the default dashboard under Moved. MiR may ask you for this information if we request the motor for analysis.

  1. Push the two buttons on the rear cover, and remove the cover from the robot.

<image: "rear\_press\_buttons.png"> <image: "rear\_remove.png">

  2. Disconnect the battery.

     * Hardware 1.0 only

Turn the Battery lock pin clockwise, and pull the Battery lever down. Confirm that a gap opens between the battery and the battery connector as the handle is pulled down. Turn the Battery lock pin counterclockwise to lock the Battery lever.

<image: "unlock\_battery\_connected.png"> <image: "disconnect\_battery.png">

     * Hardware 2.0 and higher only

Pull the Battery lock pin out while pulling the Battery lever down. Confirm that a gap opens between the battery and the battery connector as the handle is pulled down.

<image: "250\_mkII\_disconnect\_battery.png">

  3. Place the robot on a stable work surface at a comfortable working height.

  4. Remove the two screws in the front cover, and remove the cover from the robot. Use a T30 bit.

<image: "front\_unscrew.png"> <image: "front\_remove.png">

  5. Remove the screws in the side covers, and remove the covers. Use a T30 bit.

<image: "side\_unscrew.png"> <image: "side\_remove.png">

  6. Remove any top modules mounted to the robot.

  7. Remove the top plate:

     1. Unscrew the antennas from the top compartment covers and remove them.

<image: "antenna\_unscrew.png">

     2. Unscrew the two nuts from the antenna connectors. Use an 8 mm wrench. Push the antenna connectors through the covers.

<image: "antenna\_bolt\_unscrew.png">

     3. Remove the top compartment covers from the top plate by unscrewing the eight screws. Use a T10 bit. Make sure the antenna cables are not connected to the compartment covers.

<image: "top\_unscrew.png">

     4. Remove the top plate from the robot by unscrewing the four screws. Use a T45 bit. Make sure the antenna cables are not connected to the top plate.

When reassembling, reuse the screws and washers, and tighten the screws to 7.5 Nm.

<image: "remove\_top\_cover\_all\_covers.png"> <image: "remove\_top\_cover\_no\_ends.png">

## Disconnecting the cables

  1. Disconnect the six motor wires from the SS1 contactor on the side where you are replacing the motor (K3 on the right side and K4 on the left side). To disconnect the wires, follow these steps:

     1. Loosen the three screws in the contactor to release the wires. Use a PZ1 bit.

<image: "unscrew\_motor\_screws.png">

     2. Take a picture of the wires, and remove the wires from the contactor.

The wires are labeled according to which terminal they connect to. In case any wires are mislabeled or the label has fallen off , use the picture you took to ensure that the wires are connected to the same terminals. Tighten the screws to 1.7 Nm when connecting the wires.

<image: "unplug\_motor\_cables.png">

     3. On top of the contactor, unscrew the first screw, and disconnect the green wire.

<image: "unplug\_k4\_wires.png">

  2. In the front compartment, disconnect the encoder signal cables for the motor you are replacing. The cables are labeled **Right** (1 in the following image) and **Left** (2 in the following image) to identify which motor they are connected to.

<image: "encoder\_connectors\_2.png">

  3. Disconnect the following three cables from the motor controller carrier board depending on which motor you are replacing.

     * For the right side motor

<image: "right\_side\_cabels.png">

     * For the left side motor

<image: "left\_side\_cabels.png">

  4. Loosen the four screws in the front corner bumper on the side with the bogie you are replacing. Use a T30 bit.

<image: "control\_panel\_screws.png">

  5. Screw in the black set screw, and lift the corner bumper. Use a 3 mm hex key.

<image: "push\_release\_pin.png"> <image: "pull\_up\_bumper.png">

  6. Pull the cables through the bumper compartment. Start with the three small motor controller carrier board cables, and pull the encoder signal cable through last. The encoder signal cable has a larger connector that may damage the other cables if pulled through first.

<image: "pull\_cables\_through\_bumper.png">

## Removing the bogie and motor

  1. Using a crowbar, lift jack, or other lever tool, lift the bogie from the ground, and place a block beneath the front of the chassis to keep the front caster wheels raised from the ground.

     1. Apply the lever or lifting device on the rear edge of the bogie to raise the bogie. Make sure to place a cloth between the lever and the bogie to avoid damaging it.

<image: "lift\_bogie.png">

     2. Once the drive wheel is lifted so it touches the top of the chassis, push support blocks beneath the front of the chassis. Push blocks in on both sides of the robot to ensure the front of the chassis is fully supported.

<image: "lift\_bogie\_2.png">

     3. Release the bogie so it lowers again. The front wheels are now raised from the ground.

<image: "lift\_bogie\_3.png">

  2. If your robot has a traction kit installed, remove the traction kit by following the mounting instructions in reverse. See the guide _How to install the MiR250 traction kit_. You can find this document on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com).

<image: "traction\_kit.png">

  3. Remove the circlip on the bogie axle using the circlip pliers. The circlip keeps the bogie mounted to the axle.

     * Make sure the bogie arm is supported so it does not slide off the axle and causes damage to the cables or robot components.

     * Avoid overstretching the circlip so you can reuse it when mounting the bogie arm back on the robot.

<image: "remove\_circlip.png">

  4. Remove the spacer disk behind the circlip.

<image: "remove\_disk.png">

  5. Pull the bogie arm off the axle. Gently place the bogie next to the robot without pulling the cables forcefully.

Never remove both bogies from the robot at the same time. If you remove both bogies, the rod between them will fall in the robot, and you cannot correctly remount the bogies without disassembling the robot completely.

<image: "remove\_bogie.png">

  6. Pull the motor cables through the cable hole, starting with the small cables and ending with the encoder signal cable.

<image: "cable-hole\_out.png">

  7. Check that there are no other cables connected to the motor that are still connected to the robot. If so, disconnect any forgotten cables, and remove the bogie from the robot completely.

## Replacing the bogie and motor

  1. Lead the encoder signal cable of the new motor through the cable hole, followed by the other three motor cables.

<image: "cable-hole\_in.png">

  2. Gently, push the new bogie onto the bogie axle. If the axle is pushed into the robot, push the axle back in place from the opposite side of the robot. You may need a second person to help you by pushing against the other side of the bogie axle.

<image: "place\_bogie.png">

  3. Place the spacer disk on the end of the bogie axle and reattach the circlip.

<image: "place\_circlip.png">

  4. Lead the encoder signal cable of the new motor through the cable hole, followed by the other three motor cables.

<image: "pull\_cables\_through\_bumper\_2.png">

  5. Reconnect the cables to the motor controller carrier board and encoder connector—see step 2 and step 3 under Disconnecting the cables.

  6. Reconnect the wires to the SS1—see step 1 under Disconnecting the cables.

  7. Gently lower the corner bumper and ensure that no cables are pinched between the corner and the frame. Screw in the four screws. Tighten the screws to 8 Nm.

  8. Reassemble the robot and reconnect the battery by following the steps in Before replacing the bogie with motor in reverse.

## Document history

{% table %}

 * Version
 * Date
 * Description
 ---
 * 1.6
 * 2025-04-24
 * Added missing order number for left side bogie.

---

 * 1.5
 * 2024-08-14
 * Added warning on use of appropriate PPE. Added ESD notice. Added notice on considering the weight of the bogie. Updated styling throughout the guide.

---

 * 1.4
 * 2024-05-08
 * Added notice to not remove both bogies at the same time.

---

 * 1.3
 * 2023-11-27
 * Updated style and corrected reference to right and left encoder cables.

---

 * 1.2
 * 2021-06-01
 * Updated for new Support site.

---

 * 1.1
 * 2021-05-27
 * Changed "black pin" to "set screw" when lifting the corner bumper.

---

 * 1.0
 * 2020-02-05
 * First edition.

{% /table %}

how-to\_troubleshooting/PDF/how\_to/replace/\_How to replace the bogie with motor on MiR250 1.0\_en.pdf