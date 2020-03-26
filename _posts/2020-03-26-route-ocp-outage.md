---
layout: post
title: "OpenShift Service Disruption"
date: 2020-03-26 12:34:00 +0000
categories: openshift outage update
---

**What Happened**

At ~11:30am today we became aware of an issue causing system wide service degradation to the OpenShift Container Platform (OCP) as well as hosted applications and shared services such as SSO and RocketChat. Through investigation it was determined the issue was caused by the same router pod (HAProxy) issue that we had several days ago. 

We opened a conference bridge that included Platform Services, DXCAS, RedHat, and Arctiq where we collectively worked to troubleshoot the issue.

At ~11:59am we determined the HAProxy was starved for resources (CPU / threads); this was likely due to increased traffic (starting March 19th) from additional COVID-19 related load over the last week. To remedy the issue we increased the number of threads for the router pods.

At ~12:04pm a fix was implemented resorting normal operation to the platform.

**Going Forward**

The technical team including Platform Services, DXCAS, RedHat, and Arctiq will schedule a technical conference call to determine how to better architect the routing so it is better spread over the three infrastructure nodes making it more resilient as well as responsive to increased load.
