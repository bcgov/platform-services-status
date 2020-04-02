---
# Use the following two color codes for status box background
# colours a.ka.a "bgcolour" below: 
#   green = "#d2f8d2" <- things are good
#   red = "#ff9999" <- things are bad
message: "All services are operating normally"
bgcolour: "#d2f8d2"
description:
status:
    ocp: "Operational"
    sso: "Operational"
    rc: "Operational"
    mss: "Operational"
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

