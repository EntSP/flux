# Obstacle detection {% tag="obstacle_detection" %}

{% partial file="partials/navigation/text_detects_obstacles_while_driving.md" /%}

{% partial file="partials/sensors/list_sensors_for_obstacle_detection.md" /%}

{% notice type="info" %}

For more information about the sensors and obstacles detection, see {% tagref tag="deckload_robot_technical_guide" /%}.

{% /notice %}

## Safety laser scanners

The safety laser scanners provide a full 360° obstacle detection plane around the robot. The scanners are positioned 200 mm from the ground.

{% image src="/images/graphical/sensors/scanner_fov_deckload.webp" alt="Top view of the robot with a 360° obstacle detection plane around the robot."  /%}

{% partial file="partials/sensors/list_scanner_limitations.md" /%}

{% partial file="partials/sensors/text_scanners_used_in_safety_system.md" /%}

{% partial file="partials/sensors/warning_robot_detection_limitations_voids_overhangs_glass.md" /%}

## 3D cameras

The 3D cameras detect objects within the following field of view in front of the robot:

* Vertically up to 1800 mm at a distance of 1200 mm in front of the robot.
* Vertically in an angle of 54.5° from the ground.
* Horizontally in an angle of 114° and 250 mm to the first view of ground.

{% image src=$image_camera_fov alt="The field of view of the 3D cameras."  /%}

From the floor plane, the robot does not detect objects below 30 mm from the ground. This value increases by 10 mm per meter from the robot.

{% image src=$image_camera_bottom_limit alt="The ground limit of the camera field of view. "  /%}

{% partial file="partials/sensors/caution_cameras_are_not_safety_rated.md" /%}

{% partial file="partials/sensors/list_camera_limitations.md" /%}

## Proximity sensors

The proximity sensors detect low objects around the corners of the robot outside the field of view of the safety scanners and 3D cameras.

{% image src=$image_proximity_sensors_fov alt="Visualazition of the area the proximity sensors detect obstacles."  /%}

The main purpose of the proximity sensors is to detect low objects, such as pallets and forklift forks, placed close to the robot while it is standing still. When the robot begins to drive, it plans a path around the nearby detected obstacles.

{% notice type="info" %}
The proximity sensors are disabled by default. To make the robot use the proximity sensor data, you must enable the sensors and calibrate them. For more information, see the guide _How to calibrate the proximity sensors_.
{% /notice %}

The proximity sensors have the following limitations:

* They do not have a long range and are mainly used to detect obstacles placed near the robot while it is standing still and begins driving.

* They only detect low obstacles around the corners of the robot.

* When the robot is driving, obstacles detected by the proximity sensors are too close for the robot to stop or avoid. The robot relies on the laser scanners and 3D cameras to detect obstacles while it is driving.

* The effectiveness of the proximity sensors may be influenced by the shape, material, reflectivity, and color of obstacles.