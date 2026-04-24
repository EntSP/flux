# Safety configuration file {% tag="safety_configuration_file" %}

{% partial file="partials/safety/list_applied_safety_config_and_required_sw_version.md" /%}

{% partial file="partials/safety/text_checksum_description.md" /%}

The configuration file on your robot has the following checksums.

{% table %}

* Component
* Checksum {% if equals($base_robot, "MiR600/MiR1350") %}({% $mir600 %} / {% $mir1350 %}){% /if %}

{% if $checksum_safety_plc %}

---

* Safety PLC
* {% $checksum_safety_plc %}

{% /if %}

{% if $checksum_rear_scanner_function_network %}

---

* Rear scanner function and network
* {% $checksum_rear_scanner_function_network %}

{% /if %}

{% if $checksum_rear_scanner_function%}

---

* Rear scanner function
* {% $checksum_rear_scanner_function %}

{% /if %}

{% if $checksum_front_scanner_function_network %}

---

* Front scanner function and network
* {% $checksum_front_scanner_function_network %}

{% /if %}

{% if $checksum_front_scanner_function %}

---

* Front scanner function
* {% $checksum_front_scanner_function %}

{% /if %}

{% if $checksum_front_right_scanner_function_network %}

---

* Front right scanner function and network
* {% $checksum_front_right_scanner_function_network %}

{% /if %}

{% if $checksum_front_right_scanner_function %}

---

* Front right scanner function
* {% $checksum_front_right_scanner_function %}

{% /if %}

{% if $checksum_front_left_scanner_function_network %}

---

* Front left scanner function and network
* {% $checksum_front_left_scanner_function_network %}

{% /if %}

{% if $checksum_front_left_scanner_function %}

---

* Front left scanner function
* {% $checksum_front_left_scanner_function %}

{% /if %}


{% /table %}

## Checking the checksum

{% partial file="partials/safety/text_checksum_compare_requires_latest_safety_design.md" /%}

{% partial file="partials/safety/instructions_find_checksum.md" /%}