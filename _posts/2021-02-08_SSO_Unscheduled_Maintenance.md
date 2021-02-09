---
layout: post
title: "SSO Unscheduled Maintenance"
date: 2021-02-08 18:30:00 +0000
categories: sso
---

On the morning of February 8th 2021, the SSO service experienced some degradation between 9:30AM and 11:45AM. This was due to a rapid increase in network traffic from some SSO Clients. 

A typical day for the SSO service includes an average network traffic of ~2.5Mb/s. This morning we experienced traffic on average of >5Mb/s and spiking to 34Mb/s. 

This caused some SSO pods to lag behind in accepting in connections which cascaded into the slugishness of the service.

## Actions Taken

- we boosted the cpu request and limits of SSO's dependant components to mitigate service degradation in the following days and are working with teams to better utilize
the SSO api to prevent this from happening in the future!
