---
title: "Getting started"
description: "Getting started with poke"
date: 2018-08-23T10:00:00Z
categories:
    - "documentations"
tags:
    - "getting started"
    - "documentations"
author:
  github: "https://github.com/warp-poke"
  image: "/poke-avatar.png"
  name: "Poke"
  website: "https://poke.digital/"
cardbackground: "#ff0066"
---

All Poke's components are hosted on GitHub under the [warp-poke](https://github.com/warp-poke) organisation.

This organisation provides some agents in order to check protocols:

- HTTP: [https://github.com/warp-poke/http-rust-agent](https://github.com/warp-poke/http-rust-agent)
- DNS: [https://github.com/warp-poke/dns-rust-agent](https://github.com/warp-poke/dns-rust-agent)
- SSL: [https://github.com/warp-poke/ssl-go-agent](https://github.com/warp-poke/ssl-go-agent)

Furthermore, there is an API that manage checks and their scheduling:

-  API: [https://github.com/warp-poke/poke-api](https://github.com/warp-poke/poke-api).

##### Start using docker-compose

On the [poke-compose](https://github.com/warp-poke/poke-compose) repository, there is all you need to setup a docker-based poke infrastructure. This infrastructure used the standalone version of each distributed components.

Firstly, get the repository using __git__:

```sh
$ git clone https://github.com/warp-poke/poke-compose.git
```

Once, the repository is cloned, start the infrastructure using the __docker-compose__ command:

```sh
$ docker-compose --project-name poke up

Creating network "poke_default" with the default driver
...
Creating poke_warp_1       ... done
Creating poke_pg_1         ... done
Creating poke_zookeeper_1  ... done
Creating poke_kafka_1      ... done
Creating poke_api_1        ... done
Creating poke_http-agent_1 ... done
...
warp_1        | starting Warp10...
warp_1        |
warp_1        |   ___       __                           ____________
warp_1        |   __ |     / /_____ _______________      __<  /_  __ \
warp_1        |   __ | /| / /_  __ `/_  ___/__  __ \     __  /_  / / /
warp_1        |   __ |/ |/ / / /_/ /_  /   __  /_/ /     _  / / /_/ /
warp_1        |   ____/|__/  \__,_/ /_/    _  .___/      /_/  \____/
warp_1        |                            /_/
warp_1        |
warp_1        |   Revision 1.2.19
warp_1        |
warp_1        | ########[ Initialized with 1000 time units per millisecond ]########
warp_1        | log4j:WARN No appenders could be found for logger (org.eclipse.jetty.util.log).
warp_1        | log4j:WARN Please initialize the log4j system properly.
warp_1        | log4j:WARN See http://logging.apache.org/log4j/1.2/faq.html#noconfig for more info.
warp_1        | Loaded 0 GTS in 11.352754 ms
...
warp_1        | #### standalone.endpoint /0.0.0.0:8080
api_1         | [info] application - Creating Pool for datasource 'default'
api_1         | [info] p.a.d.DefaultDBApi - Database [default] connected at jdbc:postgresql://pg:5432/poke
api_1         | [info] application - ON START
api_1         | [info] play.api.Play - Application started (Prod)
api_1         | [info] p.c.s.AkkaHttpServer - Listening for HTTP on /0.0.0.0:9000
...
```

This output some logs by docker spawned.

Now, poke is started so you can access to the user interface on [http://127.0.0.1:8080](http://127.0.0.1:8080). You should see the [poke-ui](https://github.com/warp-poke/poke-ui):

![poke-ui](/documentations/user-interface.png)

That's all about setup poke using __docker-compose__! Now, it is time to play with the user interface to monitor everything.
