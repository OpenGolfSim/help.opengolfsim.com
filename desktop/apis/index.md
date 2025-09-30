---
parent: OpenGolfSim Desktop
title: Developer API
thumbnail: /assets/white_256x256.png
---

At OpenGolfSim, we believe in being as transparent and developer friendly as possible. We think this helps grow an active and engaged community and empowers more users to build cool things. 

Below you'll find documentation for our developer API. It's still in the early stages, so check back often for updates.

Have a feature or API idea? Want to nerd out? Come drop us a line on our <a href="/connect-with-us">Discord</a>, we'd love to see what you're building!


1. TOC
{:toc}


### TCP Connection

Our Developer API allows for simple TCP communication on port `3111` to communicate with the OpenGolfSim app programmatically. This makes it easy to create your own experimental integrations, launch monitor connectors, or other custom automation.

| --- | --- |
| Host | `127.0.0.1` |
| Port | `3111` |

{: .tip }
> If connecting over the network, you can also use the local IP of your machine (e.g. `192.168.x.x`)


Once you've established a connection, you can send and receive JSON payloads to interact with the API.



### Events

The API server will send JSON messages over the TCP connection, which you can look for and process for your own app. Below is a list of the events that are sent to any active TCP connection.

#### Shot Result

After a shot has been completed in OpenGolfSim Core connected sockets will receive a `result` event with some stats about the shot from the simulator. This is useful for displaying or recording shot data in your own application.

```json
{
  "type": "result",
  "result": {
    "carry": 220.0,
    "total": 221.5,
    "roll": 1.5,
    "height": 48.1
  },
  "shot": {
    "ballSpeed": 128.5,
    "horizontalLaunchAngle": 2.4,
    "verticalLaunchAngle": 2.4,
    "spinSpeed": 2002,
    "spinAxis": -1.2
  }
}
```

#### Player Change

When a new player is up, this event will fire and include some details about the player's current state in the game.

```json
{
  "type": "player",
  "player": {
    "name": "Fry",
    "id": "1234-5678-9101-11"
  },
  "state": {
    "score": 8,
    "hole": 4,
    "distanceToPin": 224
  }
}
```

### Code Examples

Here are a couple code examples, to give you a better idea of how to send and receive data:

{% tabs log %}

{% tab log node.js %}

{% capture js_example %}
{% include api-example-js.md %}
{% endcapture %}
{{ js_example | markdownify }}

{% endtab %}

{% tab log python %}

{% capture py_example %}
{% include api-example-python.md %}
{% endcapture %}
{{ py_example | markdownify }}

{% endtab %}

{% endtabs %}