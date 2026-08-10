# Dragon Burner Toolhead Cowl

![Dragon Burner Cowl CAD](../images/dragon-burner-toolhead-assembly.png)

A custom cowl for the [Dragon Burner](https://github.com/chirpy2605/voron-user-mods/tree/main/Universal/DragonBurner) toolhead by chirpy2605. Configured with a Sharkpa Mini Extruder and TZ 2.0 V6 hotend, a combination selected after testing multiple setups for the best balance of print quality and cost.

There are also files for the EBB36 toolhead board cover that provides strain relief for the CAN Bus cable and a mounting point for the spring steel umbilical guide.

Six of these toolheads are used across the printer, each printed in its corresponding CMYK color (Cyan, Magenta, Yellow, Black, White, and Gray).

---

## Bill of Materials

### Base Toolhead

This build starts from the Dragon Burner toolhead and mounts to the printer via the StealthChanger backplate, neither of which are included in this repo:

| Part | Qty | Unit Cost | Total Cost | Source | Note |
|------|-----|-----------|------------|--------|------|
| Dragon Burner Toolhead | 1 | | | [chirpy2605/voron-user-mods](https://github.com/chirpy2605/voron-user-mods/tree/main/Universal/DragonBurner) | Base toolhead body, printed parts, and hardware this cowl mounts to; external assembly hardware covered by overall misc hardware estimate, see main README |
| StealthChanger DragonBurner Backplate | 1 | | | [StealthChanger project](https://stealthchanger.com/hardware/guides/backplates/4_dragonburner/#printed-bom) | Printed backplate that mounts the toolhead to the StealthChanger toolchanger |
| 4x12mm M3 Dowel Pin | 3 | $0.75 | $2.25 | [AliExpress](https://s.click.aliexpress.com/e/_c3iT67xV) | Sold in packs of 10; secures the StealthChanger backplate |

### Component Selections

The Dragon Burner design supports several configurable options for hotend, extruder, motor, toolboard, and probe. These are the specific ones selected for this build.

| Part | Qty | Unit Cost | Total Cost | Source | Note |
|------|-----|-----------|------------|--------|------|
| TZ V6 2.0 Hotend | 1 | $17.87 | $17.87 | [AliExpress](https://s.click.aliexpress.com/e/_c3Mq5ohd) | |
| Moons Nema14 Motor | 1 | $19.84 | $19.84 | [AliExpress](https://s.click.aliexpress.com/e/_c3PY8IAP) | |
| BIGTREETECH EBB36 CANBus Toolhead Board V1.2 | 1 | $15.39 | $15.39 | [AliExpress](https://s.click.aliexpress.com/e/_c3MC48Xt) | |
| Voron Tap Probe Kit | 1 | $9.19 | $9.19 | [AliExpress](https://s.click.aliexpress.com/e/_c3SsvTCX) | |
| Gdstime 3010 24V Sleeve 2P2.54 Fan | 1 | $4.08 | $4.08 | [AliExpress](https://s.click.aliexpress.com/e/_c3NtUlNp) | |
| Gdstime 4010 24V H 2P2.54 Fan | 2 | $5.14 | $10.28 | [AliExpress](https://s.click.aliexpress.com/e/_c4E8RYo3) | |
| Sherpa Mini Extruder | 1 | $4.08 | $4.08 | [Annex-Engineering/Sherpa_Mini-Extruder](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder) | Self-printed; cost shown is a cheap [AliExpress hardware kit](https://s.click.aliexpress.com/e/_c4qK86KB) (bearings/pins/springs), see project for full BOM and print settings |

### Mods (This Repo)

Custom parts and hardware added on top of the base toolhead.

#### Cowl

| Part | Qty | Unit Cost | Total Cost | Source | Note |
|------|-----|-----------|------------|--------|------|
| dragonburner-cowl.STL | 1 | | | | Printed part |
| 35mm M3 Socket Head Cap Screw | 2 | $0.23 | $2.25 | [AliExpress](https://s.click.aliexpress.com/e/_c3tmFYGL) | $2.25 per 10pc pack, only sold as a full pack |

#### EBB36 Strain Relief Cover

| Part | Qty | Unit Cost | Total Cost | Source | Note |
|------|-----|-----------|------------|--------|------|
| ebb36-strain-relief-cover.STL | 1 | | | | Printed part |
| M2 12mm Standoff (Male-Female) | 2 | | | | Covered by overall misc hardware estimate, see main README |
| M3 18mm Standoff (Female-Female) | 2 | | | | Covered by overall misc hardware estimate, see main README |
| M3 Heatset Insert 5mm D x 4mm L | 1 | | | | Same insert used elsewhere in this project; covered by overall misc hardware estimate, see main README |
| M3 20mm Button Head Cap Screw | 2 | | | | Covered by overall misc hardware estimate, see main README |
| M3 8mm Socket Head Cap Screw | 2 | | | | Covered by overall misc hardware estimate, see main README |
| 10mm Velcro Strap or Zip Tie | 1 | | | | Secures the strain relief connection; covered by overall misc hardware estimate, see main README |
