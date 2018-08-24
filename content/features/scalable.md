---
title: Scalable
description: 'Horizontal scalability'
date: 2018-08-23T13:35:58Z
categories:
  - feature
tags:
  - scalability
  - distributed
  - big data
author:
  github: "https://github.com/warp-poke"
  image: "/poke-avatar.png"
  name: "Poke"
  website: "https://poke.digital/"
cardbackground: "#ff0066"
---

Poke rely heavily on Warp10, a very scalable platform for Time Series, and tries to reuse the same components to avoid complexifying the operational stack.
It also comes with additional components like the Poke Scheduler, Poke Us, Poke Me and Poke UI.

![Poke - Architecture](/features/architecture.png)


##### Apache Kafka

Apache Kafka is a horizontally scalable and fault-tolerant distributed streaming platform. Kafka is used by poke to distribute checks to agents, enabling : 

  * Scaling agents through partitions
  * Using multiple groups to enable checks from different zones

Kafka is also used as an ingestion buffer in Warp10.

##### Apache HBase

Apache HBase is the Hadoop database : a distributed, scalable, big data store. It can achieve massive scalability with thousands of nodes.
Warp10 currently uses HBase as its distributed store

##### Warp10

Warp10 is composed of multiple components : 

  * `Directory` for series indexing
  * `Ingress` for ingestion parsing and pushing to Kafka
  * `Egress` that runs the WarpScript engine
  * `Store` that consumes Kafka and stores into HBase

Each Warp10 components can be run multiple times to distribute the load and ensure having no SPOF.

##### Poke scheduler

The Poke scheduler is sharded and rely on Zookeeper to ensure the distribution of checks scheduling.
