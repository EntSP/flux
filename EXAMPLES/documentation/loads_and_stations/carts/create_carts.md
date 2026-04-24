---
id: "item-xxx"
type: "article"
title: ""
status: "review"
version: "1"
language: "en-us"
firstReleaseDate: "2025-11-04"
updateDate: "2025-11-04"
accessLevel: "public"
---
# Create carts {% tag="create_carts_and_marker_types" %}

Before creating missions with carts, you need to define the different carts that your robot will be docking to. This information is used when the robot is picking up, placing, and towing the cart to ensure that the cart is correctly transported.

To create a new cart, follow these steps:

  1. Go to Robot > Carts, and select Create.

  2. Under Setup you will calibrate the cart. Select a robot with a hook top module you want to use to calibrate the cart and enter the ID tag name of the cart you want to define.

To calibrate the cart, follow these steps:

     1. Open the robot interface for the selected hook robot, and enable manual control of the hook—see [Manual control](../../interface_guide_2.0/hook/manual_control/root.htm).

<image: "enable\_manual\_control.png">

     2. Move the hook arm to a height where the hook gripper can get under the cart gripper bar. This is known as the Entry height.

     3. Place the cart over the hook gripper.

<image: "Entry-height.png">

     4. Move the hook arm to a height where the hook gripper touches the cart gripper bar without lifting or pushing the cart. This step may require some trial and error until you have the correct height. This is known as the Lock height.

<image: "Lock-height.png">

     5. Place the ID tag of the cart where the hook camera can detect it.

<image: "calibrate\_cart.png">

     6. In the MiR Fleet interface, select **Calibrate cart**. The calibration values under **Advanced** will fill in automatically.

<image: "calibrate\_cart.png">

  3. Under Dimensions, enter the dimensions of the cart—see [Carts](../../mirfleet/features/cart.htm).

  4. Select Create when you are done. The cart is now displayed in the list of carts.

