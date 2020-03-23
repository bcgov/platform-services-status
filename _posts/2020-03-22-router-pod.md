---
layout: post
title: "OpenShift Routing Issue"
date: 2020-03-23 14:42:00 +0000
categories: openshift outage update
---

One of the three router pods kept crashing. Each time it crashed the
VIP would get moved between the other routers and cause some connection slowness for access to services via Routes. We've disabled the defective pod for now and opened a case with Red Hat.
