---
parent: OpenGolfSim Desktop
title: Third-Party Software
nav_order: 7
thumbnail: /assets/appicon.svg
---

Some features of OpenGolfSim Desktop unofficially integrate with other third-party simulator software, like GSPro. Below you'll find some tips and tweaks to make these apps work better with OpenGolfSim.

# AwesomeGolf &amp; E6 Connect

OpenGolfSim does not currently support Awesome Golf or E6 Connect.

# GSPro

OpenGolfSim has some experimental support for GSPro.

Some button actions on the control box or mobile app require settings to be enabled in GSPro before they'll function correctly. If these features aren't turned on, corresponding buttons (like Mulligan or Aim) won’t do anything in-game.

This page shows how to enable the most commonly used features so everything works as expected.

{: .note }
> Shots that complete a hole do not register as shot data in GSPro's logs. We're working on a solution to this, but currently the final shot of each hole won’t be captured.

---

## Mulligan Button: Enabling Mulligan Functionality

To make sure the mulligan button works during a round:

1. Launch any course in GSPro (this setting only appears once a course is loaded).
2. Go to **Settings > Round Settings > Mulligan**.
3. Set **Mulligans** to **Yes**.
4. Save and exit.

<!-- <img src="/assets/OGS_Documentation/mulligan.png" width="100%" style="max-width: 1000px;" /> -->

{: .note }
> If you don’t load a course first, you won’t see the mulligan setting in the menu.

---

## Distance Buttons: Enabling Distance and Aim Indicators

To enable aim guidance and make distance adjustments possible:

1. Go to **Settings > Visual Settings**.
2. Enable **SHOW AIM INDICATOR**.
3. Save and exit.

<!-- <img src="/assets/OGS_Documentation/show-aim-indicator.png" width="100%" style="max-width: 1000px;" /> -->

---

## Additional Suggestions: Optimizing Visual Feedback

These tweaks help you get better on-screen feedback when using distance-related controls:

1. Stay in **Settings > Visual Settings**.
2. Enable **DISTANCE DISPLAY**.
3. Set the display location to **UP** for easier visibility during play.
4. Save and exit.

<!-- <img src="/assets/OGS_Documentation/display_distance.png" width="100%" style="max-width: 1000px;" /> -->

---

If something’s still not working after adjusting these settings, [contact us](/contact) and we’ll help you sort it out.
