# Field switching and Personnel detection {% tag="field_switching_and_personnel_detection" %}

{% partial file="partials/safety/warning_drive_over_feet_wear_safety_shoes.md" /%}

{% partial file="partials/functions_features/text_personnel_detection_field_switching_description.md" /%}

{% imagegrid %}

{% gridimage image="/images/graphical/safety_system/Personnel_detection_clear.webp" alt="Robot driving freely" headline="Clear ahead" bodytext="The robot drives when the area is clear." /%}

{% gridimage image="/images/graphical/safety_system/Personnel_detection_blocked.webp" alt="Robot stopping for obstacle" headline="Obstacle detected" bodytext="The robot stops when it detects an obstacle." /%}

{% /imagegrid %}

{% partial file="partials/sensors/text_scanner_tolerance_distance.md" /%}

## Protective fields when driving forward

{% partial file="partials/functions_features/text_personnel_detection_table_field_size_description.md" /%}

{% table %}

* Case
* Speed
* Front field length (_L_)
* Field width (_W_)
* Rear field length (_R_)

---

* 1
* 0.00 to 0.30 m/s and less than 15 deg/s
* 385 mm
* 170 mm
* 110 mm

---

* 2
* 0.00 to 0.30 m/s
* 385 mm
* 210 mm
* 110 mm

---

* 3
* 0.30 to 0.50 m/s and less than 15 deg/s
* 495 mm
* 170 mm
* 110 mm

---

* 4
* 0.30 to 0.50 m/s
* 495 mm
* 210 mm
* 110 mm

---

* 5
* 0.50 to 0.90 m/s
* 805 mm
* 210 mm
* 110 mm

---

* 6
* 0.90 to 1.30 m/s
* 1 245 mm
* 210 mm
* 110 mm

---

* 7
* 1.30 to 1.70 m/s
* 1 915 mm
* 210 mm
* 110 mm

---

* 8
* 1.70 to 2.10 m/s
* 2 855 mm
* 210 mm
* 110 mm


{% /table %}

{% image src="/images/mir250/protective_fields/forward_field_sets.webp" alt="The forward field sets of the robot."  /%}

## Protective fields when driving backward

{% partial file="partials/functions_features/text_personnel_detection_table_field_size_description.md" /%}

{% table %}

* Case
* Speed
* Rear field length (_L_)
* Field width (_W_)
* Front field length (_F_)

---

* 9
* 0.10 to 0.30 m/s and less than 15 deg/s
* 235 mm
* 170 mm
* 105 mm

---

* 10
* 0.10 to 0.30 m/s
* 235 mm
* 210 mm
* 105 mm

---

* 11
* 0.30 to 0.50 m/s and less than 15 deg/s
* 345 mm
* 170 mm
* 105 mm

---

* 12
* 0.30 to 0.50 m/s
* 345 mm
* 210 mm
* 105 mm

---

 * 13
 * 0.50 to 0.90 m/s
 * 655 mm
 * 210 mm
 * 105 mm

---

 * 14
 * 0.90 to 1.30 m/s
 * 1 095 mm
 * 210 mm
 * 105 mm


{% /table %}

{% image src="/images/mir250/protective_fields/reverse_field_sets.webp" alt="The reverse field sets of the robot."  /%}

## Protective fields when pivoting or at standstill

{% partial file="partials/functions_features/text_personnel_detection_table_field_size_description.md" /%}

{% table %}

 * Case
 * Pivot speed
 * Front and rear field length (_L_)
 * Field width (_W_)

 ---

 * 15
 * 0 to 15 deg/s
 * 105 mm
 * 170 mm

---

 * 16
 * 15 deg/s or more
 * 105 mm
 * 210 mm


{% /table %}

{% image src="/images/mir250/protective_fields/pivot_field_sets.webp" alt="The field sets of the robot when it pivots or stands still."  /%}

## Muted Protective fields

{% partial file="partials/functions_features/text_mute_protective_fields_description.md" /%}

{% partial file="partials/safety/warning_muted_protective_field_areas_must_be_marked_as_operating_hazard_zones.md" /%}

{% partial file="partials/functions_features/list_mute_protective_field_behavior.md" /%}

## User-configured muting of the Protective fields

{% partial file="partials/functions_features/instructions_mute_protective_field_mission.md" /%}

{% partial file="partials/functions_features/instructions_mute_protective_field_manual_mode.md" /%}

## Pre-configured muting of the Protective fields

{% partial file="partials/functions_features/text_mute_protective_fields_pre_configured.md" /%}

{% partial file="partials/references/info_markers_docking_undocking.md" /%}