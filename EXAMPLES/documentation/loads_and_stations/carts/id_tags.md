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
# ID tags {% tag="id_tags" %}

An AprilTag or a QR code is needed for the robot to identify the individual carts. We recommend using AprilTags.

AprilTags and QR codes cannot be activated on the same site.

## AprilTags

Hook robots can be set to read AprilTags instead of QR codes. AprilTags are conceptually similar to QR codes. However, they are designed for high localization accuracy by encoding far smaller data payloads, allowing them to be detected more robustly and from longer ranges. When using AprilTags, the robot still picks up and places carts the same way as with QR codes, but the detection is more robust and faster.

**Figure 3.3** Example of an AprilTag

<image: "apriltag2.png">

The recommended size of an AprilTag is 80 × 80 mm. The system accepts any other sizes between 80 mm to 300 mm. When you use a large sized tag, the real limit is whether the camera can see the AprilTag or not.

It is required that at least 25 mm of empty white space surrounds the AprilTag.

The tag size is a global parameter so all tags used by the robot must have the same sizes if they are in the same site.

AprilTags can be generated in different patterns and classified in different tag families. Tag family 36h11 has 587 unique IDs and is the only supported tag family. When the robot is identifying carts, the ID of the AprilTag is used as the name of the tag as well as the cart. The ID could, for example, be _apriltag6_.

You can enable AprilTags and adjust the supported AprilTag size under **Hook > Settings > Advanced Hook > Use AprilTags instead of QR markers**.

<image: "activate\_apriltags.png">

## QR code

The QR code contains the dimension of the marker and a unique name.

The format is SizeUnit-Name.

  * Size: The length of one of the sides of the quadratic QR code.

  * Unit: The measuring-unit of the size, for example, mm (millimeters) or in (inches).

  * “-”: Remember the hyphen - which separates size and unit from the name.

  * Name: A unique name displayed in the system.

**Figure 3.4** This QR code reads 75mm-Cart\_A

<image: "qr.png">

The recommended size of a QR marker is between 70 and 100 mm, but the system is open to all other sizes. The limit is whether the camera can see the QR marker or not.

It is required that at least 25 mm of empty white space surrounds the QR code.

QR markers can be created using any QR code generator. As long as the size is the same as stated in the QR code, there are no requirements for how to create the codes. An easy and free method is to search the internet for QR code generators and use one of the many results.

Be sure to print a QR marker in 1:1 scale. If it does not match the size, it will not work.

It is recommended to use less than 17 characters in the QR code. For example, 75mm-Cart\_A is 11 characters long. If more than 16 characters are added, the QR code will change format, and it will become more difficult to detect.