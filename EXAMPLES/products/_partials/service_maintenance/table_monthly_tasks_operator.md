{% table %}

* Part
* Maintenance
* Symptoms of neglect

---

* Robot hardware
* In the robot interface under **Monitoring > Hardware health**, check if there are any warnings (marked with yellow).
* Over time, a warning can become an error and will stop the robot from operating.

---

* Speaker and signal lights
* Check that all visual and auditory warnings function. Adjust or replace as needed.
* Speaker plays low or distorted sounds.

---

* Charging pads
* Using your hands, ensure that each pad moves up and down freely.

    Clean the charging pads on the robot and charging stations using sandpaper.

* Contamination collects on the charging pads or they become stiff.

    Connection to the charging station becomes less reliable and charging is less effective.

    Charging issues or poor connection with charging station.

{% if $has_broom %}

---

* Charging broom
* Clean the broom, and check that it is intact.
* Dust collects on the charging pads.

    Connection to the charging station becomes less reliable and charging is less effective.

    Charging issues or poor connection with charging station.

{% /if %}

---

* 3D cameras
* Check for visual defects, for example cracks and scratches.
* Robot navigates around non-existent obstacles or fails to detect obstacles.

{% if $is_forklift %}

---

* Drive wheel height screw
* Check that the Drive wheel height screw can lift the robot's drive wheel.
* The robot's brake distance increases, the robot is not able to drive automatically, or you are not able to push the robot.

{% /if %}

{% if $has_filter %}

---

* Air filter
* Check that the air filter is intact and clear of debris. Wash if needed. The filter needs to be completely dry before use. Replace if not intact.
* The robot overheats and shuts down in environments that are within the specified operating temperature.

{% /if %}

{% if $has_top_plate %}

---

* Top plate
* Check mounting. Ensure it sits evenly on top of the robot with connections accessible. Replace as needed.
* Robot, top module, or load become unstable. Damage to the plate increases.

{% /if %}


{% /table %}