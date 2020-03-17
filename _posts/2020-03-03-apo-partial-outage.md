---
layout: post
title: "OpenShift Partial Outage"
date: 2020-03-03 15:00:00 +0000
categories: OpenShift outage update
---

An update to Aporeto today had several unintended consequences. This caused a widespread service disruption from approximately 3PM PST to 4:30 PM PST. This disruption may have left some applications in an unstable state.

When Aporeto is restarted it flushes firewall rules. This causes any in-flight network connections to fail. This left applications, including RocketChat, in an unstable state. In addition to this Aporeto was unable to restart successfully. The platform services team has turned down Aporeto until we get a clear resolution from the vender.
