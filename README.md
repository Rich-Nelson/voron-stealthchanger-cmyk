# Voron Stealthchanger CMYK

[![Voron Stealthchanger CMYK — Watch on YouTube](images/video-thumbnail.png)](https://www.youtube.com/watch?v=wOfLphvfhsM)

This repo contains all of the custom files for my 6-toolhead multi-material 3D printer, which is based on a [Voron 2.4](https://github.com/VoronDesign/Voron-2) using the [StealthChanger](https://github.com/DraftShift/StealthChanger) toolchanging system, and the [Tapchanger docking mechanism](https://github.com/viesturz/tapchanger). The build prioritizes performance, maintainability, auto calibration, and aesthetics. The CMYK in the name reffered to my printer color scheme, it's a nod to the subtractive primary colors used by 2D printers and to the capabilities of a multi tool 3D printer especially with slicer advancement like full spectrum color.

Each tool head uses a Dragon Burner toolhead with a Sharkpa Mini Extruder and TZ 2.0 V6 hotend, chosen for their combination of print quality and cost-effectiveness. The entire build is made from 3D printed parts and off-the-shelf hardware.

This repo documents all of the custom and modified components.

## Cost Estimate Guide

A common question is: **"How much does this build cost?"** It can be tricky to answer since it depends heavily on your base printer and which components you choose.

To help estimate costs, it's best to break the project down into three high-level categories:

1. **Base Printer Cost**: The cost of your Voron 2.4 (or similar) printer and any fundamental upgrades needed to get it running.
2. **Base Toolchanger Cost**: The shared components needed to convert the printer, such as the StealthChanger motion components, umbilical backplate, nozzle brush mount, calibration switches (Sexball probe), and any mainboard upgrades to support multiple CAN toolboards.
3. **Multiplier Costs (Per Toolhead)**: The cost of a fully functional toolhead plus its dock and umbilical line. Multiply this by the number of tools you plan to run (e.g., x6 for this CMYK build). This includes:
   - Toolhead components (hotend, extruder kit, stepper motor, toolboard, probe kit, fans, hardware).
   - Toolhead Dock (printed parts and hardware).
   - Umbilical assembly (umbilical brackets, CAN cable, PTFE tube, connectors).

*(Optional Add-ons)*: Calculate separately items like the custom spool holder, dryboxes, or an enclosure.

You can reference the [BOM.csv](BOM.csv) and the individual component READMEs (such as the [Dragon Burner Toolhead hardware table](dragonburner-toolhead-cowl/README.md#hardware)) for specific pricing and source links as a starting point.

![Voron Stealthchanger CMYK](images/voron24-stealchanger-cmyk.png)

---

## Components

### [Toolhead Dock](dock/)

![Toolhead Dock](images/toolhead-dock-assembly.PNG)

A three-part honeycomb dock, that uses the tapchanger screw hook docking mechanism. The design includes a built-in brush holder for an optional silicone nozzle wipe on every dock and undock.

---

### [Umbilical Backplate](umbilical-backplate/)

![Umbilical Backplate Assembly CAD](images/umbilical-backplate-assembly-cad.png)

A backplate as the single disconnect point for all six toolhead umbilicals. CAN bus cables connect via GX12-4 jacks and filament guide tubes via ECAS04 quick-connect collets, providing a straight low-friction filament path and quick disconnect capabilities for maintenance.

---

### [Umbilical Bracket](umbilical-bracket/)

![Umbilical Bracket](images/umbilical-bracket-cad.PNG)

Custom brackets that bundle the CAN bus cable, PTFE filament guide tube, and flat spring steel into a flexible, organized umbilical cable assembly. The brackets clamp firmly to the cable while allowing the tube and spring steel to move freely. Spring steel is used only at the start and end of each umbilical for the ideal balance of structure and flexibility.

---

### [Spool Holder](spool-holder/)

![Spool Holder](images/spool-holder-cad.png)

A compact, adjustable spool holder sized to fit within the width of the 300mm Voron 2.4 printer. Built from 2020 aluminum extrusion with roller carriages that slide along two threaded rods, accommodating different spool widths. Designed to be enclosed later and used used as a dry box.

---

### [Dragon Burner Toolhead Cowl](dragonburner-toolhead/)

![Dragon Burner Toolhead Assembly](dragon-burner-toolhead-assembly.png)

A custom cowl for the [Dragon Burner](https://github.com/chirpy2605/voron/tree/main/V0/Dragon_Burner) toolhead to dock configured with a Sharkpa Mini Extruder and TZ 2.0 V6 hotend. Produces good print quality while remaining budget-friendly.

---

### [Nozzle Brush Mount](nozzle-brush-mount/)

![Nozzle Brush Mount](images/nozzle-brush-mount-cad.png)

Mounts a silicone brush and a Sexball probe to a 2020 extrusion. The brush automatically cleans the nozzle during docking; the probe runs automatic XYZ nozzle offset calibration across all six tool heads with a single button press.

---

### [Toolchange Tuning](toolchange-tuning/)

Tuned motion parameters and dock path waypoints to reduce toolchange time. Covers changes to `printer.cfg` and StealthChanger macro configs, including a trimmed 4-waypoint dock path that removes the high-Z ramp-in from the default.


