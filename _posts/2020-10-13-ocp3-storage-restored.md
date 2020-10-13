---
layout: post
title: "Trident Provisioner Temporarily Disabled"
date: 2020-10-09 11:45:00 +0000
categories: openshift update
---
 Trident Service for NetApp storage provisioning on Openshift 3.11 has been turned on again at noon on Tuesday Oct 13, 2020.

## What is happening?
 
Following the Trident Storage provisioning service upgrade failure on Thursday Oct 8, the storage provisioning has been turned off on the Platform on Friday Oct 9 while we investigated the issue. Turning off the storage provisioning had no impact on existing production applications that already had storage provisioned. However, no new NetApp storage provisioning requests could be served while the Trident service was turned off.
We worked with the NetApp support team to come up with a remediation plan for the failed Trident upgrade and their recommendation was to downgrade the Trident service on the Platform to the previous stable version.
 
The  downgrade of the Trident service on the Platform will be implemented today Oct 13 at noon and following the downgrade the Trident service will again be enabled on the Platform.
 
## Impact

There will be no impact on existing applications. Once the Trident service is turned on on the Platform, new PVC provisioning will be enabled again.
 
## What can you do to help?

Following the announcement in #devops-alerts channel, that the Trident Storage Provisioning Service is turned on, verify that you can create a new PVC in your development environment and let us know in #devops-operations channel if you run into any issues.

