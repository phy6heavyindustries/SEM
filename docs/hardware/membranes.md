# Ion Exchange Membranes

## Overview

DIY ion exchange membranes are the key innovation enabling SEM's low-cost operation. A method for manufacturing homogeneous ion exchange membranes from off-the-shelf precursors has been CC0-dedicated. This is the foundation technology that makes the entire SEM platform economically viable.

**License:** CC0 1.0 Universal (public domain)
**TRL:** 5 (lab prototype validated in harsh conditions)

## Core Innovation

**Homogeneous membrane** — pulverized commercial ion exchange resin particles dispersed uniformly in a PVC/CPVC matrix. No post-functionalization, no heating, no cross-linking required.

**Cost:** <$1/sq ft (vs $100+/sq ft for commercial membranes like Nafion).

## Membrane Types and Applications

### Cation Exchange Membrane (primary for SEM)
- **Resin:** Strong acid cation exchange resin (from water softener beads)
- **Allows:** Positive ions (Na+, K+, metal cations)
- **Blocks:** Negative ions (Cl-, OH-)
- **Use:** Salt water electrolysis for HCl production, continuous mining cell separator

### Anion Exchange Membrane
- **Resin:** Strong base anion exchange resin
- **Allows:** Negative ions (Cl-, OH-)
- **Blocks:** Positive ions
- **Use:** Specific applications requiring anion selectivity, electrodialysis configurations

### Specialized Resin Variants
- Rare earth-selective resins
- Platinum group metal (PGM)-selective resins
- Can be tuned by resin type/ratio for specific ion selectivity
- Lithium separation (block larger sodium ions)

---

## Production Recipe (CC0 Public Domain)

### Materials

| Ingredient | Purpose | Source | Notes |
|------------|---------|--------|-------|
| Water softener cation resin beads | Functional ion exchange groups | Hardware/water supply store | Strong acid cation type (sulfonic acid groups) |
| PVC/CPVC cement | Polymer matrix + solvent | Hardware store | Already contains PVC dissolved in solvent blend (THF, MEK, acetone, cyclohexanone) |
| Chopped fiberglass | Structural reinforcement | Composite supply | Standard practice (not optional in working formulation) |
| Optional: fumed silica, sand | Additional structural enhancement | Various | For specific applications |

### Manufacturing Process (Detailed)

**Step 1: Pulverize Resin Beads**
- Grind commercial ion exchange resin beads to powder < 200 microns
- Equipment options:
  - Industrial blender (video-confirmed method) — fastest, < 120 seconds
  - Ball mill (preferred for large batches) — dry or wet grinding
  - High-speed grinder — good for small batches
- Wet grinding: water assists lubrication but must be removed (spray dry or settle/decant + air dry)
- **Critical:** Remove water before mixing with PVC cement (water incompatible with THF/MEK solvents)

**Step 2: Prepare Polymer Matrix**
- Use commercial PVC/CPVC cement directly (pre-dissolved PVC in solvent)
- This is a practical shortcut vs. dissolving raw PVC pellets yourself
- PVC cement already contains: PVC + THF + MEK + acetone + cyclohexanone (typical formulation)
- Add chopped fiberglass reinforcement

**Step 3: Mix**
- Target ratio: 50% resin powder by volume (patent range: 10-70%)
- Typical polymer-to-solvent ratio: ~3:7 in PVC cement
- Mix to homogeneous glue consistency
- Add chopped fiberglass during mixing
- Optionally add more solvent if thinner viscosity needed for spraying

**Step 4: Apply**
- Methods: spreading, spraying, extruding, pouring
- Surface: polypropylene sheet (non-adhesive, solvent-resistant)
- Options: direct coating on substrate (polypropylene felt for reinforcement) or cell frame/electrode
- Thickness tunable by application technique
- Thin spray films achievable (<$1/sq yard)

**Step 5: Dry**
- Partial dry to avoid cracking or warping before handling
- Use enclosed environment to prevent uneven drying
- Peel from surface when partially dried (or leave as permanent coating if applied to substrate)

### Equipment Summary

| Equipment | Use | Priority |
|-----------|-----|----------|
| Industrial blender or ball mill | Resin grinding | Required |
| Spatula/mixer | Mixing resin + PVC cement | Required |
| Polypropylene sheet | Casting surface | Required |
| Enclosed drying space | Prevent uneven drying | Strongly recommended |

---

## Patent Claims (Full Text)

1. Homogeneous ion exchange membrane: pulverized pre-functionalized resin in PVC/CPVC matrix
2. Resin types: strong/weak acid cation, strong/weak base anion, or mixtures
3. Particle size: < 200 microns
4. Resin volume: 10-70% of membrane
5. Manufacturing method: pulverize → mix → apply → dry
6. Pulverizing: mechanical shearing (blender, grinder, ball mill)
7. Solvents: THF, cyclohexanone, methyl ethyl ketone
8. Water removal required if introduced during wet pulverizing
9. Application: spreading, spraying, extruding, pouring
10. Membrane can be peeled (partially dried) or left as permanent coating

---

## Quality Testing

### Cation Membrane Test (Dye)
1. Mix methylene blue dye with baking soda (increase pH)
2. Apply to membrane
3. Wait 20 seconds
4. Wash with water
5. Result: Stain should wash off (cation membrane doesn't absorb dye)

### Anion Membrane Test (Dye)
1. Mix methylene orange with baking soda
2. Apply to membrane
3. Result: Anion membrane absorbs methylene orange (stains)

### Function Test (Electrolysis)
1. Set up two-compartment cell with membrane
2. Salt water on one side, fresh water on other
3. Run electrolysis
4. Measure pH change in each compartment
5. Result: pH change proves ion transport across membrane

---

## Performance Characteristics

| Characteristic | Value/Notes |
|----------------|-------------|
| Cost | <$1/sq ft (vs $400-1200/sq ft commercial) |
| Ion selectivity | Commercial-level (comparable to Nafion in tested conditions) |
| Chemical resistance | Stable in pH 0, high ORP (>1.5V) for months |
| Mechanical flexibility | Flexible or rigid depending on formulation |
| Electro-osmosis | Present but low energy loss |
| Dendrite resistance | Subject to dendrite damage (physical piercing) |

## Failure Modes

### Dendrite Formation
- Metal dendrites grow through membrane under electrolysis
- Physical piercing creates holes, destroying selectivity
- Primary failure mechanism in metal recovery applications

### Mitigation
- Proper current density control
- Adequate membrane thickness
- Regular membrane replacement (cheap enough to be disposable)

## Cell Integration

- PVC/CPVC cement compatibility allows direct cell sealing
- Membrane can be permanently coated onto cell frame
- Compatible with standard divided cell configurations
- Also compatible with continuous recirculation flow design (cathode → anode)

---

## Open Source Status

**CC0 1.0 Universal** — Public domain
- No patent restrictions
- No licensing required
- Free for all use, including commercial

## Research Gaps

The following details are NOT documented in the patent but would be valuable for replication:
1. **Specific PVC cement brand/formulation** — different cements have different PVC content and solvent blends
2. **Exact fiberglass type and loading ratio** — chopped vs. milled, length, % by volume
3. **Optimal drying time and temperature** — "partial dry" is vague
4. **Membrane thickness vs. performance tradeoff** — how thickness affects resistance and selectivity
5. **Long-term degradation data** — months of operation, not years
6. **Electrode material compatibility** — which electrodes pair best with this membrane

## See Also
- SEM docs: `../closed_loop.md` (system architecture using these membranes)
- SEM docs: `electrolysis_cells.md` (cell designs incorporating membranes)
