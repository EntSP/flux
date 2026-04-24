{% if $is_forklift %}

## Replace Every 5 Years

{% table %}

* Parts
* Maintenance
* Symptoms of neglect

---

* Temperature switch
* Replace to protect against overheating and to ensure the reliability of the robot's safety functions.
* The PLC may shut down due to overheating if the temperature switch is not functioning correctly. A noticeably high temperature and smell may be present in the electronics box. The robot will report a PLC communication error.


{% /table %}

{% /if %}

## Replace Every 20 Years

{% table %}

* Parts
* Maintenance
* Symptoms of neglect

---

* Emergency stop buttons
* Replace to ensure the reliability of the robot's safety functions.
* Pressing the Emergency stop button does not bring the robot into Emergency stop.

---

* Safety PLC
* Replace to ensure the reliability of the robot's safety functions.
* The robot begins reporting safety system errors.

---

* {% if $has_contactors %}STO and dynamic brake contactors{% /if %}{% if $has_mosfets %}STO and dynamic brake MOSFETs{% /if %}
* Replace to ensure the reliability of the robot's safety functions.
* The robot begins reporting errors.

---

* Mechanical brakes
* Replace to ensure the reliability of the robot's safety functions.
* The robot reports mechanical brake errors.

---

* Safety laser scanners
* Replace to ensure the reliability of the robot's safety functions. Replace as needed.
* The robot does not detect obstacles reliably and reports safety laser scanner errors.

---

* Manual brake release switch and control panel
* Replace to ensure the reliability of the robot's safety functions.
* The robot does not react to pressed buttons reliably or reports errors or false button states.


{% /table %}