---
title: Range Games
parent: Course Building
nav_order: 2
published: false
---

Range games are simple turn based games where players get multiple shots from the same spot and earn points by getting their shots to land on specific targets. You can build and sell your own range games in the OpenGolfSim store. Below you'll find a guide on building a game of your own.

### Getting Started

Building your own Range Game for OpenGolfSim is easy.

1. Create a new Unity 6.2 HDRP project, or start with one of our starter templates. Starter templates can be found in the [Downloads](https://opengolfsim.com/account/downloads) sections of your OpenGolfSim developer account.

    {: .note }
    > Tools will only display in your Downloads list if you're actively enrolled in our developer program

2. If you're starting a new Unity project from scratch, install our SDK by dragging the **OGS Unity SDK** files into your new project's `Assets` folder. If you're using a starter template, these files should already be present in your project assets.

4. Create an empty game object named `StartPoint` and position it in the scene where you want your player to hit from.
5. Create an empty game object named `AimPoint` and position it in the scene where you want your player to aim initially.

