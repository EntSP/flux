# Connect to the web-interface{% tag="connect_to_interface" %}

When the robot is turned on, you can connect a PC or tablet to the robot's internal network to access the web-interface. In the web-interface, you can configure the robot's settings and connect it to a wireless network.

{% if $has_inbuilt_display %}You can also control and configure the robot directly using the display—see {% tagref tag="control_panel" /%}. {% /if %}

## Connect to network

You can connect to the robot using an Ethernet cable or an access point. If you are located in North America, the EU, or a part of the EAC, you can purchase a MiR Access Point from MiR. Outside these areas, you need to use your own access point that is approved for use in your region. If you choose to use an access point, you must ensure that the robot is disconnected from the wireless network before attaching the access point to remain compliant—see {% tagref tag="connect_to_wi-fi_network" /%}.

{% if not($has_power_over_ethernet_service_port) %}The RJ45 Ethernet port does not support Power over Ethernet. If you connect an access point to the robot, you must connect another cable to power the access point.
{% / if %}

It is recommended that your device is configured to DHCP. If you require a static IP on your device, assign an address above 192.168.12.150, and set the DNS server and Gateway address to 192.168.12.1.

{% partial file="partials/wi-fi/warning_multiple_radio_modules.md" /%}

## Access web-interface

To connect to the robot web-interface, follow these steps:

1. Locate the RJ45 Ethernet port.

    {% if equals($location_ethernet_service_port, "left rear compartment") %}
    The Ethernet port is in the left rear compartment.
    {% else equals($location_ethernet_service_port, "front right corner")/ %}
    The Ethernet port is in the front right corner.
    {% else equals($location_ethernet_service_port, "rear compartment")/ %}
    The Ethernet port is in the rear compartment.
    {% /if %}

    {% image src=$image_ethernet_port alt="Ethernet port location" /%}

2. Connect your device directly to the robot using an Ethernet cable, or connect an access point to the Ethernet port for a wireless connection.
3. If you are using an access point, connect your device to the access point. The MiR Access Point Wi-Fi has the following format: MiR\_3042XXXXX. Use the password shipped with the access point to connect.
4. In a browser, go to the address 192.168.12.20 and sign in.