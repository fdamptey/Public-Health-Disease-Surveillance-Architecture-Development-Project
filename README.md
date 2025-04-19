# Public-Health-Disease-Surveillance-Architecture-Development-Project
This repository contains 6 projects with the aim to of creating Electronic Health Record systems, demonstrate interoperability among the 5 hospitals in the sector and demonstrate how it could be employed in Public Health disease surveilance.

Details of each project is found below.

**Project 1:** # Hospital Interoperability VM Setup
My Configuration Process: Successful configuration of five virtual machines for healthcare data exchange:
Key Steps I Completed:
   - Created VMs named: Aspirus_VM, Portage-Health_VM, BCMH_VM, MGH_VM and UPHIE_VM
   - Verified OS compatibility with both HAPI-FHIR and OpenEHR standards
Network Configuration**
   - Assigned static IPs
   - Configured firewall rules
   - Performed ping tests between all nodes
Validation
   - Confirmed all VMs can successfully ping each other
   - Documented the complete setup

**Project 2:** OpenEMR Installation & Configuration Guide

My Implementation Process
I successfully deployed OpenEMR across the four satelite hospital virtual machines with the following configurations:
Hospital VMs & IPs
- Aspirus Hospital 
- BCMH
- MGH
- Portage Hospital

Key Steps I Completed
1. System Preparation
bash
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install unattended-upgrades
sudo dpkg-reconfigure --priority=low unattended-upgrades
Core Software Installation

2. Installed MySQL and created dedicated OpenEMR databases. Configured Apache2 with optimized settings for healthcare applications. Deployed OpenEMR following the official installation guidelines.
3. Core Software Installation
Installed MySQL and created dedicated OpenEMR databases. Configured Apache2 with optimized settings for healthcare applications. Deployed OpenEMR following the official installation guidelines.




