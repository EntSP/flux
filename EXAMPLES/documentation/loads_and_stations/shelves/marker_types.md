---
id: "item-xxx"
type: "article"
title: ""
status: "published"
version: "1"
language: "en-us"
firstReleaseDate: "2025-11-04"
updateDate: "2025-11-04"
accessLevel: "public"
---
# Marker types {% tag="marker_types" %}

A marker type is a description of a shelf that MiR robots can dock to. You must have a marker type for each type and size of shelf you want your robot to be able to transport.

A marker type is used to provide the information MiR robots need to dock to a shelf correctly. When you send the robot to a Shelf position to pick up a shelf, you must also select the marker type corresponding to the shelf.

<image: "parameters.png">

| | Description | | Description | | --- | --- | --- | --- | | 1 | Name Enter a name for the marker type. | 2 | Shelf type Select the shelf marker type you want to create. Bar-markers are for MiR100 and MiR200. Leg-markers are for MiR250, MiR500, MiR600, MiR1000, and MiR1350.  | | 3 | Orientation offset Enter the orientation offset in degrees.  | 4 | X-offset Enter the marker type's X-offset. This modifies how far forward the robot drives to dock to the shelf.  | | 5 | Y-offset Enter the marker type's Y-offset. This modifies how far to either side the robot drives to dock to the shelf.  | 6 | Bar length For Bar shelf markers: Enter the length of one of the side bars. The side bars are to the left and right sides of the robot. For Leg shelf markers: Enter the distance between a pair of legs on one side of the robot.  | | 7  | Bar distance Enter the width of the area under the shelf where the robot can dock. For Bar shelf markers: Enter the distance between the side bars. The side bars are to the left and right sides of the robot. For Leg shelf markers: Enter the distance between a pair of legs on opposite sides of the robot.  | | |