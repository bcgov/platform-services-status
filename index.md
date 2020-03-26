---
# Use the following two color codes for status box background
# colours a.ka.a "bgcolour" below: 
#   green = "#d2f8d2" <- things are good
#   red = "#ff9999" <- things are bad
message: "Platform wide service disruption"
bgcolour: "#ff9999"
description: |
    2020-03-26 11:47
    We are experiencing a platform wide outage that was caused by the same router pod issue that we had a few days ago. The outage is impacting the availability of all platform applications as well as shared services such as KeyCloak, SSO, and RocketChat.
    
    We are working closely with RedHat to troubleshoot the issue and will be posting more information as it becomes available.

    2020-03-26 11:35
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

