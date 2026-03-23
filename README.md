# isaaclab-sim

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Release](https://img.shields.io/github/v/release/wuji-technology/isaaclab-sim)](https://github.com/wuji-technology/isaaclab-sim/releases)

Simulation demo (IsaacSim): minimal demo for loading and controlling the Wuji Hand in IsaacSim simulator. The script loads the default right hand model and plays the trajectory in a loop. Supports both left and right hand configurations.

https://github.com/user-attachments/assets/2f58ad84-7ed6-46fe-94c1-b4148068bec3

## Table of Contents

- [Repository Structure](#repository-structure)
- [Usage](#usage)
  - [Prerequisites](#prerequisites)
  - [Running](#running)
- [Contact](#contact)

## Repository Structure

```text
├── assets/
├── data/
│   └── wave.npy
├── wuji_hand_description/   (submodule: URDF, MJCF, USD, meshes)
├── run_sim.py
└── README.md
```

### Directory Description

| Directory / File | Description |
|------------------|-------------|
| `assets/` | Asset files for simulation |
| `data/` | Trajectory data files including `wave.npy` |
| `wuji_hand_description/` | Git submodule containing Wuji Hand model descriptions (URDF, MJCF, USD, meshes). USD assets include fused meshes with PBR materials, physics, and collision filter pairs. |
| `run_sim.py` | Main simulation script. Loads pre-built USD from submodule, no URDF conversion needed. |

## Usage

### Prerequisites

```bash
git clone --recurse-submodules https://github.com/wuji-technology/isaaclab-sim.git
```

Follow the [official documentation](https://isaac-sim.github.io/IsaacLab/main/source/setup/installation/index.html) to set up your environment.

### Running

```bash
# Right hand (default)
python run_sim.py

# Left hand
python run_sim.py --side left
```

The script loads the pre-built USD model from the submodule and plays the trajectory from `data/wave.npy` in a loop.

## Contact

For any questions, please contact [support@wuji.tech](mailto:support@wuji.tech).
