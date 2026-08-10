# Umbilical Bracket

![Umbilical Bracket CAD](../images/umbilical-bracket-cad.PNG)

A custom two-piece clamp bracket that bundles the three elements of each toolhead umbilical (a CAN bus cable, a PTFE filament guide tube, and flat spring steel) into a single organized assembly.

The bracket clamps firmly onto the CAN bus cable to maintain consistent spacing and orientation along the umbilical, while leaving enough room for the PTFE tube and spring steel to move freely. This gives the umbilical enough structure to stay organized without becoming too stiff to reach all areas of the print bed.

Flat spring steel is used only at the start and end of each umbilical rather than the full length, which proved to be the best balance between structure and flexibility. Eight umbilical assemblies are used in total, one per toolhead (six active + two spare).

![Umbilical Brackets Assembled](../images/umbilical-brackets-assembled-front.png)

---

## Bill of Materials

### Bracket: Printed Parts

| Part | Qty |
|------|-----|
| umbilical-bracket-bottom.STL | 1 |
| umbilical-bracket-top.STL | 1 |

### Bracket: Hardware

| Part | Qty | Unit Cost | Total Cost | Note |
|------|-----|-----------|------------|------|
| M3 Thread Rolling Screw | 1 | | | Covered by overall misc hardware estimate, see main README |

---

### Full Umbilical Assembly
*Per umbilical, 8 total (one per toolhead)*

| Part | Qty | Unit Cost | Total Cost | Source | Note |
|------|-----|-----------|------------|--------|------|
| Umbilical bracket (assembled) | 8 | | | | See Bracket Hardware above |
| CAN Bus Cable, 4mm diameter (~23.5 in / 600mm) | 1 | $4.00 | $4.00 | | Cut from a 6ft 100W shielded USB-C cable (2 CAN cables per 6ft USB-C cable); the exact cable I used is no longer sold. **Verify your replacement cable's rating meets your toolhead electronics' requirements** - alternatives include a 240W USB-C cable or a chainflex cable |
| PTFE Guide Tube, 4mm OD x 3mm ID (~26 in / 660mm) | 1 | $1.27 | $1.27 | [AliExpress](https://s.click.aliexpress.com/e/_c3qePSft) | $1.93/meter |
| GX12-4 Plug | 1 | | | [AliExpress](https://s.click.aliexpress.com/e/_c2vhMl6x) | Priced with the mating GX12-4 Jack, see [Umbilical Backplate](../umbilical-backplate/) BOM |
| 2x2 Microfit Connector | 1 | | | | Comes with the EBB36 toolboard, not purchased separately |
| Flat Coil Spring, 0.3mm x 3mm (70mm length) | 1 | $1.67 | $13.39 | [AliExpress](https://s.click.aliexpress.com/e/_c2xB7uAf) | Cut from a 0.3x3x34x1900mm roll ($13.39 total, ~$1.67/umbilical); one roll covers the whole build (8 umbilicals) |
| Flat Coil Spring, 0.3mm x 3mm (100mm length) | 1 | | | [AliExpress](https://s.click.aliexpress.com/e/_c2xB7uAf) | Cut from the same roll, cost counted on the 70mm line |
