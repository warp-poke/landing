---
title: Agents
description: 'Operators which create metrics from your domains'
date: 2018-08-23T13:35:58Z
repo: https://github.com/warp-poke/poke-me
categories:
  - feature
tags:
  - agents
  - dns
  - http
  - ssl
author:
  github: "https://github.com/warp-poke"
  image: "/poke-avatar.png"
  name: "Poke"
  website: "https://poke.digital/"
cardbackground: "#ff0066"
---

Agents are operators which create metrics from your websites at regular interval. In addition, they create metrics by zone where the agent is deployed.

A zone is a concept affiliated to the team or enterprise whom deploy agents. Generally, each agent is deployed on each zone used by the team or enterprise.

##### HTTP

The HTTP agent scrapes your websites in order to extract the response status and time. This agent emulates the user's traffic. In that way, the agent is able to detect, if your websites are reachable or not and how many times it can take from the zone to access your websites.

##### DNS

This agent is designed to scrape the zone of the DNS that answer the DNS request and the lookup response time. By requesting DNS, the agent is able to provide useful information about websites in order to detect slow or unreachable DNS.

##### SSL

The SSL agent is created in order to know the grade of your certificates and the his expiration date. From that, it can detect if your certificates are expiries.
