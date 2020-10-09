---
# Use the following two color codes for status box background
# colours a.ka.a "bgcolour" below: 
#   green = "#d2f8d2" <- things are good
#   red = "#ff9999" <- things are bad
message: "Storage Provisioning Platform Service is Down"
bgcolour: "#ff9999"
description: |
    Some services and applications on the Platform including RocketChat and TheOrgBook seem to be experiencing service disruptions related to the issue with the storage on the Platform starting from 6:00pm on Oct 8, 2020. The Platform Operations Team is troubleshooting the issue and will post an update as soon as more information is available. 
bgcolour: "#ff9999"
description:
status:
    ocp: "Operational"
    sso: "Operational"
    rc:  "Operational"
    mss: "Operational"
    netapp: "Down"
---
<br />

{{ page.description | default: "As an ongoing action to yesterday Service Outage the Trident Provisioner Service for Openshift 3.11 is being turned off while we look to resolve the issue. No new PVCs can be provisioned at this time. There is no impact on the existing PVCs.

" }} 


# Current Information on Service Availability

| Service                      | Status                                      |
| ---------------------------- |:-------------------------------------------:| 
| OpenShift Container Platform | {{ page.status.ocp | default: "Unknown" }}  |
| Single Sign On (SSO)         | {{ page.status.sso | default: "Unknown" }}  |
| RocketChat                   | {{ page.status.rc | default: "Unknown" }}   |
| NetApp Storage Provisioning  | {{ page.status.netapp | default: "Unknown" }}   |
| Mobile Signing Service       | {{ page.status.ocp | default: "Unknown" }}  |

 <b>OpenShift 4 Application Migration Roadmap Update - September 2020</b>

We’ve now completed two weeks of extensive planning sessions to provide the following roadmap to help guide your migration planning:
 
* Pre-Migration, Platform Services: September/October
* Phase 1, Early Adoption: October 14 - Mid-November (depending on the migration progress)
* Phase 2, Early Majority: Late November - Early January (TBC, contingent upon Early Adoption Phase)
* Phase 3, Late Majority: January/February (TBC, contingent upon Early Majority Phase)
* Phase 4, Sweep: Target end date - Feb 21, 2021 (Openshift 3.11 Platform is decommissioned)

Click [here]({% link _updates/2020-10-08-ocp4-migration-update.md %}) for more information.  