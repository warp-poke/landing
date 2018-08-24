---
title: High performance
description: ''
date: 2018-08-23T13:35:58Z
categories:
  - feature
tags:
  - performance
author:
  github: "https://github.com/warp-poke"
  image: "/poke-avatar.png"
  name: "Poke"
  website: "https://poke.digital/"
cardbackground: "#ff0066"
---

##### Why being highly efficient?

Monitoring is first class citizen while running any kind of service or infrastructure. Workloads can grow fast and it's important for the monitoring solution to support this growth without being rethought every month so we can concentrate on the customer value. An other good reason is the cost ratio between the service and the monitoring cost to ensure your service is fine.

##### How do we achieve performance

There are mainly two parts in the Poke architecture : the scheduler and agents.

The scheduler is implemented in Akka to benefits from an actof model and its concurrency model. A JVM based language makes it easy to integrate with Warp10 components. Most of the agents are implemented in Rust at the exception of the SSL one that is built around the SSLLabs Golang library. 

Performance is a subjective topic, and choosing a language is a compromise between performance, productivity, ease of maintainability, etc. Early Poke contributors were fluent with JVM based languages and also Golang and Rustlang. The choice of Rust by default for agents is justified by the workload of an agent : it needs concurrency, performance and low footprint. Rust is probably the best language today for performance & productivity developement while offering safe mecanisms.