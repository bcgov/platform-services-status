---
layout: post
title: SSO Dev Gateway Timeout (504)
date: 2021-02-26 16:07:00 +0000
categories: sso update
---

# SSO Dev - Gateway Timeout (504)

Today between approximately 3:30PM and 4:00PM users access [SSO Dev](dev.oidc.gov.bc.ca). They would get a 504 Gateway Timeout response.

## What was the issue?
Earlier today SSO Dev was patching its network policies to coincide with the Dev Network Policy Migration from Aporeto to K8s Network Policy. The installation of K8s policies was missing a Aporeto policy as described in the [migration docs](https://developer.gov.bc.ca/Networkpolicy-Migration-Workshop). The pull request review for this migration also failed to catch the issue [#187](https://github.com/bcgov/ocp-sso/pull/187).


## Retrospective

This issue occured because we erroneasly ignored Aporeto specific policies that were to be installed based on the [migration guide](https://github.com/bcgov/networkpolicy-migration-workshop/blob/main/quickstart.yaml). We've since made a PR to the repo to make it more clear that you should not ignore the excellent instruction Jason has left all of us :) 

https://github.com/bcgov/networkpolicy-migration-workshop/pull/9

