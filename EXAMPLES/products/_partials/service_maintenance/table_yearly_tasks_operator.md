{% table %}

* Parts
* Maintenance
* Symptoms of neglect

---

* Information stickers
* Check if the warning labels, identification label, and nameplate on the robot are still intact and visible.
* The labels are worn and unclear.

---

* Caster wheels and drive wheels
* Replace caster wheels and drive wheels yearly, regardless of wear.
* Unreliable docking performance. Skidding (loss of traction). Loss of localization or localization jumps. Failing to complete missions and driving patterns that previously worked fine.

{% if $has_esd_variant %}

---

* ESD capability
* Only relevant for ESD models. Check the robot's electrical resistance. If the resistance is above 1×10^9 Ω, clean the wheels and test the resistance again. If the resistance is still out of bounds, replace the drive wheels.
* Robot does not discharge static electricity.

{% /if %}

{% if $is_forklift %}

---

* Hydraulic oil
* Replace the hydraulic oil. The pistons must use Rando® HDZ-15 or an oil with similar properties.
* Excessive wear on system.

{% /if %}


{% /table %}