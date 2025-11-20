---
title: Course Meshery
parent: Utilities
category: tools
nav_order: 2
---

# Course Meshery

<img src="/assets/course-building/meshery_icon_512x512.png" alt="Course Meshery" srcset="/assets/course-building/meshery_icon_512x512.png 2x" />


**Course Meshery** is an open-source tool, created by OpenGolfSim, that converts a course SVG file and raw terrain file as input and exports a collection of meshes that conform to the terrain height. This makes it easy to layout your golf course in a vector program, like <a href="https://inkscape.org/" target="_blank">Inkscape</a> and automatically generate 3D models you can easily import on top of your terrain into Unity.


<a target="_blank" class="btn btn-icon btn-green" href="https://github.com/OpenGolfSim/course-meshery/releases/latest/download/meshery-windows.zip">
  <img src="/assets/icons/windows.svg" width="24" />
  <span style="margin-left: 3px;">Download for Windows</span>
</a>
<a target="_blank" class="btn btn-icon btn-green" href="https://github.com/OpenGolfSim/course-meshery/releases/latest/download/meshery-macos.zip">
  <img src="/assets/icons/apple.svg" width="24" />
  <span style="margin-left: 3px;">Download for Mac</span>
</a>
<a target="_blank" class="btn" href="https://github.com/OpenGolfSim/course-meshery">View Project on GitHub</a>

---

### Generating Meshes

To generate your meshes:

1. Open **OGS Meshery**
2. Set the **SVG file** for your course
3. Set the **RAW terrain** file for your course
  - If you made any changes to the terrain in Unity, make sure you export a new RAW file from your terrain settings.
4. Set the **Output Folder** we should write the meshes to.
5. Set the terrain **height scale**. (Usually found in your terrain stats CSV file)
6. Click **Generate Meshes** to start the process.
7. Once completed the generated OBJ files should be found in the output folder you selected.

The OGS SDK for Unity contains an import tool for automating the process of importing these meshes and batch assigning their materials. Follow the Unity SDK guide for importing and customizing meshes.

{: .warning }
> Note: Fow now, after importing the obj files into Unity, you likely need to manually reposition the imported mesh to line up with the terrain. It should be some variation of the terrain width height set on the x,z values in unity (try positive negative or halving the width/height). We're still working on this bug.

