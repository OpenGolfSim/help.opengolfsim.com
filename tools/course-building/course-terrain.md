---
title: 1. Course Terrain
parent: Course Building Guide
nav_order: 1
---

## Create Course Terrain

The first step in your course building journey will be choosing to build using real-world or fictional course terrain.

1. TOC
{: toc }

### Fictional Terrain

You can create a completely fictional course terrain by creating blank terrain object and shaping it using the built-in terrain tools in Unity. This will give you the most control over your course and allow you to design your course from the ground up.

1. In your Unity project, right-click in your Hierarchy on the left and select **3D Object > Terrain**{: .label } to add a new terrain object to the scene.

2. Set the terrain size to the size of your course in meters. For example, if you want to create a course that fits within 1 square kilometer, you would use a terrain size of `1000` by `1000` (meters).

3. At this point you could start to create your [Course Map](./course-map) and layout a few holes of your course. From Inkscape, you can export a high resolution PNG or TIFF file. You can then import that as the terrain's image texture, to give you some visual reference points for modeling your terrain.

4. You can use the built-in Unity terrain tools to raise/lower and shape your course terrain. You can also use various environment building tools from the Unity Asset Store to more easily create and model your terrain. Visit our course building channel on [Discord](/connect-with-us/) to discuss and share tools and techniques.

5. When you are happy with your terrain shape, export a RAW file which you'll use later in the mesh steps.

### Real World Terrain

You can source real world, public domain terrain data from around the world using [Course Terrain Tool](/tools/utilities/course-terrain-tool), one of our free course building tools.

1. Open Course Terrain Tool and zoom to the area you want to capture.
2. Hold shift while clicking the map to set the center of your capture area
4. Drag the slider to change the size of your capture area.
    <small>Note: Terrain data must be a square, so you'll need to drag and adjust to find the smallest square that fits your course within it.</small>

5. Search for lidar data or import LAZ files to the map directly

6. Click **Export**{: .label } and Configure your export


{: .warning-title }
> Copyright Notice
>
> When submitting your course to our course store, it must comply with all applicable copyright laws to be approved. We are additionally required to respond to all DCMA copyright violation requests. Reach out to find out more about what is and is not allowed.

#### Video

<iframe width="560" height="315" src="https://www.youtube.com/embed/H5YyLU_PCIo?si=U_yOlw89b6tEq6C8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

#### Unity Import

1. In Unity, import your .RAW terrain file you created in Course Terrain Tool in the terrain settings.

    1. Select or create a terrain object in your scene.
    
    2. Click the terrain settings in the inspector

    3. Select **Import Raw**{: .label } and locate the `.raw` file from your Course Terrain Tool export.

    4. Confirm that **Byte Order** is set to `Windows`.

    5. Confirm that **Terrain Size** match your stats file.

    6. Click **Import**{: .label }

2. Import your Bing or Google TIFF image and update the max resolution to 8192.

    1. Drag the `Overlays/` folder from your Course Terrain Tool export into your Unity project's assets.

    2. Click the satellite image file you want to use and the inspector change the max resolution to `8192x8192` and click **Apply**

    3. Select the terrain object in your scene and in the inspector go to the **Paint Terrain** tab and select **Paint Texture** from the dropdown.

    4. Click **Edit Terrain Layers**{: .label } and select **Create Layer**


4. You can now edit, dig, and smooth-out your course terrain using Unity's built-in terrain tools.

---

[Next up: Course Map](/tools/course-building/course-map){: .btn }