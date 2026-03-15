# Microsoft Sentinel Password Spray Detection Lab

## Project Overview

This project demonstrates the implementation of a cloud-based Security Operations Center (SOC) monitoring environment using Microsoft Azure and Microsoft Sentinel. The goal of this lab was to simulate real-world attack scenarios and build a security monitoring pipeline capable of detecting suspicious authentication activity such as password spray attacks.

The environment was designed to collect authentication logs, analyze security events, and generate alerts through a SIEM platform. This lab helped develop practical experience with security monitoring, incident detection, and log investigation in a cloud environment.

---

# Environment Architecture

The monitoring architecture was built using Microsoft Azure cloud services.

Public Internet (Simulated attackers)  
↓  
Azure Virtual Machine (Target System)  
↓  
Network Security Group controlling inbound traffic  
↓  
Azure Log Analytics Workspace collecting logs  
↓  
Microsoft Sentinel SIEM analyzing security activity  

This architecture simulates how enterprise SOC teams monitor infrastructure for potential security threats.

---

# Technologies Used

Microsoft Azure  
Microsoft Sentinel (SIEM)  
Azure Log Analytics Workspace  
Microsoft Entra ID (Azure Active Directory)  
Kusto Query Language (KQL)  
Azure Virtual Machines  
Azure Virtual Network (VNet)  
Network Security Groups (NSG)

---

# Lab Implementation

## 1. Azure Infrastructure Deployment

A Virtual Machine was deployed inside an Azure Virtual Network to simulate a cloud-based system exposed to internet traffic. The VM served as the target system for simulated attack activity.

Network Security Groups were configured to control inbound traffic and simulate real-world firewall rules protecting cloud infrastructure.

---

## 2. Log Collection Setup

A Log Analytics Workspace was created in Azure to collect security telemetry from various services.

Authentication and sign-in logs from Microsoft Entra ID were configured to be ingested into the Log Analytics Workspace. These logs include important security information such as:

- login attempts
- failed authentication events
- IP addresses
- user identity information
- device information
- authentication status

This log data becomes the primary source of security monitoring for the SIEM.

---

## 3. Microsoft Sentinel SIEM Configuration

Microsoft Sentinel was deployed and connected to the Log Analytics Workspace to function as the Security Information and Event Management (SIEM) platform.

Sentinel was configured to analyze incoming security logs and detect abnormal authentication behavior.

Security dashboards and monitoring views were used to visualize login activity and suspicious patterns.

---

## 4. Log Analysis using KQL

Kusto Query Language (KQL) queries were used to analyze authentication activity within the log data.

Queries were created to investigate:

- login attempts
- failed authentication attempts
- suspicious login patterns
- IP addresses associated with login activity

Example queries included analyzing Microsoft Entra sign-in logs and filtering authentication failures.

---

## 5. Detection Rule Creation

Analytics rules were created inside Microsoft Sentinel to detect potential password spray attacks.

Password spray attacks occur when an attacker attempts to log in to multiple accounts using a small number of commonly used passwords.

Detection rules were configured to trigger alerts when multiple authentication failures were detected across several user accounts within a short period of time.

---

## 6. Attack Simulation

To test the monitoring system, simulated attack scenarios were performed.

Unauthorized authentication attempts were generated against the lab environment to produce log events. These events were ingested into Log Analytics and analyzed by Sentinel.

The simulated activity allowed the validation of detection rules and demonstrated how Sentinel can identify suspicious authentication patterns.

---

# Security Monitoring Outcome

The SIEM environment successfully collected authentication logs, analyzed login activity, and generated alerts when suspicious behavior was detected.

This lab demonstrated how organizations use security monitoring platforms to detect and investigate potential security threats in cloud environments.

---

# Skills Demonstrated

Cloud Infrastructure Deployment (Azure)  
Security Monitoring and SIEM Configuration  
Authentication Log Analysis  
Threat Detection and Investigation  
Identity Security Monitoring  
KQL Query Development  
Cloud Security Architecture

---

# Key Learning Outcomes

Through this project I gained hands-on experience implementing a SOC monitoring pipeline in a cloud environment.

The lab provided practical understanding of how security teams collect logs, analyze authentication activity, and detect suspicious behavior using SIEM tools.

It also demonstrated how identity systems and security monitoring platforms work together to protect enterprise infrastructure.
