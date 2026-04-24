{% table %}

* Parts
* Maintenance
* Symptoms of neglect

---

* Safety marking on the floor
* Check if the safety markings around operating hazard zones are intact and visible.
* The markings are worn and unclear.

---

* Battery and assembly
* Clean the battery and the battery connection assembly with a clean, dry cloth.

    Verify the connection assembly operates smoothly.

    Check the battery for any signs of damage or misuse.

* The battery connection is unstable resulting in the robot losing power.

---

* Brake test
* Conduct a brake test as described in {% tagref tag="test_braking_distance" /%}.

    Adjust the environment, payload, or Protective field sets if necessary.

* Robot may have an increased or unverified braking distance.

---

* Caster wheels
* {% if $min_caster_wheel_diameter %}

    Measure the diameter of the wheels, and replace them if the diameter is less than {% $min_caster_wheel_diameter %} mm.
    {% /if %}

    {% if $min_cleanroom_caster_wheel_diameter %}
    If your robot has cleanroom wheels, replace if the diameter is less than {% $min_cleanroom_caster_wheel_diameter %} mm.
    {% /if %}

    Check bearings by pressing against them and rotating them to feel any internal wear or damage. Check for flat areas on the wheels. If a wheel has a noticeably flat area replace all wheels. Replace all caster wheels together.

* Robot cannot travel over large steps and gaps without scraping the bottom of the robot.

    Robot swerves more if the wheels are uneven sizes.

    Skidding (loss of traction).

    Loss of localization or localization jumps. Failing to complete missions and driving patterns that previously worked fine.

{% if $min_drive_wheel_diameter %}

* Drive wheels
* Measure the diameter of the wheels, and replace them if the diameter is less than {% $min_drive_wheel_diameter %} mm.

    Calibrate the IMU after replacing the drive wheels.

* Robot cannot travel over large steps and gaps without scraping the bottom of the robot.

    Robot swerves more if the wheels are uneven sizes. Localization becomes inaccurate due to inaccurately converted encoder data.

{% else / %}

---

* Drive wheel
* Check wheel surfaces for wear. Replace if needed.
* Robot cannot travel over large steps and gaps without scraping the bottom of the robot.

    Localization becomes inaccurate due to inaccurately converted encoder data.

{% /if %}

{% if $task_check_drive_wheels_shaft %}

---

* Inspect the drive wheel shaft nut
* Visually inspect that the drive wheel shaft nut and locking washer are properly aligned relative to the shaft.

    Replace if needed—see "How to replace the drive wheel shaft nuts on MiR600 and MiR1350".

* The robot does not drive straight and may report driving-related errors.

    The markings on the drive wheel nut and washer are unaligned relative to the marking on the shaft.

{% /if %}

{% if $is_forklift%}

---

* Support leg rollers
* Check bearings by pressing against them to feel any internal wear or damage. Check the support leg roller surfaces for wear. Replace both support leg rollers together if needed.
* Robot cannot travel over large steps and gaps without scraping the bottom of the robot.

    Robot swerves more if the support leg rollers are uneven sizes.

---

* Battery connector
* Check that the battery connector connects and disconnects smoothly—see Disconnecting the batteries section.
* The battery connector is loose or unable to connect or disconnect the batteries.

{% /if %}


{% /table %}