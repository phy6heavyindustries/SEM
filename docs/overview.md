# SEM TECH: System Overview

## What is SEM TECH?

**Salt Electro Mining Technology** — an open-source platform that uses saltwater and electricity to extract precious metals, rare earth elements, and critical minerals from ore, mining waste, and other feedstocks.

**Source:** CC0 licensed public domain research
**TRL:** 5 (lab prototype), targeting TRL 7+ with DOE funding

## Core Concept

SEM TECH generates its own leaching chemicals in situ through electrolysis:

```
Salt + Water + Electricity → HCl + Sodium Chlorate + Oxidizing Potential
```

The resulting solution has:
- **ORP > 1.5 V** (strong oxidizing potential)
- **pH ≈ 0** (highly acidic)
- **Chlorine-rich** environment capable of dissolving noble metals

Under these conditions, the solution dissolves:
- Gold, platinum, rhodium, palladium
- Silver, tin, selenium
- Most rare earth elements and critical minerals

## Element Coverage

**56 of 60 critical minerals extractable:**

| Category | Elements |
|----------|----------|
| Extracted in CMU (53) | Aluminum, Antimony, Arsenic, Beryllium, Bismuth, Boron, Cerium, Cesium, Chromium, Cobalt, Copper, Dysprosium, Erbium, Europium, Gadolinium, Gallium, Germanium, Hafnium, Holmium, Indium, Iridium, Lanthanum, Lead, Lithium, Lutetium, Magnesium, Manganese, Neodymium, Nickel, Niobium, Palladium, Phosphate, Platinum, Potash, Praseodymium, Rhenium, Rhodium, Rubidium, Ruthenium, Samarium, Scandium, Silver, Tantalum, Tellurium, Terbium, Thulium, Tin, Uranium, Vanadium, Ytterbium, Yttrium, Zinc, Zirconium |
| Requires modification (3) | Silicon, Titanium, Tungsten (need different solvents: HF or alkaline leaching) |
| Not designed for (4) | Barite, Fluorspar, Metallurgical Coal, Graphite (recovered as native compounds, not dissolved elements) |

## System Architecture

```
┌──────────────────────────────────────────────────────────┐
│                    SEM TECH SYSTEM                       │
│                                                          │
│  ┌─────────────┐    ┌─────────────┐    ┌─────────────┐  │
│  │     CMU     │ -> │     CRU     │ -> │   Products  │  │
│  │ (Mining)    │    │ (Refining)  │    │             │  │
│  └──────┬──────┘    └──────┬──────┘    └─────────────┘  │
│         │                  │                             │
│         └────────┬─────────┘                             │
│                  ▼                                       │
│          ┌──────────────┐                                │
│          │ Electrolysis │ ← Salt + Water + Electricity   │
│          │    Cells     │   → HCl + NaClO3               │
│          └──────────────┘                                │
│                  │                                       │
│                  ▼                                       │
│          ┌──────────────┐                                │
│          │  Membrane    │ ← Core enabling technology     │
│          │  (CC0 recipe)│   <$1/sq ft, DIY from resin    │
│          └──────────────┘                                │
└──────────────────────────────────────────────────────────┘
```

### Continuous Mining Unit (CMU)
- **Intake:** Raw feedstock (ore, tailings, mining waste) + leaching solution
- **Process:** Chemical dissolution of target metals under acidic, oxidizing conditions
- **Output:** Metal-rich solution + waste residue
- **Footprint:** 50-300 sq ft for 1 ton/day throughput

### Continuous Refining Unit (CRU)
- **Intake:** Metal-rich solution from CMU
- **Process:** Electrochemical separation at controlled potentials
- **Output:** Pure metals + regenerated acid (sent back to CMU)
- **Modes:** Standard electrolysis, electrodialysis, multi-cell configuration

### Electrolysis Cells
- **Primary function:** Generate HCl and sodium chlorate from saltwater
- **Secondary function:** Drive metal reduction at controlled potentials
- **Configuration:** Membrane-divided cells with continuous recirculation
- **Power:** Standard 100-amp residential service for 1 ton/day unit

## Key Innovation: Closed-Loop Recirculation

Unlike typical divided stationary cells, SEM uses a unique **continuous recirculation** design:
- Electrolyte solution circulates from cathode compartment → anode side
- This maintains charge balance while continuously processing
- Acids are regenerated in situ, reducing chemical dependence
- The integrated flow approach is more effective for continuous processing

## Performance Metrics

| Metric | Value | Notes |
|--------|-------|-------|
| Recovery yield | >99% | For many target metals |
| Ore processing cost | $50-400/ton | Early non-optimized cells |
| Energy consumption | 300-2,200 kWh/ton | Large error margin, early stage |
| Liquid waste processing | <33 kWh/255 gal | ~$5 in electricity |
| Footprint | 50-300 sq ft | For 1 ton/day CMU |
| Membrane cost | <$1/sq ft | vs $100-400 commercial |
| Temperature operation | Below 0°C possible | Solution freezing point depressed |

## Development History

| Date | Milestone |
|------|-----------|
| Nov 2023 | Project began, leveraging prior redox flow battery membrane work |
| Early 2024 | Initial aqua regia testing → pivoted to NaClO3/NaClO oxidizers |
| 2024 | Bench-scale testing on gold-bearing ore, first successful gold plating |
| 2025 | Scale-up trials, membrane manufacturing improvements, multi-cell discovery |
| 2025 | Private mining firm engagements, successful demonstrations |
| Pending | DOE proposal: $12.8M to scale TRL 5 → TRL 7+ |

## Applications

1. **Mining waste reprocessing** — recover metals from tailings and waste streams
2. **Low-grade ore processing** — economically viable at grades that mining companies ignore
3. **Toxic waste remediation** — extract heavy metals while producing non-toxic residue
4. **Remote/off-grid operations** — only needs salt, water, electricity, feedstock
5. **Space/asteroid mining** — zero external chemical dependency
6. **Acid regeneration** — continuous HCl regeneration from mining effluents

## See Also
- `closed_loop.md` — Detailed closed-loop system design
- `economics.md` — Economic analysis and cost projections
- `chemistry/core_reactions.md` — Electrochemical reactions and chemistry
- `hardware/membranes.md` — Membrane manufacturing details
- `hardware/electrolysis_cells.md` — Cell designs and configurations
