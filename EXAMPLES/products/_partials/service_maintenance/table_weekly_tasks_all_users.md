{% table %}

* Parts
* Maintenance

---

* Outer covers
* Clean the robot on the outside with a damp cloth. Do not use compressed air to clean the robot.

---

* Status lights
* Check if the LED light band is intact. Ensure the light shows all the way around the robot. Clean with a soft cloth to ensure even lighting around the robot.

---

* Signal lights
* Check if the signal lights blink and show light correctly when the robot is moving.

---

* Safety laser scanners
* Clean the optics covers of the scanners for optimum performance. Avoid aggressive or abrasive cleaning agents.

    Site conditions may affect the needed cleaning frequency. If the operating environment is very dusty, cleaning the safety laser scanners may be needed more often.

    Clean the side and top part of the optics cover. The contamination sensors scan the entire optics cover glass piece. In the robot interface under **Monitoring > Hardware health > Safety system > Emergency stop**, see if **Laser (Front) Contamination Error** and **Laser (Back) Contamination Error** is **False**.

    Static charges cause dust particles to be attracted to the optics cover. You can diminish this effect by using anti-static plastic cleaner.

---

* Antennas
* Check that the antennas are properly attached in their sockets.

{% if $proximity_sensors %}

---

* Proximity sensors
* Check for dust or dirt, and clean with a swab.

{% /if %}

{% if $is_forklift %}

---

* Ultrasonic sensor, Blue light, 3D cameras, and 3D LiDAR
* Check for dirt or visual defects, for example cracks and scratches. Clean with an anti-static microfiber cloth. Site conditions may affect the needed cleaning frequency. If the operating environment is very dusty, cleaning the safety laser scanners may be needed more often.

{% /if %}


{% /table %}