# Closed-Loop System Design

## The Core Insight

Traditional mining processes fail in resource-constrained environments because they depend on **external chemical supply chains**. SEM solves this by being **self-referential**:

```
Salt + Water + Electricity
        ↓
    ┌───────────────┐
    │  Electrolysis │ → HCl + NaClO₃ + Oxidizing Power (ORP > 1.5V)
    └───────┬───────┘
            ↓
    ┌───────────────┐
    │     CMU       │ → Metals dissolved + Waste residue (non-toxic)
    │  (Leaching)   │
    └───────┬───────┘
            ↓
    ┌───────────────┐
    │     CRU       │ → Pure metals + Regenerated acid (back to CMU)
    │  (Refining)   │
    └───────────────┘
```

## Why Closed-Loop Matters

### Space/Asteroid Mining
- Every kilogram shipped costs fortune
- Consumable-dependent processes are non-viable
- SEM needs only: salt + electricity + feedstock

### Remote Operations
- No acid shipping required
- No chemical resupply chain
- Operate anywhere with power and salt

### Economic Advantage
- Chemical cost → near zero
- No supply chain risk
- Continuous operation possible
- <$5/cubic yard waste processing, $50-400/ton ore

## Unique Flow Architecture

**The key innovation** is not just the membrane — it's the **continuous recirculation** design:

| Typical Cell | SEM Design |
|-------------|----------------|
| Fully divided, stationary compartments | Electrolyte recirculated cathode → anode |
| Batch processing | Continuous cycling |
| Acid consumed and discarded | Acid regenerated and reused |
| Two streams to manage | Single integrated loop |

This architecture has demonstrated:
- Strong performance for continuous cycling
- Stable operation over extended periods
- More effective for continuous processing than static divided cells
- Still, static divided cells remain useful for specific use cases (liquid mine waste treatment, acid regeneration)

## Self-Regenerating Chemistry

### Acid Regeneration
1. Metals dissolved in HCl solution
2. Electrolysis plates metals onto cathode at controlled potentials
3. Chloride ions remain and regenerate HCl in anode chamber
4. Regenerated acid returns to leaching
5. **Net: zero acid consumption**

### Sodium Chlorate Cycle
- Generated via extended electrolysis of salt water
- Provides oxidizing potential (part of the ORP > 1.5V system)
- Replenished as consumed
- Concentration controlled by electrolysis duration

### Metal Recovery
- Staged deposition by controlling electrode potential
- Sequential recovery: precious metals → base metals → REEs → remaining
- Mixed-metal concentrate for downstream refining
- Recovery yields >99% for many target metals

## System Architecture

### Continuous Mining Unit (CMU)
- **Intake:** Raw feedstock (ore, tailings, waste) + leaching solution
- **Output:** Metal-rich solution + waste residue
- **Process:** Chemical dissolution under pH 0, ORP > 1.5V
- **Footprint:** 50-300 sq ft for 1 ton/day
- **Largest component:** Vacuum filtration drum

### Continuous Refining Unit (CRU)
- **Intake:** Metal-rich solution from CMU
- **Output:** Pure metals + regenerated acid
- **Process:** Electrochemical separation with tuned chemistry
- **Modes:** Standard electrolysis, electrodialysis, multi-cell
- **TRL:** 5 → targeting 7+

### Electrolysis Cell Network
- Generates HCl from saltwater
- Generates sodium chlorate (oxidizer)
- Regenerates leaching solution
- Can extract specific metals (Li, Rb, Cs with add-on cells)
- Membrane-divided with continuous recirculation

## Temperature Resilience

The system operates in sub-freezing conditions:
- Sodium chlorate + HCl depress freezing point
- Solution remains liquid below 0°C
- Enables year-round operation in cold climates
- Critical for northern latitude deployment

## Scalability

| Scale | Power | Throughput | Notes |
|-------|-------|------------|-------|
| Lab | 2KW | grams/day | Research/prototyping |
| Pilot | 20KW | kg/day | Commercial testing |
| Industrial | 200KW+ | tons/day | Full-scale operation |

### Scaling Characteristics
- Electrolysis cell stack = only a few sq ft at 1 ton/day throughput
- Efficiency **improves** with scale (better integration, reduced relative losses)
- No specialty site modifications required
- Standard 100-amp residential service for 1 ton/day unit

## Safety and Operation

- Simple process controls: conductivity + current density monitoring
- Rapid training, no specialized degree required
- Chlorine odor provides leak detectability
- Ventilation, enclosures, leak detection standard
- 1 ton/day achievable with residential power infrastructure

## See Also
- `overview.md` — Full SEM TECH system overview
- `economics.md` — Cost analysis and projections
- `chemistry/core_reactions.md` — Electrochemical reactions
- `hardware/electrolysis_cells.md` — Cell designs
