---
layout: post
title: "Trident Provisioner Temporarily Disabled"
date: 2020-10-09 11:45:00 +0000
categories: openshift update
---

As an ongoing action to yesterday's Service Outage, the Trident Provisioner Service for Openshift 3.11 is being turned off while we look to resolve the issue. 

This issue does **not impact current pvcs**. 

## Impact

- no new netapp pvcs will be provisionable while the Trident Provisioner is turned off
- this will likely impact your development/promotion to production services if you are planning on provisioning **new** pvcs 

## How long will provisioning be disabled?

We will post an update about the timeline as soon as we hear back from NetApp support that is testing a downgrade path for us.

## What can you do in the mean time?

- If being unable to create **new** pvcs is causing blockers for your development, as a temporary work around you can switch to ephemeral storage for services that require data. This is something that you should do for **DEV** environments only - do not plan on promoting your infrastructure changes as this is a temporary work around

- If you are experiencing an emergeancy due to being unable to provision **new netapp volumes** contact #devops-operations to discuss options. Please provide details such as
  - project/namespace
  - deployment
  - team
  
