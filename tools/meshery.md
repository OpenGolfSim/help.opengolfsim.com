---
title: Meshery
parent: Course Building
nav_order: 4
published: false
---

Meshery is a <a href="https://en.wikipedia.org/wiki/Command-line_interface" target="_blank">CLI</a> tool that takes an SVG file and raw terrain file as input and exports a collection of meshes that conform to the terrain height. This makes it easy to layout your course in a vector program, like <a href="https://inkscape.org/" target="_blank">Inkscape</a>.


The command looks like this:


```bash
svg_to_mesh.py SVG_INPUT_FILE RAW_TERRAIN_FILE SVG_WIDTH HEIGHT_SCALE OUTPUT_FOLDER
```

### Options

- `SVG_INPUT_FILE` Is the path to the SVG file containing your course map.
- `RAW_TERRAIN_FILE` Is the path to the raw terrain data file you exported from your terrain in Unity.
- `SVG_WIDTH` The width/height of the SVG file. (Note: The SVG width and height should be the same so that it matches the 1:1 aspect of the unity terrain)
- `HEIGHT_SCALE` The maximum terrain height for scaling the meshes. Generally you want to use the **Terrain Height** setting from your Unity terrain.
- `OUTPUT_FOLDER` The folder to save the newly created mesh files to. Folder will be created if it doesn't exist.



## Unity Terrain Export Instructions

Once you have your terrain data finalized, you'll need to export a raw terrain file. This file will be used to conform your course surfaces to your terrain height.

1. Select the terrain in your Unity project.
1. In the Inspector, under Terrain Settings, select **Export Raw**
  - Depth: **Bit 16**
  - Byte Order: **Windows**
  - Flip Vertically: **True**
1. Click **Export**


### Example Command

```bash
svg_to_mesh.py my_course.svg my_terrain.raw 1000 50 ./my_meshes
```

For the terrain size, you'll need to find your heightmap resolution.
<img src="/assets/course-building/unity-terrain-size.jpg" width="300" />