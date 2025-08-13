# Evolution Simulator — Predator & Prey (NEAT-ish)

A single-file, browser-based evolution sandbox. Agents (prey & predators) use small neural networks with **mutable topology** (nodes/layers/edges) and weights to forage, flee, hunt (including predator-vs-predator), and reproduce. Traits like **color**, **attack strength**, and **network structure** evolve over time. Includes a live NN viewer, follow modes, and save/load for brains.

![UI](https://i.imgur.com/tCIFLDC.png)

## Highlights

* **Variable-topology brains**: hidden layers & node counts evolve; connections add/remove.
* **Sensing**: food aggregate, **kin aggregate**, and **top-K (4) nearest agents** with angle, closeness, type (prey/pred), and kin flags (parent/child/sibling).
* **Behavior**: predators hunt prey & other predators; **kin-penalties** discourage eating parent/child/sibling.
* **Traits**: color (HSL) is **heritable + mutatable**; predators have a damage output node.
* **Viewer**: curved-edge NN graph with live activations + labeled outputs; per-agent insights (gen, fitness, I/O snapshot).
* **Camera/Follow**: many follow modes (best, latest gen, most nodes/layers/conns, density, fittest, fastest, etc).
* **Performance**: timescale slider with sub-stepping; optional trail/vision rendering.

![NN 1](https://i.imgur.com/Hs4Snpi.png)
![NN 2](https://i.imgur.com/eEVh30a.png)

## Quick Start

1. Download/clone and open `evolution_simulator.html` in a modern browser.
2. Use the **sidebar** to tune populations, energy, evolution rates, perception/motion, and **timescale**.
3. Click an agent to inspect its brain; change **Follow** to auto-track interesting individuals.

### Controls

* **Run/Pause**, **Step**, **Reset**
* **Follow** selector (many modes)
* **Save brain** (selected) • **Load → Selected** • **Default Prey/Predator** (reseeds on Reset)
* Optional **Trails** & **Show vision** toggles

### Keyboard

* `Space` = Pause/Run
* `Shift + Space` = Step one tick

## Intention

This project is a compact playground for **emergent behavior** and **neuro-evolution** with minimal dependencies. It’s great for experimenting with sensing abstractions, selection pressure, and genome/topology mutations to see what strategies emerge.
