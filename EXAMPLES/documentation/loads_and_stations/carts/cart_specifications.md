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
# Cart specifications {% tag="cart_specifications" %}

This section describes the requirements for the carts that MiR robots can tow.

Figure 3.2 illustrates the dimensions that must be within a certain range. You must create and design your own cart type or purchase suitable carts that meet the design requirements.

The carts must have a gripper bar at the front, bottom part of the cart (typically a rectangular tube).

**Figure 3.2**Front view of a cart (left), and side view of a cart (right)

<image: "Cart\_specifications.png">

| Pos. | Description | Pos. | Description | | --- | --- | --- | --- | | A | Cart width: between 400 mm and 1 500 mm | B | Cart length: between 500 mm and 2 400 mm | | C | Cart height: maximum 1 800 mm | D | Distance between gripper bar and floor: 80 to 350 mm | | E | Gripper bar length: minimum 350 mm | F | Gripper bar width: between 15 mm and 25 mm |

For the robot to be able to locate and identify carts, an ID tag must be fixed on the front of the cart—see [ID tags](id_tags.htm).

To enable the robot to pick up a cart, you must define the cart in the interface.

## Wheel configuration of the cart

The carts must be fitted with two rigid and two swivel wheels. The two rigid wheels can either sit on the front or the back of the cart.

Whether the robot performs better towing a cart with rigid wheels on the front or the back depends on the maneuvering conditions on the individual site and should be assessed before the gripper bar is fixed.

### Two rigid wheels on the back and two swivels on the front

With this configuration, the turning radius of the robot and the cart is larger, but the driving is more stable. Reverse parking is easier.

### Two swivels on the back and two rigid wheels on the front

With this configuration, the turning radius of the robot and the cart is smaller, making it ideal for areas with tight corner passages.

## Payload

It is the responsibility of the commissioner to determine the safe total payload each cart type can support regardless of the robot's payload.

The exact payload limit depends on the cart design, payload distribution, application, and driving surface. The total payload should be determined during commissioning.

Determine the safe total payload for your cart application during commissioning.

  * Ensure that loads are correctly distributed and fastened to the robot.