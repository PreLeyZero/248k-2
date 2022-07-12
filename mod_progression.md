# Planned progression

The player starts as in usual factorio, however electricity won't be accessible from the start.
The mod will be structured in Ages similar to 248ks Stages but with more overall impact on the game and challenges:

- Steam Age
- Electricity Age
- Semiconductor Age
- Quantum Tech Age
- Exotic Age

# Difficulty/Level of the Mod

The mod should aim for a difficulty certainly below AngelBobs / pY but above K2, maybe around SE. A long game balanced and themed around the different ages should be the main goal. Byproduct handling will play a big role in the mod however should be done so that it is an reasonable alternative to processing without byproducts, mainly through increased yield/productivity and additional outputs. The chemistry part will add on the vanilla approach with kerosene and other sub oil products as well as with natural gas which behaves similar to oil. In later ages of the mod (about then when fusion is a thing) scaling the factory towards greater outputs should be the goal. This will be supported by different mechanics (not yet certain but f.e.: KI cores, Helium powered beacons, Star engine, high speed trains). How the game is won exactly in the exotic age is not yet certain and will be decided once the other ages are mainly done. 

# Science

Science packs will change from the vanilla ones (logistic, automation, chemical, production, utility and space) to one associated with each age. Military science may vanish completely and its techs will get sorted into the age progression.

1. Steam Tech
2. Electricity Tech
3. Computer Tech
4. Quantum Tech
5. Exotic Tech

`3` different Lab tiers will be available using different sciences (using above indices)

```mermaid
  flowchart LR;
    A(starter Lab) --> |1| B(vanilla Lab) --> |1,2,3| C(T-Lab) --> |3,4,5| D(end game)
```

# Resources

Resources will see some changes. Materials used in the early Ages can be found very easily as `surface ores` (normal ores as in current vanilla). Drilling spots can be found on the map resulting in `pure material chunks` or `mixed material chunks` which can be processed to both rare metals and also surface materials.

`Oil` and `natural gas` can be pumped as in vanilla.

`Stone` can be mined from **everywhere** on the map using a stone miner (maybe with the sprite of the old vanilla miner).

Here is a first draft of the minable materials:

1. **Minable Everywhere**
    - Stone
2. **Surface Ore**
    - Iron
    - Copper
    - Coal
3. **Deep Ore**
    - Coal vein
    - Copper vein
    - Iron vein
    - Sulfur vein
    - Titanium
    - Gold
    - Neodymium
    - Lead
4. **Deep fluids**
    - Oil
    - Natural Gas
5. **Space Ore**
    - Exotic Matter
6. **Only as byproduct from washing**
    - Lithium
    - Fluoride

Surface ores can be directly smelted into their `ingot` form. Washing need to be applied to the `deep ore chunks` to get them sorted and extract the raw materials, however it can also be used on surface ores for higher outputs.

Here are a few usages examples of these materials:

```mermaid
  flowchart LR
    A(Stone) --> |crushing| B(Sand) --> |smelting| C(Glass)
    A --> |Steam| D(Ceramic)
```
```mermaid
  flowchart LR
    A(Glass) --> |crushing| B(Glass powder) --> |fiber drawing| C(Glass fiber) --> |compositing| D(GFK)
    E(plastic) --> D
    A --> F(Electron tube) --> H(Green Circuit)
    G(Ceramic) --> F
    I(Copper Wire) --> H
```
Production chains will get more attention to detail in documents dedicated to each stage, which can be found in this repo.

# Component system

I intend to implement a component system for each of the above materials.
Processing an ore using different ways always will result in an ingot of the material. These ingots can be turned into `plates`, `beams`, and `mechanical parts` (an item combining gears and sticks and so other mechanical stuff).

```mermaid
  flowchart LR
    A(Ingot) --> B(Plate)
    A --> C(Beam)
    A --> D(Mechanical Parts)
    B --> |Arc| E(Molten Metal)
    C --> |Arc| E
    D --> |Arc| E
    E --> |Recast| A
```

Later when `arc furnaces` and liquid metals are available turning processed materials back into ingots will be possible. 

Besides the more mechanical component the player will also need to make `electronic components`, `high-tech components` and special `rocket parts`, which are all important items.