---
id: "item-xxx"
type: "article"
title: "Pallet transfer stations for MiR Pallet Jack"
status: "published"
version: "1"
language: "en-us"
firstReleaseDate: "2025-11-04"
updateDate: "2025-11-04"
accessLevel: "public"
---

# Pallet transfer stations for MiR Pallet Jack {% tag="pallet_transfer_stations" %}

MiR1200 Pallet Jack can pick up and place pallets from four different station types: floor positions, MiR pallet racks, custom stations, or floor conveyors. The requirements and setup for these stations are described in the following sections.

For the basic space requirements for docking to pallets and pallet stations, see  the [MiR1200 Pallet Jack specifications](https://supportportal.mobile-industrial-robots.com/specifications/mir1200-pallet-jack/mir1200-pallet-jack-specifications/) on MiR Support Portal. For pallets on the floor, the robot can approach using the left or right Entry position and detect the pallet with its side camera. This requires less space in front of the pallet. If the robot docks to a raised pallet station, it must dock from the front Entry position.

The space required in front of the station will increase if you move an Entry position further from the position, or you use a Bar-marker that is longer than the pallet.

The following configurations are **not** supported:

  * Stations where the robot can pick up the pallet and drive through the station. The robot must undock from the station by driving forward.

  * Stations where the robot can pick up or place pallet at different heights.

  * Stations where the pallet is placed higher than 85 cm from the ground.

  * Stations where the marker is offset from the expected pallet position. Pallet must be placed in the center of a marker.

  * The robot cannot pick up pallets where the **Fork entry height** is between 9–33 cm—see [Pallet position setup](create_positions.htm#Setting). In this interval, the forks block the rear scanner from detecting the pallet. The robot can still place pallets at these heights.

If you cannot avoid placing pallets at these heights, you can configure your robot to have a **Fork entry height** below 9 cm, and then raise the forks over 33 cm with the **Relative pallet pickup height**. This requires that the forks can enter from the floor, and raise 33 cm without being blocked.

## Pallet on floor

<image: "pallet\_marker.png">

If you make the robot handle pallets on the floor:

  * The robot docks to the pallet itself. You do not need to install any additional markers.

  * The robot cannot pick up or place pallets with closed pockets from the floor.

  * There are three Entry positions the robot can use to dock to the pallet. This means the robot can approach and detect the pallet from the side.

  * You can use the Pallet position with the height set to **Floor** directly in the interface without additional configuration—see [Pallet position setup](create_positions.htm#Setting).

## MiR pallet rack

<image: "pallet\_rack.png">

If you make the robot use either MiR Pallet Rack, MiR EU Pallet Rack, or a custom rack with the same dimensions:

  * The robot docks to the pallet rack. You do not need to install any additional markers.

  * Both MiR forklift robots and MiR pallet lift robots can handle pallets from the same rack.

  * There is one Entry position the robot can use to dock to the rack, so the robot must approach the rack from the front.

  * You must manually configure the Pallet position with the appropriate Entry height and pickup height—see [Pallet position setup](create_positions.htm#Setting).

## Custom rack or conveyor

<image: "vl\_marker.png"> <image: "bar\_marker.png">

If you make the robot use a custom rack, conveyor, or other pallet station:

  * There must be a VL-marker or Bar-marker the robot can use to position itself correctly. The marker must meet the basic marker design requirements—see [Markers](https://supportportal.mobile-industrial-robots.com/support-files/manuals/HTML/en/sw4_documentation/Content/manuals/commissioning/markers.htm) in _MiR Fleet Enterprise Documentation_.

    * Use VL-markers to make the robot place pallets accurately. This also requires that pallets are placed within ±2 cm of the center of the marker for the robot to be able to pick it up.

    * Use Bar-markers in setups where there is more variation in the pallet placement. Pallets must be placed within ±4 cm of the center of the marker for the robot to be able to pick it up.

  * If you use a VL-marker:

    * The V part of the marker must be placed at the center of where you want the pallet to be placed, with a tolerance of ±2 cm

    * The marker must extend 4 cm to the left of the V part of the marker. The right side must meet general VL-marker requirements—see [Markers](https://supportportal.mobile-industrial-robots.com/support-files/manuals/HTML/en/sw4_documentation/Content/manuals/commissioning/markers.htm) in _MiR Fleet Enterprise Documentation_.

    * The edge of the marker must align with the edge of the pallet, with a tolerance of ±10 cm.

    * There must be at least 10 cm clearance below the marker for the support legs to enter.

    * The VL-marker must be at least 10 cm tall.

<image: "vl\_marker\_pallet\_station.png">

  * If you use a Bar-marker:

    * The distance between the bars must be either 80 cm or 100 cm (±5 cm). If you use other dimensions, you must adjust the SICK configuration file accordingly—see [Contour lines for custom racks and conveyors](adjusting_field sets.htm#SICK con).

    * The length of the markers must be between 80–200 cm. We recommend using a length of 120 cm to match the length of the pallet.

    * The Bar-marker must be placed so the pallet is in the center of the marker, with a tolerace of ±4 cm.

<image: "bar\_marker\_pallet\_station.png">

  * The station must be able to support the payload of the heaviest load.

  * Pallets must be placed within 1.4 cm of the edge so the robot can get its forks fully under the pallet.

  * When the robot places pallets, the pallet is still stable when placed ±15° from the expected placement. When the robot undocks, the forks can push the pallet slightly and tilt its position.

  * There must be mechanical end stops on the conveyor or rack. The forks may drag the bottom of the pallet while undocking. The end stops must prevent the pallet from being dragged off the edge of the station.

  * There is one Entry position the robot can use to dock to the rack, so the robot must approach the rack from the front.

  * You must manually configure the Pallet position with the appropriate Entry height, pickup height, and marker definitions—see [Pallet position setup](create_positions.htm#Setting).

## Floor conveyor

<image: "bar\_marker\_floor.png">

If you make the robot use a floor conveyor:

  * There must be a Bar-marker the robot can use to position itself correctly on the outer sides of the conveyor. The marker must meet the basic marker design requirements—see [Markers](https://supportportal.mobile-industrial-robots.com/support-files/manuals/HTML/en/sw4_documentation/Content/manuals/commissioning/markers.htm).

  * The rollers may not be taller than 10 cm, otherwise they will block the scanner.

  * The distance between the bars for the Bar-marker must be 100 cm (±5 cm). If you use other dimensions, you must adjust the SICK configuration file accordingly—see [Contour lines for custom racks and conveyors](adjusting_field sets.htm#SICK con).

  * The length of the markers must be between 80–200 cm. We recommend using a length of 120 cm to match the length of the pallet.

<image: "bar\_marker\_floor\_conveyor\_station.png">

  * The station must be able to support the payload of the heaviest load.

  * For the robot to pick up pallets, the pallet must be placed within ±4 cm of the expected position relative to the marker and Pallet position.

  * When the robot places pallets, the pallet is still stable when placed ±15° from the expected placement. When the robot undocks, the forks can push the pallet slightly and tilt its position.

  * There must be mechanical end stops on the conveyor. The forks may drag the bottom of the pallet while undocking. The end stops must prevent the pallet from being dragged off the edge of the conveyor.

  * Pallets must be placed within 1.4 cm of the edge so the robot can get its forks fully under the pallet.

  * There is one Entry position the robot can use to dock to the rack, so the robot must approach the rack from the front.

  * You must manually configure the Pallet position with the appropriate Entry height, pickup height, and marker definitions—see [Pallet position setup](create_positions.htm#Setting).

## Safety

Consider the following risks when designing, installing, and operating with load transfer stations designed for MiR1200 Pallet Jack:

  * The robot cannot detect objects or personnel behind the marker it uses to dock to. When personnel perform maintenance or other tasks behind the marker, assess if there are any risks if the robot uses the load transfer station while personnel are behind the marker and cannot be detected. Consider covering the marker while undergoing maintenance to prevent the robot from using the station.

  * When the robot docks, the Protective fields do not extend to the end of the robot's forks. There is a risk of collision with personnel or objects inside the loading area.

  * Robots are not able to detect if a pallet is already placed on a pallet rack, shelf, or conveyor. There is a risk of the robot pushing the pallet off while trying to place a new pallet. The Check postion status action can only be used to check for pallets on the floor.

  * If the robot picks up a pallet with closed pockets, never let the robot lower the pallet to the bottom position of the forks. The bottom support beams will block the robot from lowering to the bottom and may cause the load to tip or become unstable.