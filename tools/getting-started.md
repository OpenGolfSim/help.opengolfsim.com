---
title: Getting Started
parent: Course Developers
nav_order: 1
---

# Getting Started

Before you start building courses, you'll need a few of different tools installed on your machine to create courses for OpenGolfSim. We recommend grabbing and setting up all these tools before you start. Don't worry if you're not very technical, they are all pretty user friendly.

1. TOC
{:toc}


## Install Unity

We use Unity as our 3D engine and simulator environment. To create playable courses you'll need to create a project in a compatible version of Unity and export your course as a Unity asset bundle. Start by installing the correct version of Unity using the steps below.

1. Download and install Unity Editor `6000.2.6f2`. It needs to be that specific version of Unity, or the built course may not work correctly. You can Unity Hub to install specific versions, or directly using the link below.

<a href="https://unity.com/releases/editor/whats-new/6000.2.6f2" target="_blank" class="btn">
  <span>Download Unity Editor 6000.2.6f2</span>
</a>

2. Download the latest OpenGolfSim Unity [Project Template](https://github.com/OpenGolfSim/unity-project-template) from our github repository.

<a href="https://github.com/OpenGolfSim/unity-project-template/archive/refs/heads/main.zip" target="_blank" class="btn">Download OGS Project Template</a>

---

## Install Inkscape

Inkscape is a free vector graphics editing program. We use it to layout the course using the pen tool to create vector paths that represent features like fairways, greens, tee boxes, etc. 

<a href="https://inkscape.org/" target="_blank" class="btn">Download Inkscape</a>

### Install the OGS Color Palette

You'll need the official OGS color palette installed in Inkscape so you can set shapes to the correct color codes.

1. Download the latest OpenGolfSim color palette:

    <a download="OGSColorPalette.gpl" href="https://raw.githubusercontent.com/OpenGolfSim/course-meshery/main/data/palette.gpl" target="_blank" class="btn">Download OGS Color Palette.gpl</a>
    <br>
    <small>Right-click the download button and select   <em>Save Link As...</em></small>

    1. Save the file to your local machine with a name like `OGS Color Palette.gpl`

    2. Place the file into the user palettes folder, which can be found via **Edit > Preferences > System > User Palettes**{: .label }

    


## Install Course Terrain Tool

[Course Terrain Tool](/tools/utilities/course-terrain-tool) is an open-source tool created by OpenGolfSim to source and process real-world lidar point-cloud data into usable terrain data for your golf course. It also downloads and processes satellite and hill-shade imagery to aid in course design.

<a href="/tools/utilities/course-terrain-tool" target="_blank" class="btn">Download Course Terrain Tool</a>


## Install Course Meshery

[Course Meshery](/tools/course-building/terrain.md) is an open-source tool created by OpenGolfSim to generate course meshes from SVG and raw terrain data files.

<a href="/tools/utilities/course-meshery" target="_blank" class="btn">Download Course Meshery</a>


## Course Publisher Account

You'll need access our online course publishing tools. You can request access for your OpenGolfSim account on our course building Discord channel.

<a class="btn" href="https://discord.gg/9JqxNArQ" target="_blank">#course-building Discord Channel</a>

---

<!-- [Next up: Install OpenGolfSim SDK Package](/tools/unity-sdk){: .btn } -->