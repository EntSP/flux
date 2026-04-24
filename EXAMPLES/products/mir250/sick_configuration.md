---
id: "item-xx"
type: "article"
title: "MiR250 SICK configuration files and compatibility"
status: "published"
version: "1"
language: "en"
firstReleaseDate: "2001-01-01"
updateDate: "2025-07-21"
accessLevel: "public"
tags:
- "mir250"
- "sick"
- "protective"
- "fields"
- "safety"
files: []
products:
- "MiR250"
- "MiR250 Shelf Carrier"
- "MiR250 Hook"
---

# SICK configuration files and compatibility {% tag="mobile_industrial_robots_mir250_sick_configuration_files_and_compatibility" %}

## MiR250 Base Robot SICK configuration files

{% table %}

 * Link and description
 * Robot HW
 * File version
 * Minimum SW
 * Validated scanner FW
 * Safety PLC checksums
 * Front scanner checksums
 * Rear scanner checksums
 ---
 * [MiR250_HW2-0_V2.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250_HW2-0_V2.sdp2) Support for hardware version 2.0. May turn slower in corners and takes longer to clear Protective stop.
 * 2.0 and higher
 * 2.0
 * 2.14.5  3.3.3
 * 1.94 1.93
 * 0x4A5D6A37
 * 0xBAD77FF8 0xAA20A7F8
 * 0xE82799E9 0xC13B42F7

---

 * [MiR250_v.22.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 v.22.sdp2) Resolved safety system errors when switching fields.
 * 1.0
 * 2.2
 * 2.10.5.5
 * 1.94 1.93
 * 0x64EA9F8F
 * 0x992D952E 0x577CF396
 * 0xD241347F 0x925E6700

---

 * [MiR250_v.21.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 v.21.sdp2) Resolved issues with Protective stop in charging stations.  Improved diagnostics.
 * 1.0
 * 2.1
 * 2.10.3
 * 1.93
 * 0xD45DDEA6
 * 0x3F8278CC 0xF1D31E74
 * 0x74EED99D 0x34F18AE2

---

 * [MiR250_v.19.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 v.19.sdp2) Resolved encoder errors.
 * 1.0
 * 1.9
 * 2.10.0
 * 1.93
 * 0x14A11BBC
 * 0xE7D06331 0x29810589
 * 0xACBCC260 0xECA3911F

---

 * [MiR250_v.18.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 v.18.sdp2) First version.
 * 1.0
 * 1.8
 * 2.8.3
 * 1.93
 * 0xE025554D
 * 0xE7D06331 0x29810589
 * 0xACBCC260 0xECA3911F

{% /table %}

## MiR250 Shelf Carrier SICK configuration files

{% table %}

 * Link and description
 * Robot HW
 * File version
 * Minimum SW
 * Validated scanner FW
 * Safety PLC checksums
 * Front scanner checksums
 * Rear scanner checksums
 ---
 * [MiR250_HW2-0_V3_Shelf.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250_HW2-0_V3_Shelf.sdp2) Support for hardware version 2.0. Takes longer to clear Protective stop. Larger Protective fields when driving with shelf and more agility when driving without a shelf.
 * 2.0 and higher
 * 3.0
 * 3.3.3
 * 1.94 1.93
 * 0x5AE8CE0C
 * 0xB0027EB6 0xC8DC095D
 * 0x97CCC47E 0xC699E939

---

 * [MiR250_HW2-0_V2_Shelf.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250_HW2-0_V2_Shelf.sdp2) Support for hardware version 2.0. Takes longer to clear Protective stop. Same behavior as hardware 1.0.
 * 2.0 and higher
 * 2.0
 * 2.14.5
 * 1.93
 * 0x8F272061
 * 0x81322FAD 0x4F634915
 * 0x69B92DF5 0x29A67E8A

---

 * [MiR250_v.22_shelf.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 Shelf Carrier v.22.sdp2) Resolved issues with Protective stops from nearby robots.  Resolved safety system errors when switching fields.  Updated IP addresses for scanners.
 * 1.0
 * 2.2
 * 2.10.5.5
 * 1.94 1.93
 * 0xF48650A7
 * 0x81322FAD 0x4F634915
 * 0x69B92DF5 0x29A67E8A

