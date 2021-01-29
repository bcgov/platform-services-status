---
layout: post
title: "OpenShift Partial Outage"
date: 2021-01-29 18:54:16 +0000
categories: openshift outage update
---

On Thursday January 28th, 2021 there was a partial outage of the OpenShift Container Platform (OCP) from ~13:22 PST to ~16:17 PST. Details of the incident are as follows:

# TL;DR
 
In October we applied “Workaround 2” from [https://access.redhat.com/solutions/5448851](here) to the clusters to resolve an issue with the k8s API. According to the knowledge base, that bug should be fixed in v4.5.16+. The Silver cluster is running v4.5.20 so, as part of CHG0022285, we rolled back "Workaround 2" which triggered the issue.

# Play by Play 

13:22 Alerts were triggered that the cluster was unhealthy and some CronJobs were failing.

13:36 First reports of issues from users.

13:40 Posed in #devops-ocp4-migration that the issue is being investigated.

13:47 Tagged our Technical Account Manager (TAM) from Red Hat in #devops-operations and start posting findings and logs.

14:13 Attempt a rollback of the mornings change, but since pods are failing to start, the operation hangs.

14:23 Updated the Status Page

14:25 Opened a Sev1 case with Red Hat. Opened an INC and began reaching out to AdvSol Situation Management to escalate to a P2.

14:39 Internal group chat with DXC Advanced Solutions team members.

14:42 Posted to #internal-platform-services to alert Platform Services (P.S) team members.

14:50 Follow up with TAM

14:51 Posted a notice to #devops-alerts

15:11 Advise additional Red Hat team members of teh situation.

15:35 TAM arrives in chat and starts asking for data/logs

16:05 Made changes to the API server similar to Workaround 1 from the KB upon direction from Red hat and force a rollout of the API server.

16:08 First API server starts up and users start reporting recoveries.

16:16 Announce in #devops-alerts that things appear to be improving

16:17 All API pods have now rolled out

### How did we resolve it?

Opened a case with Red Hat and followed their directions. It is unclear if the fix is due to rolling back the change, or the additional settings tweaks that were made.

### Any specific challenges / delays in resolving?

Red Hat took more than the 1 hour SLA for Sev1 cases to respond.

### Who did it affect and how?

- The Kubernetes API became slow or unresponsive. Applications like Patroni that have a heavy reliance on the API failed.

- New pods were unable to start up, reducing resiliency. New storage could not be provisioned.

- Already running applications that do not rely on the API (like RocketChat) remained functional.
