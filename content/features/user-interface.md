---
title: User interface
description: 'A beautiful and fancy user interface to visualize metrics provided by agents'
date: 2018-08-23T13:35:58Z
repo: https://github.com/warp-poke/poke-ui
categories:
  - feature
tags:
  - user interface
  - ui
  - ux
author:
  github: "https://github.com/warp-poke"
  image: "/poke-avatar.png"
  name: "Poke"
  website: "https://poke.digital/"
cardbackground: "#ff0066"
---

The user interface provides an easy way to visualize metrics provided by agents. It is created in order to fastly highlight websites malfunctions.

Just behind there is an example of what you could see using the poke monitoring system:

![Poke - Google](/features/poke-ui-google.png)

As we can see, there are three __paths__ of the __domain__ google.com answering using HTTPS protocol which are monitored by poke. Furthermore, there are the HTTP response status and latency displayed.

An example of what could appear when a HTTP status error occurred:

![Poke - Error](/features/poke-ui-error.png)

We can see that the HTTP status code has a red background and 404 as status code.
