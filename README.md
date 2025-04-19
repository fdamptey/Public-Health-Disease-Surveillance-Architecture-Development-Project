# Public-Health-Disease-Surveillance-Architecture-Development-Project
This repository contains 6 projects with the aim to of creating Electronic Health Record systems, demonstrate interoperability among the 5 hospitals in the sector and demonstrate how it could be employed in Public Health disease surveilance.

Details of each project is found below.

**Project 1:** # Hospital Interoperability VM Setup
My Configuration Process: Successful configuration of five virtual machines for healthcare data exchange:
Key Steps:
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
Implementation Process
Successfully deployed OpenEMR across the four satelite hospital virtual machines:
Hospital VMs: Aspirus Hospital, BCMH, MGH and Portage Hospital

Key Steps
1. System Preparation
bash
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install unattended-upgrades
sudo dpkg-reconfigure --priority=low unattended-upgrades
Core Software Installation
2. MySQL installation and creation of dedicated OpenEMR databases, configured Apache2 with optimized settings for healthcare applications and deployed OpenEMR. 
3. Core Software Installation
Installed MySQL and created dedicated OpenEMR databases. Configured Apache2 with optimized settings for healthcare applications. Deployed OpenEMR following the official installation guidelines.
4. Security Hardening
Implemented multiple security layers including firewall configuration, apache security enhancements and restarted Apache with the command, sudo systemctl restart apache2Verification Testing.
5. Validated installations by accessing each OpenEMR instance via web browser, confirmed database connectivity and tested user authentication with strong password requirements.

**Project 3:** This phase was to generate  synthetic patient data to be used in covid-19 syndromic surveillance which will simulate disease Outbreak. Synthetic patient data was generated from the four satelite virtual machine hospitals fron the open EMR installed in phase 2. This produced HL7 FHIR-formatted .json files for syndromic surveillance testing. Quantified Outbreak scenarios were quantified by hospital population.

**Project 4:** HAPI FHIR Server Setup
Set up a HAPI FHIR server to manage healthcare data on VM 5 - UPHIE VM. The following tasks were performed: 
   - See how much memory was being used/left.
   - Made sure the server port was open and available.
   - Checked if another program was blocking the server.

**Project 5:** FHIR Data Exchange Project
Phase 5 was to demonstrate interoperability of Health Information Exchanges (HIE) by successfully setting up a system to share healthcare data between hospitals using FHIR standards. This shows how different medical systems can safely exchange data. The project chronicles simple steps to create new patient/doctor records and tested the system using Postman (an API tool).
This HIE worked by 
1. stablishing access to the FHIR Server**: Connect to the HAPI FHIR system created on VM 5.
2. Used Postman tool to help test data sharing by pushing or pooling data from the HAPI FHIR.

The Postman API showed key features essential in real world HIE standards by showing displaying feedbacks for action.

**Project 6:** Healthcare Data Dashboard Project
the objective of phase 6 was to extract data from the 4 satelite virtual hospitals, convert the data into csv file and aggregate the dataset to form a single file. The results was then loaded onto google Looker studio and a dashboard was created to display data patterns. Informaticist utilize such dashboards to display findings and patterns. These strong visual displays allow users to easily understand information that could have been otherwise difficulty to appreciate.

How I Did It
Step 1: Collected the Data
   - Gathered hospital information from multiple CSV files
   - Used Python to combine all the data (see screenshot below)
Step 2: Created Visualizations
   - Used Google Looker Studio to build interactive charts
   - Designed different views to show various aspects of the data
Step 3: Shared the Dashboard
   - Published the dashboard online for easy access.
Dashboards can be a valuable tool to display real-time heathcare information which is very essential in disease outbreaks like pandemics, epidemics and in infectious disease surveillance.

You can view it here: [Healthcare Data Dashboard](https://lookerstudio.google.com/reporting/149e3613-5fea-4928-a834-8607e40c9c11/page/a2KGF)

## Try It Yourself
Visit the dashboard link above to:
- Explore different hospital metrics
- See how visualizations can change improve understanding
- Discover trends in the data

This project shows how we can turn raw numbers into meaningful pictures that help make better healthcare decisions.
