{% table %}

* Part
* Maintenance
* Symptoms of neglect

---

* Safety laser scanners
* Check for visual defects, for example cracks and scratches.

    Replace as needed.

* The robot goes into unexpected Protective stops or navigates around non-existent obstacles.

    The robot reports contamination errors.

---

* Covers
* Check mounting. Ensure the covers are even and are not in contact with the wheels.

    If you replace the cover with the robot's nameplate, make sure to mount a new copy of the nameplate to the replacement cover.

* Covers hang loose, get scratched, do not protect the robot's internal parts, or are in contact with moving parts.

{% if $has_mehanical_brakes %}

---

* Mechanical brakes
* Check if the Manual brake release switch functions by releasing the brakes and pushing the robot gently forward.

    Confirm that the STO contactors have deactivated for the brakes. Go to **Monitoring > Hardware health > Safety system** - it should display "Robot is in Emergency stop (Manual Brake Release Switch)".

    Enable the brakes again when done.

* The mechanical brake system does not stop the robot or keep it in place at standstill.

{% /if %}

{% if $is_forklift %}

---

* Drip tray for hydraulic fluid
* Check if there is any fluid in the drip tray for hydraulic fluid. If there are any signs of leakage, contact MiR Technical Support. Hydraulic oil is hazardous waste and should be collected in a leak-proof container. Transport the oil to an authorized waste disposal facility.
* Lowering and raising the forks takes longer than normal or emits abnormal noises.

{% /if %}


{% /table %}