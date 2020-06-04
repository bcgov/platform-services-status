---
layout: post
title: "Platform Service Priority Update - June 2020"
date: 2020-06-03 13:31:00 +0000
categories: openshift update
---


## What’s changing?

Effective immediately, we’re moving back to our standard maintenance schedule.  All operational maintenance on the platform will occur during day-time office hours.

## Why?

We temporarily shifted to after-hour maintenance (March 16 – May 31) to accommodate urgent requirements for COVID-19. Several rapid-turnaround projects required a level of availability that was not yet built into their application design. Project teams have worked hard to re-architect and have now successfully built in high resiliency by distributing their applications across nodes.

Over the past few years working with the community within a containerized environment, we have learned as a community that unlike with traditional server maintenance, containerized environments by their very nature are ephemeral (lasting for a very short time) and by design require elasticity to grow and shrink in real time.

Operationally, this means that nodes (servers) must be drained, at times even daily to support application health, depending upon various circumstances.  We will continue to work closely with line of business apps that have been identified to us as critical to ensure that their application configurations are properly configured.
This best-practice allows your team to be present and troubleshoot quickly--affording maximum safety for all applications and projects in our community.

As always, you’ll be notified of maintenance in advance via Rocket.Chat in the `#devops-alert` channel.

## How you can help


### Resilient Applications

If you think your application is not ready to withstand maintenance activities i.e. it uses single node deployment pattern, please ask your development team to check out our new [Application Resiliency Guidelines](https://developer.gov.bc.ca/Resiliency-Guidelines) for best practices in application design and reach out to the Platform Community in RocketChat for help if needed.

Resiliency is a shared responsibility.  Platform Services Team builds and operates the resilient foundation, the OpenShift Platform, then you choose to enable relevant services in your business applications to help with your resiliency needs.


### Keep us Informed

Keep us informed about major milestones for your project. If you have an important launch coming up and you are not sure your application can provide undisrupted continuity of operations during a scheduled maintenance, let the Platform Services Team know in `#devops-operations` channel and we will work with you to ensure your business service is uninterrupted.


### Frequently and Open Communication

If you have any questions or concerns about support activities happening on the Platform or the approaches that we are taking to run these activities, please let me know. You can find me in RocketChat or send me an email.  We are building the Platform together as a community and you, as a valued partner, have an important role to play in shaping this service.

### Come to our Sprint Reviews!

We run 3 week Sprints and have a Sprint Review at the end of each Sprint where we share our accomplishments and future plans for the Platform. Please find time in your busy schedule to attend those sessions as it is the best opportunity to stay up to date on what’s happening on the Platform and provide your input into choosing a direction for growing and expanding the Platform. Let me know if you didn’t receive an invite for the Platform Services’ Sprint Reviews.

### Contribute 

Contribute your development resources to building new ways to better communicate.

We have been asked to add other communication channels for maintenance updates such as posting in MS Teams or sending an email. However, as our small team is fully focused on Platform maintenance and OpenShift 4 Build-Out, we don’t have a capacity at the moment to take upon this new development. If you have spare capacity in your team and are willing to contribute to improving the communications on the Platform, please let me know.

I am looking forward to hearing back from you!

Thanks,
Olena Mitovska | Product Owner for Platform Services