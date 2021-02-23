---
layout: post
title: Silver Cluster Login Failures
date: 2021-02-23 14:54:00 +0000
categories: openshift outage
---

# Login Failures into Silver Cluster

Today between approximately 12:45PM and 2:00PM users were not able to authenticate against the Silver cluster.
This was due to a bad config within the SSO realm used for Openshift Authentications. It was quickly found and resolved. There was no impact to other client applications and realms. 

## What was the issue?

The issue was due to an empty authentication flow execution for `post-broker login` with Github. When the empty authentication flow was removed and or properly configured, the Silver cluster login behaved normally.


## Retrospective

This issue brings to light a few things that teams should consider when configuring their realms:

1. Pay careful attention to your custom authentication flows and ensure, when created, that they are configured correctly. 
2. Have a backup plan for accessing your realm. If you break the authentication flow for a given provider you should still have admin access to your realm to resolve the problem. This can be in the form of using an alternative IDP or having a local admin user login. 

## Next Steps

We've identified some next steps for preventing or mitigating issues like these in the future:

1. Automated scheduled testing of a login flow to ensure cluster access is working as well as having a quicker time-to-detect

2. Sharing this retrospective with parties involved in administering the realm that was involved with this incident.

