
{% table %}

* Parts
* Maintenance

---

{% if $is_forklift %}

* Caster wheels, drive wheel, and support leg rollers
* Remove dirt with a damp cloth, and make sure nothing is entangled in the wheels or rollers.

{% /if %}

{% if $is_deckload %}

* Caster wheels (the four corner wheels)
* Remove dirt with a damp cloth, and make sure nothing is entangled in the wheels.

    Check that the wheels spin freely and do not emit grinding noises.

    Check that all bolts and screws are tight.

---

* Drive wheels (the two middle wheels)
* Remove dirt with a damp cloth, and make sure nothing is entangled in the wheels.

    {% if $task_grease_drive_wheels %}
    Wipe away any grease that may have leaked from the roller bearings.
    {% /if %}

{% /if %}


{% /table %}