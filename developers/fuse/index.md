---
parent: Developers
title: FUSE
nav_order: 2
---

## FUSE (Fast Universal Simulator Engine)

FUSE (Fast Universal Simulator Engine) is [OpenGolfSim](https://opengolfsim.com/)'s lightweight 3D golf simulation and physics engine. Providing components and utilities for building fully featured golf simulator experiences in any WebGPU or WebGL-capable browser or device.

Download and install [OpenGolfSim](https://opengolfsim.com) Desktop or Mobile, to see the engine in action, connect, and send shots your launch monitor.

<a target="_blank" class="btn btn-icon" href="https://github.com/OpenGolfSim/fuse">
  <img src="https://cdn.simpleicons.org/github/EEEEEE" width="24" />
  <span style="margin-left: 3px;">View on Github</span>
</a>

> <small>This software is licensed under the PolyForm Noncommercial License 1.0.0. For commercial use, please [contact us](/contact).</small>


### Building & Installing

First clone the FUSE repo:

```bash
git clone https://github.com/OpenGolfSim/fuse.git
```

Enter the cloned directory:

```bash
cd fuse
```

Run the development server locally:

```bash
npm run dev
```

You should now be able to load the examples in your browser at `http://localhost:5173`

### Module

The FUSE repo can be installed as an node module in your own project and used to create fully custom games and experiences.

```bash
npm install github:@opengolfsim/fuse
```
