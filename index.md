---
# Use the following two color codes for status box background
# colours a.ka.a "bgcolour" below: 
#   green = "#d2f8d2" <- things are good
#   red = "#ff9999" <- things are bad
message: "RocketChat and TheOrgBook are down"
bgcolour: "#ff9999"
description: |
    Some services and applications on the Platform including RocketChat and TheOrgBook seem to be experiencing service disruptions starting from 6:00pm on Oct 8, 2020. The Platform Operations Team is troubleshooting the issue and will post an update as soon as more information is available.
bgcolour: "#d2f8d2"
description:
status:
    ocp: "Operational"
    sso: "Operational"
    rc: "Service Down"
    mss: "Operational"

<br />

{{ page.description | default: "In the event of a disruption to any of the service listed below, this message will be replaced with informational text." }} 

<b>Platform Service Priority Update - July 2020</b>

To address current capacity issues related to the limited Platform CPU, we’ve made the difficult decision to temporarily prioritize new project requests, based on the following criteria:

1. Your project addresses the needs of an urgent COVID-19 response;
2. Your project has been designated as high business priority;
3. You have the DevOps capacity in place to support the development of resilient architecture suitable for multi-node deployment;

If your projects meets all 3 requirements, we can provision a namespace for you now. If it doesn’t , we ask that the project wait until a new Openshift 4 Platform becomes available in September 2020.

Click [here]({% link _updates/2020-08-05-availability.md %}) for more information.  

# Current Information on Service Availability

| Service                      | Status                                      |
| ---------------------------- |:-------------------------------------------:| 
| OpenShift Container Platform | {{ page.status.ocp | default: "Unknown" }}  |
| Single Sign On (SSO)         | {{ page.status.sso | default: "Unknown" }}  |
| RocketChat                   | {{ page.status.rc | default: "Unknown" }}   |
| Mobile Signing Service       | {{ page.status.ocp | default: "Unknown" }}  |

