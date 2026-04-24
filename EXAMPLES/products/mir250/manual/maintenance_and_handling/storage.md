# Storage {% tag="storage" %}

The main component affected by storage are batteries. Monitor the robot's battery percentage before and during storage to prevent damage from undercharging.

## Preparing the robot for storage

When taking the robot out of operation:

* Charge the robot 80% battery percentage. This is the optimal state of charge for batteries.
* Store the robot in an area at room temperature and humidity according to the robot specifications—see {% tagref tag="specifications" /%}. Temperatures and humidity below or above the specifications will shorten the service life of the battery.
* Disconnect the main battery connector—see {% tagref tag="power_connection" /%}. Keeping batteries connected to robots greatly reduces the storage time.
* Protect batteries immediately after removing them from a robot. Never allow any moisture or foreign particles to get into a battery. If you store a battery outside the robot, you can protect it by storing it in a well-ventilated area to prevent moisture build-up and water logging.
* Check the battery percentage of the robot regularly. Charge the robot if the battery percentage is low. Always disconnect batteries after checking or charging them.

## Storage time

Storage duration depends on the battery's charge state, storage conditions, and version. For the expected storage time for new 48V batteries, see _MiR 48V Battery Technical Guide_ on the [MiR Support Portal](https://supportportal.mobile-industrial-robots.com/).

{% partial file="partials/power/notice_battery_storage_damage.md" /%}

## Battery modes

{% table %}

* Battery percentage
* Mode
* Reactivation method

---

* Low or unused for extended period
* Power save mode
*   * Disconnect battery for 30 seconds, reconnect, wait 30 seconds, then turn on robot.
    * {% if $location_charging_port %}Connect MiR Cable Charger Lite 48V 3A to the robot's charging interface while the batteries are connected to the robot.{% else / %} Connect a 48V cable charger directly to the battery while the battery is disconnected from the robot, or connect MiR Cable Charger Lite 48V 3A to the robot's charging interface while the battery is connected to the robot.{% /if %}

---

* Critically low
* Deep sleep mode
* May be revivable using MiR Cable Charger Lite 48V 3A, depending on duration in Deep sleep.


{% /table %}

{% partial file="partials/references/info_battery48v_technical_guide.md" /%}