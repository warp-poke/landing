---
title: "About Page"
description: "All About poke"
date: "2018-08-23"
type: "about"
layout: "single"
categories:
    - "bio"
    - "about"
    - "meta"
tags:
    - "bio"
blurb: "an Open Source and Highly Scalable Web Monitoring Solution"
recentposts: 0
recentprojects: 0
photo: "/poke-avatar.png"
# cardheaderimage: "/images/default.jpg" # optional: default solid color if unset
cardbackground: "#ff0066" #optional: card background color; only shows when no image specified
---

#### Goals

Poke has been designed to monitor hundreds of thousands web sites in an efficient and operable manner. Relying on Time Series, and more specificaly Warp10, Poke leverages advanced sliding window algorithms to alert on trends instead on basic checks and thresholds. This metrics approach opens your web monitoring to anomaly detection, outlier, prediction, etc.

#### Components

Poke infrastructure has been designed to reuse a maximum of a Warp 10 infrastructure components like Apache Kafka and Apache HBase, reducing new dependencies like databases. From a helicopter perspective, the architecture is based on a scheduler that generates check requests for each web sites or domains. These check requests are sent to a Kafka topic that will be consumped by agents dedicated to differents checks like DNS, HTTP and SSL.

#### Open Source & Contributions

Poke is a collaboration effort between multiple companies that had a similar need. Contributions are welcomed and discussions happen on [gitter](https://gitter.im/warp-poke/Lobby).

Furthermore, there is a periscope live from Criteo Paris' meetup about Poke:

- [https://www.pscp.tv/waxzce/1OwGWEEvapkxQ](https://www.pscp.tv/waxzce/1OwGWEEvapkxQ)
