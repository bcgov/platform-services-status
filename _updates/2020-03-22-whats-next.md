---
layout: post
title: "Platform Service Priority Update - March 2020"
date: 2020-03-23 14:42:00 +0000
categories: openshift update
---

DevOps Platform Community: 
 
First of all, a note of solidarity during these unique and challenging times. Like yours, surely, our team is feeling the destabilizing effects of the acute change and uncertainty brought on by the COVID-19 outbreak. Given this, our goal is to make every effort to bring stability and certainty to our shared work, and to the tools upon which that work depends. 
 
To that end, acknowledging the number of our government’s critical applications hosted on the On-Premise Container Platform, and the fact that that Platform is identified as a critical service in the OCIO’s business continuing planning, the Platform Services team will be adjusting its priorities to ensure uninterrupted service of all products, tools and services hosted on the current version of the Platform (i.e. the Openshift 3.11 version). 
 
As you are aware, the fact that the Platform has to-date been a Pathfinder initiative has meant that Platform enhancements and innovations have been undertaken in the same environment as production applications. Our roadmap to establishing the Platform as an “enterprise service,” including the upgrade to Openshift v.4.3, will address this limitation and the destabilizing impact it has had; however, until such time as the upgrade has been completed we will be addressing the following focuses, listed in priority order, as discussed amongst Platform governance: 
 
**1. Telework for Platform Services Team** 
 
In accordance with recommendations from BC’s Provincial Health Officer and the direction of leadership in the BC Public Service, the team has switched to telework as of Monday March 16, 2020 until further notice. The team has access to all necessary tools and technology to make telework a success - remote access, teleconferencing and collaboration tools.

**There will be no disruption to the regular maintenance operations on the Platform.** The team will continue to be available during regular business hours in RocketChat, via email and phone - please continue to use the designated channels, e.g. #devops-sos for acute issues. 
 

**2. OCP 3.11 Platform Change Freeze**
 
 - New feature freeze 

**No new features/services** will be introduced onto the OCP 3.11 Platform. 
All security tools (except those that have already been added to the Platform i.e. Artifactory) will not be added to the current Openshift 3.11 Platform and will be introduced as part of the Openshift 4 Upgrade.

**Aporeto service will NOT be restored on the Platform at this moment**, see the following explanatory note:
 
*Keeping the Aporeto service disabled on the Platform was not an easy decision for the team. We’ve put a lot of hard work into bringing this technology to the Platform and helping the product teams leverage its benefits. However, in the current circumstances, our focus is to eliminate or minimize the impact of any potential risk that could disrupt Platform operations during the COVID-19 situation. We will revisit this decision as soon as the situation changes. 
At this moment the Platform uses the Openshift native network security model that has been in effect prior to the Aporeto launch on the Platform in Oct 2019. 
The Platform Services Team is working on the guidelines for the Product Teams that currently have custom Aporeto Network Security Policies in place to secure their applications, to assist them with migrating off the Aporeto service and will share those with the Platform community shortly.*
 
- Onboarding for non-prod new projects only 

The only new projects allowed on the Platform at this time are those that are NOT looking to go to production before the Openshift 4 migration in summer 2020.
 
**3. Improved Outage Communications**

Develop and implement an improved outage communication plan (including setting up comm channels outside the Platform to supplement RocketChat).
 
We are working on building a comms site outside of the Platform where Platform users can access the real time updates during outages and also stay up to date on the latest Platform Services priorities.
Check out our new Platform Status Page at http://status.developer.gov.bc.ca/
 
**4. Next Gen Application Security Project**
 
- Aporeto in Zone B pilots

Explore  Alternative solution (non-Aporeto).
We will be working with the Zone B pilots to come up with alternative solutions that can satisfy their requirements for building secure integrations between the Openshift applications and Zone B components without the use of Aporeto.
 
- AQUA, Artifactory, Vault 

Moved to Openshift 4. The R&D work on those tools will continue on the Openshift 4 Platform and will resume as soon as Openshift 4 PROD cluster becomes available.
 
- Repo-Mountie 
Work will continue as planned. The next deliverable is the extraction of the STRA/PIA completion self-assessment data out of /bcgov repos into a report for MISOs. 
 
**5. OCP 4 Migration Prep**
- Completing the OCP 4 PROD and DR Cluster Build-Up

- Develop a migration plan and assist teams with preparing for migration - tentative May 2020

- Platform Applications Review and Cleanup of “abandoned” apps
 
**6. Improved Platform User Support**
 
- Develop a shared Platform responsibility model

- Clearly define the responsibilities for the Platform teams vs application product teams

- Review of the current product team onboarding procedure
 
- Requirement checklist for new teams (i.e. a dedicated DevOps person for ongoing support of the app)
  - Responsibilities on communicating changes for the Product Owner (PO) and DevOps person roles
  - Clear recommendations for what communication channels to use in what situations and the escalation procedure 

- Product Owner Distribution List Clean-up

  - Review the current list of POs for Platform apps to ensure all contacts in it are relevant and up-to-date

- Platform Privileged (cluster admin access) User List Cleanup

If you have any questions about the priorities above, please contact the Platform Director, Justin Hewitt, at justin.hewitt@gov.bc.ca and/or DevOps Platform Product Manager, Olena Mitovska at olena.mitovska@gov.bc.ca and/or the ED responsible for Platform Services, Rumon Carter, at rumon.carter@gov.bc.ca. 