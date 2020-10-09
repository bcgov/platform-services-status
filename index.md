---
# Use the following two color codes for status box background
# colours a.ka.a "bgcolour" below: 
#   green = "#d2f8d2" <- things are good
#   red = "#ff9999" <- things are bad
message: "All services are operating normally"
bgcolour: "#ff9999"
description: |
    Some services and applications on the Platform including RocketChat and TheOrgBook seem to be experiencing service disruptions starting from 6:00pm on Oct 8, 2020. The Platform Operations Team is troubleshooting the issue and will post an update as soon as more information is available.
status:
    ocp: "Operational"
    sso: "Operational"
    rc: "Service Down"
    mss: "Operational"
---

<br />

{{ page.description | default: "In the event of a disruption to any of
the service listed below, this message will be replaced with
informational text." }} 

<b>Platform Service Priority Update - March 2020</b>

Due to the increasing number of business critical applications that are now hosted on the Openshift Platform and provide emergency and essential services to the residents of British Columbia, the Platform Services team will be adjusting its priorities to ensure uninterrupted service of all products, tools and services hosted on the current version of the Platform (i.e. the Openshift 3.11 version). Click [here]({% link _updates/2020-03-22-whats-next.md %}) for more information.  

# Current Information on Service Availability

| Service                      | Status                                      |
| ---------------------------- |:-------------------------------------------:| 
| OpenShift Container Platform | {{ page.status.ocp | default: "Unknown" }}  |
| Single Sign On (SSO)         | {{ page.status.sso | default: "Unknown" }}  |
| RocketChat                   | {{ page.status.rc | default: "Unknown" }}   |
| Mobile Signing Service       | {{ page.status.ocp | default: "Unknown" }}  |

