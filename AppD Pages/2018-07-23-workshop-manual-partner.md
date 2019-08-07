---
layout: single
title: "What is AppDefense?"
permalink: /workshop-manual-partner/
date: 2018-06-01
tags: workshop
classes: wide
author_profile: false
---

AppDefense is a data center endpoint security product that protects applications running in a virtualized environment.

AppDefense learns the intended state of set applications, and responds if the app deviates from its intended state.

# How does it work? 
AppDefense works inside the vSphere hypervisor to learn and monitor the behavior of an application running in the VM (virtual machine). 

The chance of AppDefense being compromised is greatly reduced due to its position inside the vSphere hypervisor. 

AppDefense takes a proactive approach by learning and understanding an application's intended state of behavior. After learning the intended state, AppDefense automatically responds if behavior deviates from the intended state.
 
After AppDefense detects a threat, AppDefense automates a response using vSphere and NSX DataCenter allowing for: 
- Block process communication. 
- Snapshot an endpoint for forensic analysis.
- Suspend or shut down endpoint.

# Technical Pre-reqs
A target application environment that will be protected by AppDefense must have the following:

1. Hosts running ESXi 6.5u1 or later.
2. Minimum vCenter 6.5u1 managing the ESXi hosts. If you use anything less than vCenter 6.7u1, then there will be no      plugin.
3. Complete installation of VMTools of at least version 10.3.2. (Windows Only)
4. Set VM Hardware type to version 13+.
5. IP Address for AppDefense Appliance OVA.
6. HTTPS connectivity from the Appliance to the internet. (appdefense.vmware.com)
7. SSO Admin Credentials to register the Appliance. 

# Installation Steps: 

1. AppDefense Manager - No installation is required. The service is provisioned in the cloud. You will be sent an email with log-in information.

2. Appliance - Install appliance on premise in management cluster. You will need one appliance for every vCenter. Following this you will register the appliance in the manager.

3. Host component- vib only- no reboot required.

4. Guest module- enable guest integrity and then install guest modules through VMtools. (Please note this will require a reboot.)
 

### Helpful URL's

Appdefense Manager Login <https://appdefense.vmware.com/app/sign-in-user>

Learn how Appdefense works from Tom Corn: <https://www.youtube.com/watch?v=HiJgn6GGX5w>

Interactive quick start guide by Stanton Thomas: <https://prezi.com/p/brsxr06esozp/ad-example/>




