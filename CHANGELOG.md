# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Changed

- Load pre-built USD from `wuji_hand_description/usd/` submodule instead of URDF conversion at runtime
- Remove `wuji_hand.py` — articulation config inlined in `run_sim.py`, PD gains and collision filters read from USD
- Add `--side` CLI argument for left/right hand selection (replaces hardcoded `HAND_SIDE`)
- Update `wuji_hand_description` submodule to v0.2.3 (includes USD assets with PBR materials and collision filter pairs)

## [0.1.0] - 2026-02-02

### Added

- Main simulation script `run_sim.py` for loading and controlling Wuji Hand in IsaacSim
- Wuji Hand model implementation `wuji_hand.py`
- Trajectory playback from `data/wave.npy` with loop support
- Support for both left and right hand configurations
- Wuji Hand model as git submodule (`wuji_hand_description/`)

[Unreleased]: https://github.com/wuji-technology/isaaclab-sim/compare/v0.1.0...HEAD
[0.1.0]: https://github.com/wuji-technology/isaaclab-sim/releases/tag/v0.1.0
