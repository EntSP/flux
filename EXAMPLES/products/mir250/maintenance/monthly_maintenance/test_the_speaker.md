# Test the speaker {% tag="test_the_speaker" %}

<image: "mir250\_base\_robot\_test\_speaker.png">

## Purpose

To ensure that the robot can play warning sounds and other audible signals to inform the surroundings of its behavior or intention.

Frequency: **monthly**

To complete this task, the battery must be connected, and the robot must be turned on.

When performing maintenance, you risk electrical shock from exposed electrical wires, and crushing, collision, or pinching from unexpected movement.

* Be careful of exposed electrical wires.

* Avoid inserting your hands between actuators or other moving parts of the robot.

* Make sure the drive wheels are not in contact with the ground—see [Lifting the robot](../How to lift the robot.htm).

## Procedure

1. In the robot interface, go to **Setup > Sounds**.

2. Select a default sound from the list to open **Edit sound**.

<image: "maintenancen\_setup\_sounds.png">

3. Verify that Volume is set to 100%.

4. Select **Play on robot**.

<image: "maintenance\_edit\_sound.png">

5. Verify that the sound plays loud and clear with no distortion.

See a [video](https://vimeo.com/896164147) of the process on the Mobile Industrial Robots profile on vimeo.com.

## Pass criteria <image: "mmg\_pass.svg">

* The robot can play sounds from its internal speaker.

* There are no distortion or errors in playback.

## Remediation

{% table %}

* Issue
* Remedial action

---

* The robot does not play a sound when **Play on robot** is selected.

{% /table %}

* Verify that the sound works by selecting **Listen** in the **Edit sound** settings.
* Verify that the volume level for the sound that you are trying to play on the robot is set to an audible level in the **Edit sound** settings.
* See Troubleshoot MiR250 sound not working. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-replace/how-to-replace-the-speaker-on-mir250/). If no sound is playing still, the speaker is most likely damaged and should be replaced. See the guide How to replace the speaker on MiR250. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-replace/how-to-replace-the-speaker-on-mir250/).

The robot plays a sound, but the sound is distorted or sounds bad. |  Some speaker-related issues have been fixed in software updates. Make sure to update to the latest software version. If this does not help, the speaker is damaged and should be replaced. See the guide How to replace the speaker on MiR250. You can find this guide on [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/documentation/how-to-replace/how-to-replace-the-speaker-on-mir250/).