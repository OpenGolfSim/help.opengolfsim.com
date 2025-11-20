---
title: Install OpenGolfSim Tools
parent: Course Developers
nav_order: 2
published: false
---

# Install OpenGolfSim Unity Package

You should start by installing the latest version of the OpenGolfSim Tools package in your new Unity project. The SDK includes tools for importing meshes, batch assigning materials, setting your tee and hole positions, and finally exporting your course file.


1. Open Unity's package manager by selecting **Window** > **Package Management** > **Package Manager**
2. Select the add package (`+`) button and select **Install package from git URL...**
3. Enter the following git repository url (including the `.git` extension):

    ```
    https://github.com/OpenGolfSim/unity-course-scripts.git
    ```
4. Click **Install**
5. You should now see a new **OpenGolfSim** menu under the **Tools** menu.

<img src="/assets/course-building/ogs-sdk-install.jpg" alt="SDK Screenshot" />


{: .tip }
> Want to report a bug or contribute? Our course building tools are open-source and can be found at <a href="https://github.com/OpenGolfSim/unity-course-scripts" target="_blank">github.com/OpenGolfSim/unity-course-scripts</a>


---

[Next up: Build a Practice Range](/tools/practice-range){: .btn }