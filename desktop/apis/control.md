---
title: Control API
parent: Developer API
nav_order: 2
---

# Control API

In addition to shot data, you can also remotely control your simulator by sending actions over a simple TCP connection.

### Events

For most actions, `press` event will work fine. For some commands, you can also simulate a button being held down by sending the `down` and `up` events separately. 


| Command | Supported Events | Description |
| --- | --- | --- |
| `left` | `press`, `down`, `up` | Adjust the aim to the left |
| `right` | `press`, `down`, `up` | Adjust the aim to the right |
| `up` | `press`, `down`, `up` | Increase the aim distance |
| `down` | `press`, `down`, `up` | Decrease the aim distance |
| `club-up` | `press` | Select the next longest club in the bag |
| `club-down` | `press` | Select the next shortest club in the bag  |
| `drop` | `press` | Take a drop (if available) |
| `mulligan` | `press` | Take a mulligan (if available) |
| `rehit` | `press` | Take a re-hit (if available) |

```json
{
  "type": "control",
  "command": "club-down",
  "event": "press"
}
```

