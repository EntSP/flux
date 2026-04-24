# Compatible products

The following products can be used with {% $model %}:

## Charge 48V 35A and Charge 48V 105A

Charging station that enable MiR robots to recharge their batteries. Together with MiR Fleet, charging of robots can be fully automated, ensuring that robots never run out of power during missions.

The 105A variant can charge {% $mir1200_pallet_jack %} faster than the 35A variant. For deckload and hook robots, there is not difference in performance between the charging station types.

{% if include($compatible_products, $mir_fleet) %}

## {% $mir_fleet %}

MiR robots can be operated individually or as a part of a fleet. MiR Fleet is the compatible fleet manager for MiR robots. MiR Fleet offers centralized control of robots throughout all of your facility.

{% /if %}

{% if include($compatible_products, $mir_eu_pallet_rack) %}

## {% $mir_eu_pallet_rack %}

A MiR-specific pallet rack that enables MiR EU pallet lift robots to pick up and place EU pallets from the rack autonomously.

{% /if %}

{% if include($compatible_products, $mir_pallet_rack) %}

## {% $mir_pallet_rack %}

A MiR-specific pallet rack that enables MiR pallet lift robots to pick up and place US stan dard 40" × 48" pallets from the rack autonomously.

{% /if %}

{% if include($compatible_products, $mir_shelf_lift) %}

## {% $mir_shelf_lift %}

{% partial file="partials/product_properties/text_shelf_lift_carrier_description.md" /%}

{% /if %}

{% if include($compatible_products, $mir_shelf_carrier_250) %}

## {% $mir_shelf_carrier_250 %}

{% partial file="partials/product_properties/text_shelf_lift_carrier_description.md" /%}

{% /if %}

{% if include($compatible_products, $mir_eu_pallet_lift_600) %}

## {% $mir_eu_pallet_lift_600 %} and {% $mir_eu_pallet_lift_1350 %}

A lift top module that can be mounted on the robot enabling it to pick and place standard EPAL 1 pallets on pallet racks.

{% /if %}

{% if include($compatible_products, $mir_pallet_lift_600) %}

## {% $mir_pallet_lift_600 %} and {% $mir_pallet_lift_1350 %}

A lift top module that can be mounted on the robot enabling it to pick and place US standard 40"×48" pallets on pallet racks.

{% /if %}

{% notice type="info" %}
For more information about top modules from third parties, see MiRGo on [mobile-industrial-robots.com/products/mir-go](https://mobile-industrial-robots.com/products/mir-go).
{% /notice %}