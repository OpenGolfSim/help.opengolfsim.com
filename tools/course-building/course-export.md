---
title: 4. Course Export
parent: Course Building Guide
nav_order: 4
---

# Course Export

Before we can export and play the new course, we need to define each hole's par, pin locations, and tee position.

1. Add a new Course Details object to your scene. Right-click the **Hierarchy** panel and from the dropdown menu select **OpenGolfSim > Create Course Details**{: .label }. This should add a new game object called `OGSCourseDetails` with an **OGS Course** script attached.

2. With the new `OGSCourseDetails` object selected, you should see some settings in the **Inspector** panel.

3. Expand the **Holes** section and click the **+**{: .label } button to add your first hole. This should add 2 movable handles to the scene, the hole and tee box.

4. Set the Par for your hole. For most par 3 holes, you won't need an aim point. The player will be aimed at the hole position. For par 4 or 5 holes that require an aim point, check the **Aim Point** box.

5. Drag the handles around your course to position the hole, tee (and aim) points on your course.

    {: .tip }
    > Make sure you don't drag the parent game object. At first all the points are added on top of each other, making it hard to drag the correct handle. In that case, just manually enter some random values in the Inspector to move just the points you want first. Then you can drag them around.

6. The points should auto-snap to the ground Y position, but only when they are within 100 or so meters of the terrain. If you can move the point on the Y axis, it's not close enough to snap.

7. Once you have your course laid out. You're ready to export your course build!


---


[Next up: Build Your Course](/tools/course-building/course-export){: .btn }