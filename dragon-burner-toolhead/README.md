# Dragon Burner Toolhead Cowl

![Dragon Burner Cowl CAD](../images/dragon-burner-toolhead-assembly.png)

A custom cowl for the [Dragon Burner](https://github.com/chirpy2605/voron-user-mods/tree/main/Universal/DragonBurner) toolhead by chirpy2605. Configured with a Sharkpa Mini Extruder and TZ 2.0 V6 hotend, a combination selected after testing multiple setups for the best balance of print quality and cost.

There are also files for the EBB36 toolhead board cover that provides strain relief for the CAN Bus cable and a mounting point for the spring steel umbilical guide.

Six of these toolheads are used across the printer, each printed in its corresponding CMYK color (Cyan, Magenta, Yellow, Black, White, and Gray).

---

## Bill of Materials

### Base Toolhead

This build starts from the Dragon Burner toolhead and mounts to the printer via the StealthChanger backplate, neither of which are included in this repo:

| Part | Source | Note |
|------|--------|------|
| Dragon Burner Toolhead | [chirpy2605/voron-user-mods](https://github.com/chirpy2605/voron-user-mods/tree/main/Universal/DragonBurner) | Base toolhead body, printed parts, and hardware this cowl mounts to |
| StealthChanger DragonBurner Backplate | [StealthChanger project](https://stealthchanger.com/hardware/guides/backplates/4_dragonburner/#printed-bom) | Printed backplate that mounts the toolhead to the StealthChanger toolchanger |

### Component Selections

The Dragon Burner design supports several configurable options for hotend, extruder, motor, toolboard, and probe. These are the specific ones selected for this build.

| Part | Qty | Cost | Source | Note |
|------|-----|------|--------|------|
| TZ V6 2.0 Hotend | 1 | $17.87 | [AliExpress](https://s.click.aliexpress.com/e/_c3Mq5ohd) | |
| Moons Nema14 Motor | 1 | $19.84 | [AliExpress](https://s.click.aliexpress.com/e/_c3PY8IAP) | |
| BIGTREETECH EBB36 CANBus Toolhead Board V1.2 | 1 | $15.39 | [AliExpress](https://s.click.aliexpress.com/e/_c3MC48Xt) | |
| Voron Tap Probe Kit | 1 | $9.19 | [AliExpress](https://s.click.aliexpress.com/e/_c3SsvTCX) | |
| Sherpa Mini Extruder | 1 | | [Annex-Engineering/Sherpa_Mini-Extruder](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder) | See project for full BOM and print settings |

### Mods (This Repo)

Custom parts and hardware added on top of the base toolhead.

#### Cowl

| Part | Qty | Note |
|------|-----|------|
| dragonburner-cowl.STL | 1 | Printed part |
| 35mm M3 Socket Head Cap Screw | 2 |  |

#### EBB36 Strain Relief Cover

| Part | Qty | Note |
|------|-----|------|
| ebb36-strain-relief-cover.STL | 1 | Printed part |
| M2 12mm Standoff (Male-Female) | 2 | |
| M3 18mm Standoff (Female-Female) | 2 | |
| M3 Heatset Insert 5mm D x 4mm L | 1 | Same insert used elsewhere in this project |
| M3 20mm Button Head Cap Screw | 2 | |
| M3 8mm Socket Head Cap Screw | 2 | |
| 10mm Velcro Strap or Zip Tie | 1 | Secures the strain relief connection |
