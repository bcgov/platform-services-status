---
# Use the following two color codes for status box background
# colours a.ka.a "bgcolour" below: 
#   green = "#d2f8d2" <- things are good
#   red = "#ff9999" <- things are bad
message: "Intermittent issues reported and under investigation."
bgcolour: "#ff9999"
description: |
    The OCP4 platform is currently experiencing issues. Existing / running
    applications appear to be unaffected however, new pods trying to start
    are unable to communicate with the k8s API and start. This issue also
    appears to be impacting PV/PVC provisioning. We have a Sev1 ticket open
    with the vender are are working to resolve the issue.
status:
    ocp: "Intermittent"
    sso: "Operational"
    rc:  "Operational"
    mss: "Operational"
    netapp: "Intermittent"
---
<br />

{{ page.description | default: "All Platform Services are operational." }} 


# Current Information on Service Availability

| Service                      | Status                                      |
| ---------------------------- |:-------------------------------------------:| 
| OpenShift Container Platform | {{ page.status.ocp | default: "Unknown" }}  |
| Single Sign On (SSO)         | {{ page.status.sso | default: "Unknown" }}  |
| RocketChat                   | {{ page.status.rc | default: "Unknown" }}   |
| NetApp Storage Provisioning  | {{ page.status.netapp | default: "Unknown" }}   |
| Mobile Signing Service       | {{ page.status.mss | default: "Unknown" }}  |

 <b>OpenShift 4 Application Migration Roadmap Update - September 2020</b>

We’ve now completed two weeks of extensive planning sessions to provide the following roadmap to help guide your migration planning:
 
* Pre-Migration, Platform Services: September/October
* Phase 1, Early Adoption: October 14 - Mid-November (depending on the migration progress)
* Phase 2, Early Majority: Late November - Early January (TBC, contingent upon Early Adoption Phase)
* Phase 3, Late Majority: January/February (TBC, contingent upon Early Majority Phase)
* Phase 4, Sweep: Target end date - Feb 21, 2021 (Openshift 3.11 Platform is decommissioned)

Click [here]({% link _updates/2020-10-08-ocp4-migration-update.md %}) for more information.  