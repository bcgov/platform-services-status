---
layout: post
title: "Trident Provisioner Temporarily Disabled"
date: 2020-10-09 11:45:00 +0000
categories: openshift update
---

As an ongoing action to yesterdays Service Outage. The Trident Provisioner Service for Openshift 3.11 is being turned off while we look to resolve the issue. 

This issue does **not impact current pvcs**. 

## Impact

- no new netapp pvcs will be provisionable while the Trident Provisioner is turned off
- this will likely impact your development/promotion to production services if you are planning on provisioning **new** pvcs 

## How long will provisioning be disabled?

***

## What can you do in the mean time?

If being unable to create **new** pvcs is causing blockers for your development. As a temporary work around you can switch to ephemeral storage for services that require data. This is something that you should do for **DEV** environments only. 


