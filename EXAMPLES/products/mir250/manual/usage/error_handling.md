# Error handling

The robot enters an error state when it can not solve a problem on its own. Some errors the robot clears and resolves itself, but for most errors the robot pauses operation until you clear the error.

To clear an error, select the red warning indicator in the interface, and select **Reset**.

When the robot stops because of an error, it also cancels its current mission. After clearing an error, make sure the robot completes the task it was assigned, especially if the robot was transporting a load and did not finish delivering it.

Errors include:

* Hardware faults
* Failed localization
* Failure to reach destination
* Unexpected events in the system
* Custom errors in missions that are defined with Throw error actions.

## Software errors

Software errors such as localization and failure to reach the goal destination can be prevented with the proper setup of maps and missions:

* Always test your missions under full observation and normal work environment conditions before leaving the robot to execute the missions autonomously.

* Use Try/Catch actions to make the robot react in a specific way if it fails to execute certain actions.

* Use Prompt user actions in missions that require intervention from users.

* Define Forbidden areas with Forbidden or Unpreferred zones on the map.

* Remove noise from maps.

* Create Directional or Preferred zones to guide the robot around areas that are difficult for the robot to travel through.

{% partial file="partials/references/info_commissioning_guidelines_best_practices.md" /%}

## Hardware errors

If the error is a fault in the hardware, either you will not be able to clear it, or the error will return until the fault is fixed. If this occurs, you can try to fix the issue with these actions:

* Turn your robot off and then on again. This resets the robot components and may resolve the issue.

* Check that all Emergency stop buttons are released.

* Check your robot for any physical damage such as cracks, dents, or severe scratches or contamination such as dust, dirt, and grease. Pay special attention to the 3D cameras, safety laser scanners, and drive wheel.

* Sign in to the robot interface, and go to **Monitoring > Hardware health**. The interface displays which component is failing and often for what reason. This can help identify the source of the error. If an internal component is failing, turn off the robot, disconnect the battery, and have the commissioner or operator visually check the internal component for obvious faults.