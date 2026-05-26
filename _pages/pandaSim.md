---
title: "PandaSim"
permalink: /pandaSim/
author_profile: true
header:
  overlay_image: 
  overlay_filter: 
  caption: 
  actions:
    - label: "GitHub Repository"
      url: "https://github.com/VahidDanesh/pandaSim"
---

Physics-based dexterous manipulation pipeline for the Franka Emika Panda robot in the [Genesis](https://github.com/Genesis-Embodied-AI/Genesis) simulator. The system integrates geometry extraction, screw motion planning, and resolved-rate motion control to reorient fallen objects using environmental contact and finger-level rotational slippage.

**Publication:** M. Boroji†, **V. Danesh**†, I. Kao, A. Fakhari, "[Motion Planning for Object Manipulation by Edge-Rolling](https://doi.org/10.1109/IROS58592.2024.10802581)," *IEEE/RSJ IROS*, 2024.

## Overview

We use a tabletop Franka Panda to reorient cuboids, cylinders, and bottles that start in random fallen poses. The Genesis Geometry Adapter extracts size, edges, and vertices from each object; a screw axis is constructed for the planned manipulation; and rotational slippage at the grasp point improves manipulability during uprighting. Across multiple simulation runs, the pipeline achieved a **96% reorientation success rate**.

## Core Components

* **Genesis Geometry Adapter** — Extracts geometric features (size, edges, vertices) from simulated objects for motion planning.
* **Screw Motion Planner** — Computes screw axes and trajectories for object reorientation, including rotational slippage at the grasp.
* **Resolved-Rate Controller** — Executes planned screw motions on the Panda manipulator.

```
pandaSim/
├── src/pandaSim/
│   ├── geometry/genesis_adapter.py
│   ├── planning/screw_motion_planner.py
│   └── control/resolved_rate.py
├── examples/upright.ipynb
└── model/
```

## Gallery

Object reorientation using environmental contact and finger-level rotational slippage ([`examples/upright.ipynb`](https://github.com/VahidDanesh/pandaSim/blob/master/examples/upright.ipynb)):

<table style="height:auto; width:auto;" cellspacing="0" cellpadding="0">
  <tr>
    <td><img src="/images/research/v1.gif" height="250" alt="Object reorientation in PandaSim"></td>
    <td><img src="/images/research/v4.gif" height="250" alt="Object reorientation in PandaSim"></td>
  </tr>
</table>

## Getting Started

Install PyTorch, then set up the environment and package:

```bash
git clone https://github.com/VahidDanesh/pandaSim.git
cd pandaSim
uv venv panda && source panda/bin/activate   # or: python -m venv panda
uv pip install 'pytransform3d[all]'
# Install Genesis from https://github.com/Genesis-Embodied-AI/Genesis
uv pip install .
```

See the [full README](https://github.com/VahidDanesh/pandaSim) for detailed installation steps and the [`upright.ipynb`](https://github.com/VahidDanesh/pandaSim/blob/master/examples/upright.ipynb) walkthrough.
