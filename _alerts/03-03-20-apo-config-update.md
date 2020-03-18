---
layout: post
title: "Aporeto Configuration Update"
date: 2020-03-03 15:00:00 +0000
categories: OpenShift alert
---

Today Tuesday (Mar 3rd, 2020) at 3:00PM PST we will change some configuration of the enforcers on the three infrastructure (infra) nodes. This change will fix an issue where the enforcers get overloaded and are unable to keep up with traffick.

The above mentioned outage will take approximately 15 minutes. During this window regular workload **will be** impacted as follows:
- Any in-flight external network connections will be terminated while the enforcers restart to pickup new configuration.

If your application requires the high level of security provided by Aporeto please take measures to mitigate the risk to these application. A final update will be posted in #devops-alerts once maintenance is complete.
