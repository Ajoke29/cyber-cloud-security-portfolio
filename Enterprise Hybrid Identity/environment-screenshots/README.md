# Environment Screenshots

## Microsoft Entra ID Tenant Dashboard

This screenshot shows the Microsoft Entra ID tenant overview used in the hybrid identity environment.

It displays tenant information including:

- Tenant ID
- Primary domain
- Number of users
- Number of groups
- Registered devices
- Applications
- Global administrator role assignments

The dashboard provides a high-level view of identity resources and security posture within the tenant.

![Entra Tenant Overview](screenshots/entra-dashboard.png)

---

# Azure Entra Groups Configuration

Groups were created to manage user access and enforce role-based access control (RBAC).

Security groups allow administrators to:

- assign permissions to multiple users at once
- manage access to resources
- simplify identity governance

Example groups created include:

- IT Admins
- IT Support
- Software Engineers
- External Guests
- Compliance Users
- Device Management Groups

![Entra Groups Overview](screenshots/entra-groups-overview.png)

---

# Security Groups List

This screenshot shows the list of security groups configured within the Entra ID tenant.

These groups support access management and role assignment.

Examples include:

- SG-IT-Admins
- SG-IT-Support
- SG-Software-Engineer
- Windows Autopilot Devices
- Windows Compliance Users
- Production Devices
- External Guests

These groups can be used for:

- Conditional Access policies
- Application access control
- Role-based administration
- Device compliance enforcement

![Security Groups](screenshots/security-groups.png)

---

# Virtual Lab Environment (VMware)

The hybrid identity environment was built using VMware Workstation.

The following virtual machines were deployed:

- Domain Controller (Windows Server 2022)
- Windows 11 Client
- Ubuntu Attacker Machine
- Azure AD Connect Server

These machines simulate a small enterprise network environment.

![VMware Environment](screenshots/vmware-lab.png)

---

# Domain Controller Setup

A Windows Server 2022 machine was configured as the Domain Controller.

Server Manager was used to install the following roles:

- Active Directory Domain Services
- DNS Server
- DHCP Server

This server acts as the central identity provider for on-premises authentication.

![Server Manager](screenshots/server-manager.png)

---

# Active Directory Domain Configuration

The domain **teckvisuals.local** was created.

Organizational Units (OUs) were created to organize users and devices:

- TECK_Admin
- TECK_Users
- TECK_Computers
- TECK_Groups
- TECK_Departments
- TECK_Servers

This structure allows administrators to apply group policies and manage resources efficiently.

![Active Directory OU Structure](screenshots/active-directory-ous.png)

---

# Domain User Login

This screenshot shows a domain user logging into a Windows client machine using domain credentials.

Authentication is handled by the Domain Controller.

This confirms that:

- the workstation successfully joined the domain
- domain authentication is working
- Active Directory identity management is functioning correctly

![Domain Login](screenshots/domain-login.png)

---

# Hybrid Identity Synchronization

Azure AD Connect was used to synchronize identities from on-premises Active Directory to Microsoft Entra ID.

Synchronization allows users to authenticate to:

- on-premises systems
- cloud services
- Microsoft 365 applications

using the same identity.

This creates a hybrid identity architecture.

---

# Identity Security Features Configured

The following security controls were implemented in the environment:

Multi-Factor Authentication (MFA)

Users must provide an additional verification factor during login.

Conditional Access

Policies were created to enforce security conditions such as:

- requiring MFA
- restricting access from non-compliant devices
- blocking risky login attempts

Role Based Access Control (RBAC)

Security groups were used to assign access privileges based on roles.

Audit Logs

Administrative actions and identity changes were tracked using audit logs.

Sign-In Logs

Authentication activity was monitored through Entra ID sign-in logs.

---

# Security Testing

To test the identity security controls, several attack simulations were performed:

- password spray attempts
- login from non-compliant device
- monitoring authentication failures
- reviewing sign-in logs
- reviewing audit logs

These tests verified that security policies and monitoring systems were functioning correctly.
