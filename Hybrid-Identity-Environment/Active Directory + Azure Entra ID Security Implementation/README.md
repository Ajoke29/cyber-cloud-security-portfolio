# Hybrid Identity Lab – Active Directory + Azure Entra ID Security Implementation

## Project Overview

This lab demonstrates the deployment and security configuration of a **hybrid identity environment** integrating an on-premises Active Directory infrastructure with Microsoft Azure Entra ID.

The purpose of this project was to simulate how modern enterprises manage digital identities across both **on-premises infrastructure and cloud platforms** while enforcing strong security controls.

The lab focuses heavily on **Identity and Access Management (IAM)** concepts including:

• user identity management  
• authentication and authorization  
• role-based access control  
• multi-factor authentication  
• identity synchronization  
• security monitoring and auditing  

This environment replicates how organizations manage user access in **real enterprise hybrid environments**.

---

# Lab Architecture

The hybrid environment consists of the following components:

```
Internet
   ↓
Microsoft Azure Tenant
   ↓
Azure Entra ID (Cloud Identity Platform)
   ↓
Azure AD Connect (Directory Synchronization)
   ↓
On-Premises Active Directory Domain Controller
   ↓
Domain Users / Groups / Organizational Units
```

This architecture allows identities created in **Active Directory** to be synchronized to **Azure Entra ID** for cloud authentication.

---

# Technologies Used

Active Directory Domain Services (AD DS)  
Microsoft Azure  
Azure Entra ID (formerly Azure AD)  
Azure AD Connect  
Windows Server  
Virtual Machines  
Identity and Access Management (IAM)

---

# Step 1 – Active Directory Domain Setup

A Windows Server virtual machine was deployed and configured as a domain controller.

### Installation steps

1. Installed **Active Directory Domain Services (AD DS)**
2. Promoted the server to a **domain controller**
3. Created a new domain
4. Configured DNS for domain resolution

The domain controller acts as the **central identity authority** for the environment.

---

# Step 2 – Active Directory Identity Management

## Organizational Units

Organizational Units (OUs) were created to structure users logically.

Example OUs:

• IT Department  
• HR Department  
• Finance Department  

OUs allow administrators to apply policies and manage identities efficiently.

---

## User Account Creation

User accounts were created to simulate enterprise employees.

Each user account includes attributes such as:

• username  
• password  
• department  
• job role  
• email identity  

These accounts represent **digital identities inside the organization**.

Example users created:

• IT administrators  
• HR personnel  
• standard employees  

Each user authenticates to the domain using Active Directory credentials.

---

# Step 3 – Security Groups and RBAC

Security groups were created to implement **Role-Based Access Control (RBAC)**.

Example groups:

• IT_Admins  
• HR_Group  
• Finance_Group  

Permissions are assigned to groups instead of individual users.

Benefits:

• easier management  
• consistent permissions  
• reduced administrative overhead  

This approach reflects how **enterprise IAM systems manage authorization**.

---

# Step 4 – Azure Tenant Configuration

A Microsoft Azure tenant was configured to simulate cloud infrastructure.

Key services enabled:

• Azure Entra ID  
• Azure Resource Groups  
• Azure identity services  

Azure Entra ID acts as the **cloud identity provider** for the organization.

---

# Step 5 – Azure Entra ID User Management

After connecting Azure to the environment, identities were managed in Entra ID.

### Cloud identity configuration includes:

• viewing synchronized users  
• managing user properties  
• assigning roles and permissions  

Users synchronized from Active Directory appear in **Azure Entra ID directory services**.

---

# Step 6 – Azure AD Connect (Identity Synchronization)

Azure AD Connect was installed to synchronize identities between:

On-Premises Active Directory  
and  
Azure Entra ID

### Synchronization enables

• unified identity management  
• cloud authentication  
• consistent user accounts across environments  

When a user is created on-premises, it automatically appears in Azure Entra ID.

This is known as **Hybrid Identity**.

---

# Step 7 – Authentication Process

Users authenticate using their domain credentials.

Authentication flow:

1. User enters username and password
2. Identity is verified by Active Directory
3. Azure Entra ID recognizes the synchronized identity
4. Access is granted based on permissions and policies

This ensures centralized authentication across environments.

---

# Step 8 – Multi-Factor Authentication (MFA)

Multi-Factor Authentication was configured to strengthen identity security.

MFA requires users to provide:

• password  
• secondary verification factor

Examples of MFA methods:

• authenticator app  
• phone notification  
• verification code  

Benefits of MFA:

• reduces credential theft risk  
• prevents unauthorized logins  
• protects privileged accounts

---

# Step 9 – Azure Entra ID Role Assignment

Administrative permissions were controlled using Azure RBAC.

Example roles include:

• Global Administrator  
• User Administrator  
• Security Reader  
• Application Administrator  

Assigning roles ensures users only have **necessary administrative privileges**.

This supports the **principle of least privilege**.

---

# Step 10 – Conditional Access Policies

Conditional access policies restrict access based on security conditions.

Policies may enforce:

• MFA requirements  
• location-based restrictions  
• device compliance  
• risk-based sign-in protection  

These controls help protect sensitive cloud resources.

---

# Step 11 – Sign-In Monitoring

Azure Entra ID provides detailed **sign-in logs**.

Sign-in logs track:

• login attempts  
• user location  
• IP address  
• device information  
• authentication status  

These logs are essential for detecting suspicious activity.

---

# Step 12 – Audit Logs

Audit logs record administrative activities such as:

• user creation  
• role assignments  
• policy changes  
• security updates  

Audit logs provide accountability and visibility into identity management actions.

---

# Step 13 – Identity Security Monitoring

Monitoring identity activity helps detect threats such as:

• credential compromise  
• unusual login locations  
• repeated failed login attempts  
• suspicious account behavior  

Identity monitoring is a critical component of modern cybersecurity operations.

---

# Security Concepts Demonstrated

## Authentication
Verifying a user's identity before access is granted.

## Authorization
Determining what resources the user can access.

## RBAC
Assigning permissions based on role rather than individual user.

## MFA
Adding additional security layers beyond passwords.

## Identity Synchronization
Connecting on-premises identity systems with cloud identity platforms.

## Audit Logging
Tracking identity-related events for investigation and compliance.

---

# Skills Demonstrated

Active Directory administration  
Azure Entra ID configuration  
Hybrid identity architecture  
Role-Based Access Control (RBAC)  
Multi-Factor Authentication deployment  
Identity monitoring and logging  
Enterprise IAM design

---

# Real World Relevance

Most organizations today operate hybrid environments where identity systems span:

• on-premises infrastructure  
• cloud platforms  
• SaaS applications

Hybrid identity solutions allow companies to transition to cloud services while maintaining legacy systems.

Understanding hybrid IAM is essential for roles such as:

Security Analyst  
IAM Engineer  
Cloud Security Engineer  
System Administrator

---

# Screenshots (To Be Added)

• Active Directory users and groups  
• Domain controller configuration  
• Azure tenant overview  
• Azure Entra ID users  
• MFA configuration  
• Sign-in logs  
• Audit logs  
• Azure AD Connect synchronization
