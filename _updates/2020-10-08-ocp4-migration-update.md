---
layout: post
title: "Platform Service Priority Update - August 2020"
date: 2020-08-05 13:31:00 +0000
categories: openshift update
---

## What's New?
Openshift 3.11 Platform is getting decommissioned and all applications are required to migrate to the new Openshift 4 Platform by end of Feb 2021. 

## Migration Preparation and Support

The Platform Services team will develop migration guides based on the Early Adopter experience and host developer workshops to assist your product teams. In the interim, here are a few things you can do to get started:
 
* Review OpenShift 4.x documentation and release notes [here](https://www.openshift.com/blog/introducing-red-hat-openshift-4).
* Pipeline your deployments. Migration to OpenShift 4.x will be easier based on how developed your build/deploy pipelines are. For fully automated deployment migration efforts should be minimal and measure in hours. 
* Start looking at external dependencies now:
   *   Production Vanity Names (no Pathfinder URLs)
   *   External Service Integration (e.g., firewall rules needed with new cluster?)
   *   State Migration Planning. If you have to move your state/data, how are you going to accomplish it? (no DB replication between OpenShift 3.11 and OpenShift 4.x; will need to be manual push)
* Staffing. Do you have DevOps and Site Reliability Engineer skills available? (hint: you'll need them).
* Keep checking the [OCP 4 App Migration Guide](https://github.com/BCDevOps/OpenShift4-Migration) as it gets updated.
 