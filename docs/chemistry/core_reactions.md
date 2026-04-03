# Core Reactions in SEM TECH

## Overall Process Chemistry

SEM TECH uses **saltwater (NaCl + H2O) + electricity** to generate the leaching environment in situ. The key chemical species are:

1. **Hydrochloric acid (HCl)** — primary leaching agent
2. **Sodium chlorate (NaClO3)** — oxidizing agent
3. **Chlorine (Cl2)** — generates strong oxidizing potential

## Electrolysis of Salt Water

### Primary Anode Reactions
```
2Cl⁻ → Cl₂(g) + 2e⁻              E° = -1.36 V
Cl₂ + H₂O → HClO + H⁺ + Cl⁻      (chlorine hydrolysis)
3HClO → ClO₃⁻ + 2Cl⁻ + 3H⁺      (chlorate formation)
```

### Primary Cathode Reactions
```
2H₂O + 2e⁻ → H₂(g) + 2OH⁻        E° = -0.83 V
Na⁺ + e⁻ → Na                    (not favorable in water)
```

### Net Effect
- **Anode compartment:** Acidic (H⁺ generated), oxidizing (Cl₂, HClO, ClO₃⁻)
- **Cathode compartment:** Alkaline (OH⁻ generated), reducing

### Membrane Role
The ion exchange membrane separates the two compartments while allowing ion transport to complete the circuit:
- **Cation membrane:** Na⁺ migrates from anode side to cathode side
- Maintains charge balance while keeping chemistries separated

## Leaching Chemistry

The generated leaching solution has:
- **pH ≈ 0** (concentrated HCl)
- **ORP > 1.5 V** (strong oxidizing potential from Cl₂/ClO₃⁻ system)

### Metal Dissolution

Under these conditions, noble and base metals dissolve as chlorocomplexes:

| Metal | Dissolution Reaction | Notes |
|-------|---------------------|-------|
| Au | Au + 3Cl₂ + 2Cl⁻ → [AuCl₄]⁻ + Cl₂ | Gold requires chloride + oxidizer |
| Pt | Pt + 2Cl₂ + 2Cl⁻ → [PtCl₄]²⁻ | Platinum group metals |
| Rh | Rh + 3Cl₂ → RhCl₃ | Rhodium dissolution |
| Pd | Pd + Cl₂ → PdCl₂ | Palladium dissolution |
| Ag | Ag + Cl⁻ → AgCl(s) → [AgCl₂]⁻ | Silver (forms precipitate, dissolves in excess Cl⁻) |
| Fe | Fe + 2H⁺ + Cl₂ → Fe²⁺ + 2HCl | Iron (easily dissolved) |
| Cu | Cu + Cl₂ → CuCl₂ | Copper |
| Ni | Ni + Cl₂ → NiCl₂ | Nickel |
| REEs | 2REE + 6HCl → 2RECl₃ + 3H₂ | Rare earth elements |

### Selectivity

- **53 of 60 critical minerals** dissolve in the single leaching solution
- **Not dissolved:** Barite (BaSO4), Fluorspar (CaF2), Coal, Graphite (native compounds)
- **Requires modification:** Si, Ti, W (need HF or alkaline conditions)

## Metal Recovery (Refining)

### Electrochemical Deposition

Metals are recovered from solution by controlling applied potential:

```
[AuCl₄]⁻ + 3e⁻ → Au + 4Cl⁻        E° ≈ +0.93 V vs SHE
Pt²⁺ + 2e⁻ → Pt                    E° ≈ +1.18 V vs SHE
Cu²⁺ + 2e⁻ → Cu                    E° ≈ +0.34 V vs SHE
Fe²⁺ + 2e⁻ → Fe                    E° ≈ -0.44 V vs SHE
```

**Key principle:** Different metals plate at different potentials. By controlling voltage, you can selectively recover metals in stages.

### Staged Recovery

By adjusting electrode potential, electrolyte composition, and electrode material:
1. Stage 1: Precious metals (Au, Pt, Pd) at high potentials
2. Stage 2: Base metals (Cu, Ni, Co) at moderate potentials
3. Stage 3: Heavy metals and REEs at lower potentials
4. Stage 4: Remaining species (concentration)

## Acid Regeneration

### The Closed Loop

After metal plating at the cathode:
1. Chloride ions remain in solution
2. Anode chamber regenerates HCl from the remaining species
3. Regenerated acid is recirculated to leaching
4. Net chemical consumption approaches zero

### Sodium Chlorate Cycle

Continuous electrolysis replenishes chlorate:
- Generated as a byproduct of extended saltwater electrolysis
- Provides consistent oxidizing power
- Concentration maintained by controlling electrolysis time

## Electrodialysis (Multi-Cell Mode)

A multi-cell configuration enables single-stage elemental separation:
- Multiple compartments with alternating membrane types
- Each stage concentrates different ion species
- More efficient than single-cell batch processing

## Temperature Effects

- Solution freezing point is depressed by dissolved salts and acids
- System can operate below 0°C
- Reaction rates decrease at lower temperatures but remain viable

## See Also
- `regeneration.md` — Detailed acid and electrolyte regeneration
- `leaching_chemistry.md` — Specific leaching conditions and optimization
- `../hardware/membranes.md` — Ion exchange membrane details
