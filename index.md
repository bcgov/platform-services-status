---
message: "Platform wide service disruption"
description: |
    We are investigating what appears to be a system wide outage effecting a wide range of services including OCP, SSO and
    RocketChat.
status:
    ocp: "Intermittent Issues"
    sso: "Intermittent Issues"
    rc: "Intermittent Issues"
    mss: "Intermittent Issues"
---

<br />

{{ page.description | default: "In the event of a disruption to any of
the service listed below, this message will be replaced with
informational text." }} 

# Current Information on Service Availability

| Service                      | Status                                      |
| ---------------------------- |:-------------------------------------------:| 
| OpenShift Container Platform | {{ page.status.ocp | default: "Unknown" }}  |
| Single Sign On (SSO)         | {{ page.status.sso | default: "Unknown" }}  |
| RocketChat                   | {{ page.status.rc | default: "Unknown" }}   |
| Mobile Signing Service       | {{ page.status.ocp | default: "Unknown" }}  |

