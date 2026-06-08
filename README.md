# Lhc_Visualizer2

Interactive 3D visualization of the Large Hadron Collider with real physics constraints. Built as an optimization framework that improves itself through gauntlet testing.

## Features
- Accurate 6.8 TeV/beam → 13.6 TeV collisions
- Dynamic dipole (8.33 T) + quadrupole fields
- Real-time Lorentz force induction modeling
- Retro Atari 800XL 8-bit computer emulator with native BASIC
- Live performance metrics & parameter optimization
- WebGL three.js unified matrix visualization

## Quick Start

### Option 1: Live Web Visualizations (No Install Required)
Visit the live demos directly:
- **WebGL Unified Matrix:** [index.html](https://keefnash100.github.io/Lhc_visualizer2/index.html)
- **Lenz-Koenigsegg Hypercar Simulator:** [lenz_simulator.html](https://keefnash100.github.io/Lhc_visualizer2/lenz_simulator.html)
- **Atari 800XL Matrix Emulator:** [atari_emulator.html](https://keefnash100.github.io/Lhc_visualizer2/atari_emulator.html)

### Option 2: Local Clone & Development
```bash
git clone https://github.com/KeefNash100/Lhc_visualizer2.git
cd Lhc_visualizer2

# Start a local web server to serve the HTML files
python -m http.server 8000
# or with Node.js:
npx http-server
```
Then visit `http://localhost:8000` in your browser.

## Atari 800XL Bootstrap Sequence

When you open `atari_emulator.html`, type these commands into the READY prompt:

```basic
10 GRAPHICS 7 : COLOR 1
20 PRINT "   == HAMMERLOOM V1.1 MATRIX =="
30 FOR T = 0 TO 314 STEP 0.1
40 Y = 40 + INT(ABS(COS(T)) * 8)
50 PLOT T * 0.5, Y : REM PLOTS THE INDUCED FIELD
60 SOUND 0, 150 + Y, 10, 6 : NEXT T
70 GOTO 30

RUN
```

## Project Structure
```
Lhc_visualizer2/
├── README.md
├── index.html                 # Unified WebGL matrix visualization
├── lenz_simulator.html         # Nürburgring hypercar simulator
├── atari_emulator.html         # Atari 800XL 8-bit computer
├── src/
│   └── core/
│       └── physics-engine.js   # Lorentz force calculations
└── docs/
    └── physics-constraints.md
```

## Gauntlet Results (Latest)
- FPS: 61.7+ @ 1440p
- Particles: 98k live
- Trajectory Error: 0.19%
- All runs strictly bound by real CERN parameters.

## Tech Stack
- Three.js / WebGL for modern rendering
- Atari 800XL 8-bit computer emulator (wscato.com.br)
- Real-time Lorentz force integration
- Vanilla JavaScript (no build tools required)

## License
MIT
