# Unified IAM Across AD, SailPoint, Okta & Ping

## Project Aim
Develop a comprehensive, audit-ready IAM ecosystem combining governance, access control, and federated identity management for 25,000+ enterprise users.

## 🛠 Implementation
- Integrated SailPoint with Active Directory and Workday
- Deployed Okta for adaptive MFA
- Configured PingFederate for external partners
- Automated user provisioning using REST APIs and PowerShell

##  Results
- Achieved SOX/GDPR compliance
- 90% faster access provisioning
- Seamless SSO experience

## Tools
SailPoint, AD, Okta, PingFederate, PowerShell

# Okta Lifecycle Management with SCIM Integration

## Project Aim
This project demonstrates how to automate user provisioning to third-party SaaS applications using Okta and the SCIM (System for Cross-domain Identity Management) protocol.

## 🛠 Implementation

- The script `scim_create_user.py` simulates creating a user in a SCIM-enabled application using a Python script.
- This is useful in Okta-driven identity management where Okta acts as the identity provider, and pushes users into connected apps via SCIM.
- `requests` library is used to make an API call to a SCIM endpoint.

## 🔧 How to Use

### 1. Install Python
Make sure Python is installed. You can download it from: https://www.python.org/downloads/

### 2. Install Required Library
Open your terminal and run:

```bash
pip install requests
# Federated Access with Phishing-Resistant MFA

This project simulates secure federated access for enterprise users and external partners using **Okta**, **PingFederate**, and strong multi-factor authentication (MFA) methods such as **YubiKeys** and **WebAuthn**.

## Project Goal

- Establish Single Sign-On (SSO) using SAML and OAuth federation
- Enforce phishing-resistant MFA with multiple authenticators
- Simulate B2B secure access scenario

##  Included Files

### `Program.cs`
- Simulates a federated access handshake
- Prints steps for SAML + OAuth federation, MFA policy application

### `yubikey_mfa_policy.json`

This JSON file defines a phishing-resistant MFA policy, meant for integration with **Okta**'s security settings.

```json
{
  "name": "Phishing-Resistant MFA Policy",
  "type": "MFA_ENROLL",
  "conditions": {
    "users": {
      "include": ["EVERYONE"]
    }
  },
  "settings": {
    "authenticators": [
      "okta_verify_push",
      "webauthn",
      "yubikey_token"
    ]
  }
}
