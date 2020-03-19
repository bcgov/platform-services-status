---
layout: post
title: "Nginx Build Issues"
date: 2020-03-11 14:00:00 +0000
categories: openshift outage update
---

Today at approximately 2PM an issue was identified in a commonly used nginx Dockerfile. This nginx Dockerfile was changing the permissions of /etc to be wide open; this conflicted with a directory injected by our container scanning tool Aqua and caused builds to fail.

To remedy this the community has come together and identified a fix: Teams that have identified this issue will fix it on the fly. If you have this problem and don't yet know it expect a PR to show up in your repository shortly.

If you need immediate help ask "how do I fix the nginx /etc permission problem in my build" in the `#devops-how-to` of **RocketChat**; The community will chime in and sort you out.
