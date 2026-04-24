# Overspeed detection {% tag="overspeed_detection" %}

The Overspeed function makes the robot enter Protective stop and report an error if it drives or turns faster than pre-defined safety limits. This ensures the robot stops and enters a safe state before it becomes unstable or loses control while driving. Cases that can trigger this safety function are:

* Steep slopes
* Low-friction, wet, or dirty floors
* Hardware errors
* Unstable loads
* Loads that are not distributed as defined in {% tagref tag="payload_distribution" /%}.

If any speed limit is exceeded, the robot reports an error. You must clear the error and press the Restart button before the robot can continue operating.

{% if $is_deckload %}

{% table %}

* Case
* Limit

{% if equals($base_robot, "MiR250") %}

---

* Forward direction
* 2.075 m/s

{% else equals($base_robot, "MiR600/MiR1350") /%}

* Forward direction
* {% $mir600 %}: 2.10 m/s

    {% $mir1350 %}: 1.30 m/s

{% /if %}


---

* Reverse direction
* 1.30 m/s

---

* With muted Protective fields
* 0.30 m/s

---

* Pivoting
* 0.55 rad/s


{% /table %}
{% /if %}

{% if $is_forklift %}
{% table %}

* Turning angle
* Maximum reverse speed before Overspeed detection
* Maximum forward speed before Overspeed detection

---

* 0° to 15°
* 0.8 m/s
* 1.5 m/s

---

* 15° to 30°
* 0.8 m/s
* 1.1 m/s

---

* 30° to 90°
* 0.8 m/s
* 0.8 m/s


{% /table %}

When the robot is driving under one of the following conditions, the following limits apply for all driving directions:

* 0.5 m/s when controlling the robot with the tiller and the forks are above drive height.
* 0.3 m/s when the robot drives automatically and the forks are above drive height.
* 0.12 m/s when controlling the robot with the tiller and the tiller is in Home position.

'
{% /if %}
