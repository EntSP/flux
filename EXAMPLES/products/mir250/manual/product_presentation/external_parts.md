# External parts {% tag="external_parts" %}
{% if equals($model, "MiR250") %}
{% image src="/images/mir250/overview/external_parts.webp" alt="Identification of the robots external parts."  /%}
{% else equals($model, "MiR250 Shelf Carrier") /%}
{% image src="/images/mir250/overview/external_parts_shelf_carrier.webp" alt="Identification of the robots external parts."  /%}
{% /if %}


{% table %}

* Pos.
* Description
* Pos.
* Description

---

* 1
* Corner bumper: four pcs., one on each corner
* 2
* Signal light: eight pcs., two on each corner—see {% tagref tag="light_indicator_and_speaker" /%}

---

* 3
* 3D depth camera: two pcs., both in the front—see {% tagref tag="obstacle_detection" /%}
* 4
* Caster wheel with foot guard: four pcs., one in each corner

---

* 5
* nanoScan3 safety laser scanner: two pcs., in opposite corners—see {% tagref tag="obstacle_detection" /%}
* 6
* Drive wheel: two pcs., one on each side of the robot

---

* 7
* Status light: on all four sides of the robot—{% tagref tag="light_indicator_and_speaker" /%}
* 8
* Proximity sensor: eight pcs., two in each corner behind corner covers—see {% tagref tag="obstacle_detection" /%}

---

* 9
* Control panel—see {% tagref tag="control_panel" /%}
* 10
* Manual brake release switch—see {% tagref tag="control_panel" /%}

---

* 11
* Nameplate
* 12
* Top cover

---
{% if equals($model, "MiR250") %}
* 13
* Antenna: two pcs., one on each top compartment cover
* 14
* Left top compartment—see {% tagref tag="internal_electrical_interfaces" /%}

---

* 15
* Right top compartment—see {% tagref tag="internal_electrical_interfaces" /%}

*
*

{% else / %}
* 13
* Carrier pin: two pcs.
* 14
* Emergency stop button: two pcs.



{% /if %}



{% /table %}