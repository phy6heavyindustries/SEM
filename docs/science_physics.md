# Science and Physics of SEM

## Electrochemical Foundation

SEM is fundamentally an **electrochemical process** that leverages the interaction between:
1. **Salt water electrolysis** to generate reactive chemical species
2. **Chlorine-based leaching chemistry** to dissolve metals
3. **Ion exchange membranes** to separate and purify reactions

## Membrane Electrolysis of Salt Water

### Electrochemical Reactions

At the **anode (positive electrode)**:
```
2Cl- → Cl2(g) + 2e-
```
Chlorine gas is generated from chloride ions in the salt solution.

At the **cathode (negative electrode)**:
```
2H2O + 2e- → H2(g) + 2OH-
```
Hydrogen gas and hydroxide ions are generated.

With a **cation exchange membrane** separating the compartments:
- Sodium ions (Na+) migrate to the cathode side
- Chloride ions stay in the anode compartment
- Result: HCl generated in anode chamber, NaOH in cathode chamber

### Leaching Chemistry

The chlorine gas and hydrochloric acid produced create a **highly oxidizing, acidic environment**:

```
Cl2 + H2O ⇌ HCl + HOCl (hypochlorous acid)
```

This system achieves:
- **pH ~0** (highly acidic)
- **ORP (Oxidation-Reduction Potential): 1.5V+**
- Enough oxidizing power to dissolve even noble metals

## Metal Dissolution Mechanisms

### Noble Metals (normally resistant to acids)

| Metal | Dissolution Reaction |
|-------|---------------------|
| Gold | `Au + 3Cl- + HOCl + H+ → [AuCl4]- + H2O` |
| Platinum | `Pt + 4Cl- + 2HOCl + 2H+ → [PtCl6]2- + 2H2O` |
| Rhodium | Similar chlorocomplex formation |
| Iridium | Similar chlorocomplex formation |

### Common Metals

| Metal | Dissolution Reaction |
|-------|---------------------|
| Silver | `Ag + Cl- → AgCl(s)` then complexed |
| Lead | `Pb + 2Cl- → PbCl2` |
| Copper | `Cu + 2Cl- → CuCl2` |
| Iron | `Fe + 2Cl- → FeCl2` |

## Physical Phenomena

### Temperature Effects
- SEM works **below freezing** because:
  - Sodium chlorate depresses freezing point
  - Hydrochloric acid further depresses freezing point
  - Solution remains liquid below 0°C

### Electrode Spacing Effects
- **Voltage-current sensitivity**: Moving electrodes apart drops voltage
- **Configuration matters**: Multiple electrode arrangements affect plating behavior
- **Electrode positioning** directly impacts current density and plating efficiency

### Dendrite Formation
- **Primary failure mode**: Metal dendrites grow through membranes
- **Mechanism**: Physical poking through membrane
- **Mitigation**: Proper current density control, membrane thickness selection

## Ion Exchange Membranes

### Cation Exchange Membrane
- Allows **positive ions** (cations) to pass
- Made from: **PVC cement + water softener resin**
- Resin provides sulfonic acid (-SO3H) functional groups
- Blocks anions and large molecules

### Anion Exchange Membrane
- Allows **negative ions** (anions) to pass
- Different resin type provides quaternary ammonium groups
- Blocks cations

### Testing Methods
| Test | Cation Membrane | Anion Membrane |
|------|----------------|----------------|
| Methylene Blue | Stains, washes off | Absorbs (stains permanently) |
| Methylene Orange | Stains, washes off | Absorbs |

## Power Characteristics

| Parameter | Value |
|-----------|-------|
| Typical Voltage | 12V |
| Typical Current | 17A |
| Unit Capacity | 2KW+ |
| Ore Processing | ~1 ton per unit (theoretical) |
| Electrolysis | Generates both HCl and sodium chlorate |
