# Security Threat Simulation and Investigation

To test the security posture of the hybrid identity environment, several simulated attack scenarios were performed.

These simulations helped validate identity protection controls and monitoring capabilities within Azure Entra ID.

---

# Scenario 1 – Login Attempt from Non-Compliant Device

## Objective

To test whether Conditional Access policies correctly block authentication from devices that are not compliant with organizational security requirements.

---

## Steps Performed

1. A test user account was configured with access policies requiring device compliance.

2. The user attempted to log in from a device that was **not enrolled or compliant with Microsoft Intune policies**.

3. The authentication attempt was evaluated against Conditional Access rules.

---

## Result

The login attempt was **blocked** due to device compliance requirements.

The security policy correctly prevented access from an unmanaged device.

---

## Security Insight

Conditional Access policies can enforce strong security controls such as:

• requiring compliant devices  
• requiring MFA  
• restricting risky sign-ins  

This protects enterprise environments from compromised or unmanaged devices.

---

# Scenario 2 – Password Spray Attack Simulation

## Objective

To simulate a common attacker technique known as a **password spray attack**.

Password spraying occurs when attackers attempt to log into multiple accounts using a commonly used password.

---

## Steps Performed

1. Multiple login attempts were made against user accounts using incorrect passwords.

2. These attempts simulated how attackers test weak credentials across many accounts.

3. The goal was to observe how Azure Entra ID logs and monitoring systems capture these events.

---

## Result

The failed authentication attempts were recorded in **Azure Entra ID sign-in logs**.

These logs include important information such as:

• timestamp of the login attempt  
• username targeted  
• failure reason  
• IP address  
• client application used  

---

## Security Insight

Monitoring authentication failures is important because:

• repeated failures may indicate brute force or password spray attacks  
• security teams can detect suspicious activity early  
• alerts can be created for automated threat detection  

---

# Sign-In Log Investigation

Azure Entra ID provides detailed **sign-in logs** that allow security teams to analyze authentication activity.

These logs provide visibility into:

• successful login attempts  
• failed login attempts  
• user location  
• IP address  
• device information  
• authentication method  

---

## What Was Observed

During the password spray simulation:

• multiple failed login attempts were recorded  
• authentication failures were logged  
• user and IP information was captured  

This data can help identify suspicious login patterns.

---

# Audit Log Investigation

Azure Entra ID audit logs were reviewed to monitor administrative activities.

Audit logs track important changes such as:

• user account creation  
• role assignments  
• security policy updates  
• directory changes  

Audit logs are essential for compliance and incident investigations.

---

# Importance of Identity Monitoring

Identity systems are one of the most targeted components in modern cyber attacks.

Monitoring identity activity helps detect threats such as:

• credential theft  
• brute force attacks  
• suspicious login locations  
• unauthorized privilege changes  

Identity monitoring is a key responsibility of security operations teams.

---

# Key Lessons from the Security Simulation

This exercise demonstrated several important cybersecurity principles:

• identity systems must be continuously monitored  
• strong authentication reduces attack risk  
• conditional access protects cloud resources  
• audit logs provide visibility into administrative actions  
• sign-in logs are essential for threat investigation  

These security controls form the foundation of **modern cloud identity protection strategies**.

---

# Future Security Improvements

Additional improvements that could be implemented include:

• Microsoft Sentinel integration for automated threat detection  
• automated alerts for suspicious login patterns  
• risk-based conditional access policies  
• identity protection risk scoring  
• security incident response playbooks