---

 * [MiR250_v.21_shelf.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 Shelf Carrier v.21.sdp2) Resolved issues with Protective stop in charging stations.  Improved diagnostics. Improved field sizes and carrier pins are operable with in Protective stop.
 * 1.0
 * 2.1
 * 2.10.3
 * 1.93
 * 0x4431118E
 * 0x063E6769 0xC86F01D1
 * 0x7752E649 0x374DB536

---

 * [MiR250 v.19_shelf.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 Shelf Carrier v.19.sdp2) First version.
 * 1.0
 * 1.9
 * 2.8.3
 * 1.93
 * 0xA92934FE
 * 0xDE6C7C94 0x103D1A2C
 * 0xAF00FDB4 0xEF1FAECB

{% /table %}

## MiR250 Hook SICK configuration files

{% table %}

 * Link and description
 * Robot HW
 * File version
 * Minimum SW
 * Validated scanner FW
 * Safety PLC checksums
 * Front scanner checksums
 * Rear scanner checksums
 ---
 * [MiR250_HW2-0_V2_Hook.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250_HW2-0_V2.sdp2) Support for hardware version 2.0. Takes longer to clear Protective stop.
 * 2.0 and higher
 * 2.0
 * 2.14.0  3.3.3
 * 1.94 1.93
 * 0xE9B1C0B6
 * 0xC3533C60 0xD1C0CD1C
 * 0xED6C9239 0x4E85EC4F

---

 * [MiR250 Hook v.22.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 Hook v.22.sdp2) Resolved safety system errors when switching fields.
 * 1.0
 * 2.2
 * 2.12.0.2
 * 1.94 1.93
 * 0xD77F58C8
 * 0xC3533C60 0xD1C0CD1C
 * 0xED6C9239 0x4E85EC4F

---

 * [MiR250 Hook v.21.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 Hook v.21.sdp2) First version.
 * 1.0
 * 2.1
 * 2.11.0
 * 1.93
 * 0x67C819E1
 * 0xC3533C60 0xD1C0CD1C
 * 0xED6C9239 0x4E85EC4F

{% /table %}

## MiR250 Dynamic SICK configuration files

{% table %}

 * Link and description
 * Robot HW
 * File version
 * Minimum SW
 * Validated scanner FW
 * Safety PLC checksums
 * Front scanner checksums
 * Rear scanner checksums
 ---
 * [MiR250_HW2-0_V2_Dynamic.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250_HW2-0_V2_Dynamic.sdp2) Support for hardware version 2.0.  Takes longer to clear Protective stop.
 * 2.0 and higher
 * 2.0
 * 2.14.0 3.3.3
 * 1.94 1.93
 * 0x20190115
 * 0x70FEEB65 0xBEAF8DDD
 * 0x3B924A34 0x7B8D194B

---

 * [MiR250 Dynamic v.22.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 Dynamic v.22.sdp2) Resolved safety system errors when switching fields.
 * 1.0
 * 2.2
 * 2.10.5.5
 * 1.94 1.93
 * 0x1A5FE017
 * 0x70FEEB65 0xBEAF8DDD
 * 0x3B924A34 0x7B8D194B

---

 * [MiR250 Dynamic v.21.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 Dynamic v.21.sdp2) Resolved issues with Protective stop in charging stations.  Improved diagnostics.
 * 1.0
 * 2.1
 * 2.10.3
 * 1.93
 * 0xAAE8A13E
 * 0xD6510687 0x1800603F
 * 0x9D3DA7D6 0xDD22F4A9

---

 * [MiR250 Dynamic v.19.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 Dynamic v.19.sdp2) Resolved encoder errors.
 * 1.0
 * 1.9
 * 2.10.0
 * 1.93
 * 0xC4882393
 * 0x0E031D7A 0xC0527BC2
 * 0x456FBC2B 0x0570EF54

---

 * [MiR250 Dynamic v.18.sdp2](https://mirwebsupportportalsa.blob.core.windows.net/largemirfiles/SICK files/MiR250 Dynamic v.18.sdp2) First version.
 * 1.0
 * 1.8
 * 2.8.3
 * 1.93
 * 0x19B22E85
 * 0x0E031D7A 0xC0527BC2
 * 0x456FBC2B 0x0570EF54

{% /table %}