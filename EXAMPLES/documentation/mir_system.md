---
id: "item-xx"
type: "article"
title: "MiR system"
status: "published"
version: "1"
language: "en"
firstReleaseDate: "2001-01-01"
updateDate: "2025-07-21"
accessLevel: "public"
tags:
- "overview"
- "system"
- "fleet"
- "network"
---

# MiR system {% tag="mir_system" %}

A MiR system can consist of many MiR products and compatible modules. The base MiR components are:

  * MiR robots with top modules to automate various tasks.
  * MiR charging stations to charge robots between tasks.
  * MiR Fleet for centralized control to manage robot tasks, charging, and traffic.

MiR Fleet and MiR robots must be connected to the same network and communicate over Wi-Fi or 5G—see [Meet system requirements](../mirfleet/4.0_installation/requirements.htm).

## MiR robots

Use MiR robots as a mobile base for any compatible top module. Design or purchase a top module suited for the task you want your MiR application to execute, then program missions to define the tasks your MiR robots will execute.

Each robot has its own network that you can connect the robot's top module or other devices to. You can use the following methods to enable communication between a robot and its top module:

  * The [MiR Top Module API](../api/tm/top_module_root.htm)
  * I/O modules using 24V signals through the top compartment interfaces
  * Modbus
  * Safety interfaces, intended for safety-related communications

## MiR Fleet

MiR Fleet offers centralized control of robots on the same network. It is intended to manage all communication from users and integration systems to MiR robots.

You can operate and set up your MiR system using the web-based user interface. Your entire site is set up, stored in, and shared with robots through MiR Fleet. MiR Fleet can also handle limited traffic and resource management, assign scheduled missions to suitable robots, evacuate robots in case of emergencies, and automatically send robots to charging stations and staging areas. You must define and program all behaviors you want MiR Fleet to apply.

To integrate external systems into your MiR system, use MiR Fleet Integration API with MiR Fleet—see [MiR Fleet Integration API](../api/fleet/fleet_root.htm).

MiR Fleet **cannot** :

  * Manage other vehicles than MiR robots.
  * Act as a warehouse management system.
  * Collect and analyze historical data. This is done in MiR Insights instead or through custom external integrations—see [Monitor system](../manuals/commissioning/monitoring.htm).

## MiR charging stations

MiR Fleet sends any robots that are not running missions to the nearest MiR charging station. This keeps robots charged and ready for future missions.

MiR Charge 24V is compatible with MiR100 and MiR200.

All 48V charging station models are compatible with MiR250, MiR500, MiR600, MiR1000, MiR1350, and MiR1200 Pallet Jack. The 105A model charges MiR1200 Pallet Jack faster than the 35A model. For all other robots, the charging speed is the same regardless of the charger model.

## External systems

Integrate any number of additional systems and devices. Use the API options to set up communications to the MiR system—see [APIs and integration](../api/api_root.htm).