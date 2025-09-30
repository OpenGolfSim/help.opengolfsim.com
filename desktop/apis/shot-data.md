---
title: Shot Data API
parent: Developer API
nav_order: 1
thumbnail: /assets/appicon.svg
---

# Sending Shot Data

This article outlines integrating a custom launch monitor connector using our Developer API.

## Connect

First create a new TCP socket and connect to it.

- Host: `127.0.0.1`
- Port: `3111`


## Payload

The TCP socket expects JSON payloads with a `type` key and one of the following event types:


## Device Status

You can indicate the device's status by sending a `ready` or `busy` event type.

*An example payload for indicating a launch monitor is ready to receive shots:*

```javascript
{
  "type": "device",
  "status": "ready"
}
```

*An example payload for indicating a launch monitor is busy:*

```javascript
{
  "type": "device",
  "status": "busy"
}
```

## Shot Payload

### `type`
- `shot` - The message type for shots

### `unit`
- `metric` - Indicates meters per second for speed and distances (default).
- `imperial` - Indicates the values are in miles per hour and yards for speed and distances.

Note: If no unit is supplied, then `metric` will be assumed.

### `shot`
- `ballSpeed` - The ball speed in miles per hour (`imperial`) or meters per second (`metric`)
- `verticalLaunchAngle` - The vertical launch angle of the shot. Should be between 0&deg; and 45&deg;
- `horizontalLaunchAngle` - The horizontal launch angle of the shot. Should be between -45&deg; and 45&deg;
- `spinSpeed` - The ball spin speed in rotations per minute (RPM)
- `spinAxis` - Spin axis. Values should be between -45&deg; and 45&deg;

*An example payload for a shot in imperial units:*

```json
{
  "type": "shot",
  "unit": "imperial",
  "shot": {
    "ballSpeed": 101.2,
    "verticalLaunchAngle": 15.4,
    "horizontalLaunchAngle": -2.1,
    "spinSpeed": 3021,
    "spinAxis": -0.5
  }
}
```

*An example payload for a shot in metric units:*

```json
{
  "type": "shot",
  "unit": "metric",
  "shot": {
    "ballSpeed": 44.704,
    "verticalLaunchAngle": 15.4,
    "horizontalLaunchAngle": -2.1,
    "spinSpeed": 3021,
    "spinAxis": -0.5
  }
}
```

