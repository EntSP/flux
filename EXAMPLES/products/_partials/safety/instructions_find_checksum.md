To find the current checksums, follow these steps:

1. Connect to your robot's network as described in {% tagref tag="connect_to_interface" /%}.
2. Open SICK Safety Designer.
3. Select **Search for devices**.

    {% image src="/images/other_screenshots/safety_designer/search_devices.webp" alt="Search for devices in the SICK Safety Designer tool."  /%}

4. Drag all devices from the Device search window to the corresponding device in the Device overview window.

    When you are prompted to upload to the safety PLC, select No.

    {% image src="/images/other_screenshots/safety_designer/add_devices.webp" alt="Add devices to the active workspace."  /%}

    You can now read the current checksum values for each device configuration. If the values differ from the ones in Table 7.1, the safety configuration file has been modified from the original.

    {% image src="/images/other_screenshots/safety_designer/checksum.webp" alt="The checksum values of the current configuration."  /%}