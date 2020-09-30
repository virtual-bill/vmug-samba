# vmug-samba
---
## Notice
The content in this repository was used for development and execution of a VMware User Group session **Home Lab Resources: Alternative Active Directory Domain Services**
While the code worked in my lab environment, **YOU** are responsible for understanding the code and how you leverage it in your lab environment(s). 

Additionally, the use of a Samba-based domain controller **IS NOT** supported by VMware. This is an example of thinking outside of the box in our homelabs. At any point, VMware may make a change that renders a Samba-based domain controller as non-functional with their solutions. 

## Introduction
As part of the VMUG 2020 season, I developed a session called **Home Lab Resources: Alternative Active Directory Domain Services**. The content from the session is a combination of:
1. Slide Presentation intro and overview
2. A series of commands customized for deploying in my home lab
3. Lab environment to deploy in

## Instructions
In order for you to leverage the code in this repository (see **commands.txt**), you'll need a couple of things in place:

- Server deployed using Ubuntu 18.04
- Server with access to Ubuntu repositories
- Understanding of the subnets and IP addresses for use by the domain controller and whichever DNS records the domain controller will serve

Unless you are running your lab in my environment (highly unlikely), you will need to make some adjustments to the code:

- Change hostname references from **VMUGDC01.vb.info**
- Change domain name references from **VB.INFO**
- Change DNS entries in the following manner, with the following as an example: 
  - sudo samba-tool dns add **name of domain controller** **domain** **record hostname** A **IP_Address**
  - example: samba-tool dns add vmugdc01 vb.info vmugvcenter A 192.168.86.151
  
## Presentation
The slide presentation is included in this repository under the **Content** directory
