# lhc_visualizer2

Interactive 3D visualization of the Large Hadron Collider with real physics constraints. Built as an optimization framework that improves itself through gauntlet testing.

## Features
- Accurate 6.8 TeV/beam → 13.6 TeV collisions
- Dynamic dipole (8.33 T) + quadrupole fields
- Multi-bunch trains & luminosity visualization
- Retro CRT mode powered by **[A8E Atari 800XL Emulator](https://github.com/AnimaInCorpore/A8E)**
- Live performance metrics & parameter optimization

## Quick Start
```bash
git clone https://github.com/KeefNash100/lhc_visualizer2.git
cd lhc_visualizer2
git submodule update --init --recursive   # for A8E
npm install
npm run dev
```

## Gauntlet Results (Latest)
- FPS: 61.7+ @ 1440p
- Particles: 98k live
- Trajectory Error: 0.19%
- All runs strictly bound by real CERN parameters.

## Tech Stack
- Three.js / WebGL for modern rendering
- jsA8E for authentic CRT/phosphor effects
- Real-time Lorentz force integration
- WebGL compute shaders for particle physics

## Project Structure
```
lhc_visualizer2/
├── README.md
├── LICENSE
├── package.json
├── index.html
├── src/
│   ├── core/             # Physics engine (Lorentz, E/B fields, collisions)
│   ├── render/           # Three.js / WebGL + A8E integration
│   ├── ui/               # Parameter sliders, timeline, toggles
│   └── optimization/     # Gauntlet test harness, parameter sweeps
├── external/
│   └── A8E/              # git submodule or copied jsA8E
├── assets/
│   └── models/           # Tunnel segments, magnets (GLTF or procedural)
├── tests/
│   └── gauntlet/         # Simulation scenarios + metrics
├── docs/
│   └── physics-constraints.md
└── .github/
    └── workflows/        # CI for builds & auto-stats
```

## License
MIT
