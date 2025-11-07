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
- `imperial` - (default) Indicates the speed values are in miles per hour
- `metric` - Indicates the speed is supplied in meters per second

Note: If no unit is supplied, then `imperial` (MPH) will be assumed.

### `shot`
- `ballSpeed` - The ball speed in miles per hour (`imperial`) or meters per second (`metric`)
- `verticalLaunchAngle` - The vertical launch angle of the shot. Should be between 0&deg; and 45&deg;
- `horizontalLaunchAngle` - The horizontal launch angle of the shot. Should be between -45&deg; and 45&deg;
- `spinSpeed` - The ball spin speed in rotations per minute (RPM)
- `spinAxis` - Spin axis. Values should be between -45&deg; and 45&deg;

*An example payload for a shot in MPH:*

```json
{
  "type": "shot",
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


## Shot Result

When a shot is completed in the simulator, the Developer API will send a result event with some details about the shot. Note that at the time of writing result data will always be stored/sent in meters.

```json
{
  "type": "result",
  "data": {
    "result": {
      "carry": 196.06776428222656,
      "height": 18.728025436401367,
      "roll": 6.482479572296143,
      "total": 202.54876708984375,
      "lateral": -0.07558325678110123
    },
    "club": {
      "name": "5W",
      "id": "5W",
      "distance": 205
    },
    "shot": {
      "ballSpeed": 135,
      "verticalLaunchAngle": 11.100000381469727,
      "horizontalLaunchAngle": 1.2000000476837158,
      "spinAxis": -2.5,
      "spinSpeed": 4800
    },
    "sessionId": 22
  }
}
```