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
# Carts {% tag="carts" %}

A cart in the user interface is a description of a physical cart that MiR robots can pick up and place. You must define every individual cart that you want the robot to be able to transport.

A cart in the interface is used to provide the information MiR robots need to pick up, drive, and place the cart correctly. When you send the robot to a Cart position to pick up a cart, the robot scans the ID tag on the cart to link the corresponding cart description in the interface that describes the dimensions, calibrations, and docking offsets of the cart.

## Setup

Use the Setup page to calibrate the height of the hook and placement of the ID tag for a specific cart.

When you calibrate a cart, configure the hook so the gripper is attached to the cart gripping bar and is at the hook height you want while it tows the cart. Select **Calibrate cart** to make the robot automatically detect all the necessary values. The determined values are shown under **Advanced**.

<image: "setup.png">

| | Description | | Description | | --- | --- | --- | --- | | 1 | Robot to calibrate with Select a robot with a hook top module that you want to use to calibrate the cart. Place the robot in front of the cart and attach the cart to the gripper at the height you want the robot to transport the cart. You must control the robot and hook from the robot interface. | 2 | Name Enter the ID tag of the cart. The name must be the same as the string of the ID tag. This is used to identify the cart. | | 3 | Hook height Displays the current height of the hook. Adjust the value to move the hook up and down. | 4 | Hook gripper Displays the current state of the gripper. Use the drop-down to open and close the gripper. | | 5 | Hook brake Displays the current state of the hook brake. Use the drop-down to activate and deactivate the brake. When the brake is deactivated, the hook arm can swing freely. | | |

## Dimensions

Use the Dimensions page to specify how large the cart is. The robot uses this information to plan its paths so the cart does not collide with obstacles and to correctly reverse with the cart.

<image: "dimensions.png">

| | Description | | Description | | --- | --- | --- | --- | | 1 | Height Enter the highest point of the cart measured from the ground. | 2 | Length Enter the length of the cart from the gripper bar to the point furthest from the robot. | | 3 | Width Enter the width of the cart. | 4 | Locked wheels offset Enter the distance from the gripper bar to the locked wheels axis. |

## Advanced

Use the Advanced tab to see values that the hook detected when you ran the cart calibration. You can adjust these values if necessary.

<image: "advanced.png">

| | Description | | Description | | --- | --- | --- | --- | | 1 | ID tag The unique tag string. This is the text the ID tag reads when the hook scans it. | 2 | Entry height The hook height where the gripper can slide under the gripper bar.  | | 3 | Lock height The hook height where the gripper can attach to the gripper bar.  | 4 | Drive height The hook height where the robot can tow the cart.  | | 5 | ID tag offsets Values describing the position of the ID tag so the hook camera knows where to detect the tag. | | |