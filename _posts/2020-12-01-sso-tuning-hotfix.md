---
layout: post
title: "SSO Tuning Hotfix"
date: 2020-12-01 20:00:00
categories: sso update
---
A hot fix is scheduled for the BCGov Redhat SSO instance in the dev, test, and prod environments later this evening. There are remediatory actions being taken
to prevent the service degradation issues that have recently been affecting the service.

## More Information
- Approximate Time of Change: Dec 01 2020 8PM PST
- Type of Change: hotfix
- Service Bulletin No: n/a
- Impact Notes:
- we will be rolling changes through environments in order (dev, test, prod) and only rolling through to the next environment on verification of successful rollout of the previous one
- the expected service downtime for each environment is minimal. We expect a service downtime in each environment to be ~10 minutes.
- Clients holding long lived sessions will experience a disruption as their sessions will be terminated. Clients will need to re-authenticate against sso after the rollout
- Clients utilizing offline tokens may experience issues. This is commonly resolved by refreshing your browser cache (ctrl+shift+r) or closing your tabs and reopening your browser.
