{% notice type="caution" %}

Connecting an unsupported device to the Power interface can damage the robot or result in injury to personnel from electrocution or burns.

* Do not connect power and ground signals to the chassis.
* Do not stack the 24 V and 48 V power supplies.
* Do not connect 48 V power supplies to 24 V pins or vice versa.
* Do not connect a top module that can deliver an inverse current to the robot interfaces.
* Ensure connected devices do not have a capacitance of more than 2 000 µF combined from pins 1 and 3. If they do, integrate a softstarter that keeps the current under 2 A for the first 100 ms.
* Ensure connected devices do not draw more than {% $max_current_power_pins_1_and_3_driving %} A combined from pins 1 and 3 while the robot is driving.
* Ensure connected devices do not draw more than {% $max_current_power_pins_1_and_3_standstill %} A combined from pins 1 and 3 while the robot is at standstill.

{% /notice %}