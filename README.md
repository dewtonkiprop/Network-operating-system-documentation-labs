# Network-operating-system-documentation-labs
# **Windows Server Security Configuration Guide**

This guide provides step-by-step instructions for configuring security settings on a Windows Server, including restricting user logon, planning an audit policy for account management, and implementing additional security measures.

****## **Restricting User Logon at Specific Times and Days**
****
To restrict user logon at specific times and days on a Windows Server, follow these steps:

1. Open Group Policy Management: Press `Windows Key + R` to open the Run dialog, type `gpmc.msc`, and press Enter.
2. Create or Edit a Group Policy Object (GPO): Navigate to the domain or organizational unit (OU) where you want to apply the policy. Right-click on it and select "Create a GPO in this domain, and Link it here" or "Edit" if a GPO already exists.
3. Navigate to Logon Hours Settings: In the Group Policy Management Editor, navigate to `Computer Configuration -> Windows Settings -> Security Settings -> Account Policies -> Logon Hours`.
4. Set Logon Hours: Double-click on "Logon Hours" to open its properties. Define the allowed logon hours for users by specifying the hours during which users are allowed to log on to the server.
5. Apply the Group Policy Object: Close the Group Policy Management Editor. Ensure that the GPO is linked to the appropriate domain or OU where the settings should apply.

**## Planning an Audit Policy for Account Management**

To plan an audit policy for account management on a Windows Server, follow these steps:

1. Determine Audit Requirements: Identify the specific account management activities you need to audit, such as creation, modification, or deletion of user accounts.
2. Configure Audit Policy Settings: Open Group Policy Management or Local Security Policy and navigate to the Audit Policy settings. Configure settings related to account management auditing, such as "Audit account management" and "Audit user account management."
3. Define Audit Log Settings: Specify where audit logs will be stored and set log size limits and retention policies.
4. Apply the Audit Policy: Link the Group Policy Object containing the audit policy settings to the appropriate domain or OU.

****## Implementing Additional Security Measures**

**### Limiting Local Account Use**
**
To limit the use of local accounts on a Windows Server, follow these steps:

1. Open Group Policy Management or Local Security Policy.
2. Configure "Deny logon locally" and "Deny logon through Remote Desktop Services" policies to prevent local accounts from logging on locally or remotely.
3. Force Group Policy Update (Optional).
4. Verify the Changes by testing the restrictions with the restricted local account(s).

**## Monitoring and Maintenance**

- Regularly monitor security events and audit logs to detect suspicious activities or security breaches.
- Review and update security configurations periodically to adapt to evolving threats and compliance requirements.

**## Additional Resources**

- Microsoft Documentation:
  - [Group Policy Overview](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-firewall/create-a-group-policy-object)
  - [Advanced Security Audit Policy Settings](https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/advanced-security-audit-policy-settings)


