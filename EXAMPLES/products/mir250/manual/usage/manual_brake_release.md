# Manual brake release {% tag="manual_brake_release_switch" %}

The Manual brake release switch is located below the control panel. You release the robot's mechanical brakes by turning the Manual brake release switch clockwise.

{% image src=$image_activate_manual_brake_release  /%}

The mechanical brakes require electrical power to be released. The robot must be connected to its battery power source to release the brakes—see {% tagref tag="power_connection" /%}.

When the robot is driving, the robot engages and releases the mechanical brakes automatically. You should only release the brakes manually when you want to move the robot by hand. The robot cannot operate automatically while the mechanical brakes are released manually.

When you release the brakes manually, all power to the motors is cut. This means the robot loses connection to certain components, including sensors used for localization.  If the robot is running software 3.6.1 or higher, the software localizes the robot's position based on the scanner data alone. On older software versions, you must localize the robot manually if you move it while the brakes are released.