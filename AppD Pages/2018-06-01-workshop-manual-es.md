---
layout: single
title: "Deploying AppDefense"
permalink: /workshop-manual-es/
date: 2018-09-08
tags: workshop
classes: wide
author_profile: false
---
## Deployment Timeline

AppDefense takes between 4-6 weeks to fully deploy and operationalize. Below is an overview of the weekly deployment schedule once all pre-requistes are met: 

### Week One:
Deploy the Appdefense Appliance, Host, and Guest Modules (this step).
Set up scopes and Services

### Week Two-Three:
Once Scopes and Services are set up, discovery will begin.
No user action for this period of time

### Week Four-Five:
Check the Scope Dashboard to see if the number of behaviors learned over time has tapered off,
move to protected mode, and 
integrate with internal SIEM (opitional)

Beyond: 
Identify and implement desired rules for service(s)

## AppDefense Deployment Demo 
{% include video id="D2nMRzmJXF0" provider="youtube" %}

# Technical Pre-reqs
 Target application(s) that will be protected by AppDefense must have the following:
1. Hosts running ESXi 6.5u1 or later.
2. Minimum vCenter 6.5u1 managing the ESXi hosts. If you use anything less than vCenter 6.7u1, then there will be no      plugin.
3. Complete installation of VMTools of at least version 10.3.2. (Windows Only)
4. Set VM Hardware type to version 13+.
5. IP Address for AppDefense Appliance OVA.
6. HTTPS connectivity from the Appliance to the internet. (appdefense.vmware.com)
7. SSO Admin Credentials to register the Appliance. 
8. Received Login email from AppDefense support. (If you haven't recevived this email check FAQ section)

## Deployment Procedure 
1. Deploy the OVA: 
- Networking requirements: Appliance IP,gateway,fully qualified domain name,search path, domain IP, netmask
- Root password cannot be recovered.
- Root and Admin password must be at least 8 characters with complexity requirements. 
2. Register appliance
- HTTPS:// < Appliance IP >
- You will need SSO credentials to register the appliance.
3. Deploy host from AppDefense Manager
- VIB only install, does not require reboot. 
- This needs to be done with every host that will have AppDefense enabled VMs
4. Deploy Guest Module (through VMtools)
you will need version 10.3.2 or higher of VMtools
- Please plan for a reboot with the guest module install
- Check some of our blogs for scripting tips to deploy to many VMs
- Enable guest integrity from the AppDefense Manager 
- Deploy the guest module

### Helpful URL's

Find helpful links to documentation and videos related to deployment below

## Blog Post 
