# Heathkit Restoration Plans — Index

Restoration plans for Heathkit SB-line and HW-series amateur radio gear, plus the power supplies that run it. Each plan covers which parts fail with age, a phased restoration procedure, alignment or tune-up, symptom quick-references, maintenance schedules and sources. Every plan is checked against the original Heath assembly manual and cites its printed page numbers.

Each repo holds the plan as pandoc markdown (`*-restoration-plan.md`), a rendered PDF and a README with the build command.

## Plans

| Equipment | Type | Repo | Status |
|---|---|---|---|
| **SB-301** | HF receiver | [heathkit-sb301-restoration](https://github.com/usa4148/heathkit-sb301-restoration) | Rev. 2, checked against the Heath manual (595-946-01) |
| **HW-101** | HF SSB/CW transceiver | [heathkit-hw101-restoration](https://github.com/usa4148/heathkit-hw101-restoration) | Rev. 2.2, checked against the Heath manual, plus the PS-23 and HP-23A manuals |
| **SB-102** | HF SSB/CW transceiver | [heathkit-sb102-restoration](https://github.com/usa4148/heathkit-sb102-restoration) | Rev. 2.2, checked against the Heath manual (595-1058-06), plus the PS-23 and HP-23A manuals |
| **SB-110 / SB-110A** | 6 m SSB/CW transceiver | [heathkit-sb110-restoration](https://github.com/usa4148/heathkit-sb110-restoration) | Rev. 2.2, checked against the SB-110A manual (595-1145-01), plus the PS-23 and HP-23A manuals |
| **SB-220** | HF linear amplifier (2 × 3-500Z) | [heathkit-sb220-restoration](https://github.com/usa4148/heathkit-sb220-restoration) | Rev. 1, checked against the Heath manuals |
| **SB-200** | HF linear amplifier (2 × 572B) | [heathkit-sb200-restoration](https://github.com/usa4148/heathkit-sb200-restoration) | Rev. 1, checked against the Heath manual |
| **HP-23 / 23A / 23B / 23C, PS-23** | AC power supplies | [heathkit-hp23-ps23-restoration](https://github.com/usa4148/heathkit-hp23-ps23-restoration) | Rev. 1, checked against the HP-23A and PS-23 manuals |

## Power supply quick-reference

The HW-101, SB-102 and SB-110A all run from the HP-23 series or PS-23, but they need **different low-voltage B+ settings.**

| Rig | B+ needed | HP-23A setting | PS-23 setting | Bias |
|---|---|---|---|---|
| HW-101 | 300 V @ 150 mA | Switch **right** (350 VDC tap) | **350 VDC** internal wiring | Fixed −130 V on pin 1; set on the transceiver (supply's bias control inoperative) |
| SB-102 | 300 V @ 150 mA | Switch **right** (350 VDC tap) | **350 VDC** internal wiring | Same as HW-101 |
| SB-110A | **250 V @ 100 mA** | Switch **left** (275 VDC tap) | **275 VDC** internal wiring | Same; −115 V needed |

If one supply is shared between rigs, **label the switch**, or rewire the PS-23 before using it with a different rig. On the HP-23A, pin 11 at the supply socket is adjustable bias; in the rig manuals' plug tables, pin 11 is a linear-amp relay contact at the transceiver end.

## Safety

Every unit here can kill. The supplies and transceivers carry about **700–850 V DC**, the SB-200 about **2.4 kV** and the SB-220 about **2.5–3 kV**. Charge stays on the filter capacitors after the equipment is unplugged.

- Discharge every time, with a grounded bleeder stick, before putting your hands inside.
- Bring restored gear up slowly on a variac.
- Use a 50 Ω dummy load (not a light bulb) for all transmit work.

## Common sources

- Original Heath assembly manuals: W5RKL ([w5rkl.com/manuals](https://w5rkl.com/manuals/)), Internet Archive, Bill Latta's HW-101 site (frostburg.edu)
- Heath mailing list archive, including transcribed service bulletins: [puck.nether.net/pipermail/heath](https://puck.nether.net/pipermail/heath/)
- groups.io: [Heathkit-Radios](https://groups.io/g/Heathkit-Radios), [heathkit](https://groups.io/g/heathkit), [HeathKit-HFAmps](https://groups.io/g/HeathKit-HFAmps)
- AF6C *Heathkit of the Month* series ([w6ze.org/Heathkit](https://www.w6ze.org/Heathkit/Heathkit_Index.html))
- W5RKL, *Heathkit HW-101 and SB-10x Restoration and Troubleshooting*

## Conventions

- **Manual-verified** items cite the Heath manual's printed page numbers.
- **Field** items (service bulletins, list threads, restorer notes) are credited to their source.
- **Mods** are marked optional and reversible; each plan restores to factory spec first.
- None of the manuals print voltage ratings for the electrolytics. The plans' replacement ratings come from the measured circuit voltages, so check them against your own unit.
