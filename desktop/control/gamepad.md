---
title: Button Boxes
parent: Control
nav_order: 2
---
## Physical Control Boxes

Prefer tactile buttons over touchscreen taps? (I know we do) You can hook up a USB gamepad or joystick to your sim PC and use it as a physical control box, either off-the-shelf or DIY.

OpenGolfSim supports most generic USB controllers. Once connected, you can assign button presses to specific simulator functions using the desktop app. This lets you build anything from a simple one button mulligan box to a full featured controller with aim, drop, flyover, pretty much anything you can do from a keyboard, you will be able to easily program.

If you’re building your own, all you need is:

- A basic USB joystick or controller board (e.g. USB encoder board or a micro controller with joystick firmware)
- A few arcade-style buttons or toggles
- A case to mount it in

---

#### Interesting in building your own box?

Checkout our [DIY Button Box build]({% post_url 2024-11-15-gspro-button-box %}) post.

---

## Physical Control Setup

Setting up a physical controller is quick and straightforward, just plug it in and map your buttons.

1. **Connect the device**  
   Plug in or pair your gamepad, joystick, or button box to your PC.

2. **Open OpenGolfSim Desktop**  
   Go to the **Control** section in the app. Your device should appear in the list.  
   If it doesn’t:
   - Close and reopen the desktop app.
   - Unplug the device and plug it back in.
   - Make sure your PC recognizes the device under Windows controller settings. Search "set up USB game controllers"

3. **Device appears in the control panel**  
   Once detected, the device will show up in controls page.

   <img src="/assets/OGS_Documentation/control-setup.png" width="100%" style="max-width: 1100px;" />

4. **Set up the device**  
   Click **Setup Device**, then give it a name so you can easily identify it later.

5. **Assign buttons**  
   Choose an action from the list, click **Assign Button**, then press the button you want to map on your controller.

6. **Repeat as needed**  
   Continue assigning buttons for any actions you want, mulligans, aim adjustments, flyovers, etc.  
   Use whatever layout makes the most sense for your setup.

   <img src="/assets/OGS_Documentation/control-setup-options.png" width="100%" style="max-width: 1100px;" />

7. **ENJOY**  
   Fire up a course and enjoy not having to sprint back to your keyboard every time you want a mulligan.

---
   
If something’s still not working on your setup, [contact us](/contact) Just keep in mind, not all controllers are supported, and some may need extra configuration.
We’re building a list of supported devices as we get more feedback, so stay tuned.
