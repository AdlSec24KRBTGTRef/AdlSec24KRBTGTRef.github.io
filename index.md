## LinkedIn 

- [Sam Freeman](https://www.linkedin.com/in/sam-f-7092491b0?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app)

## Reset Script 

- [KRBTGT Password Reset Script](https://github.com/zjorz/Public-AD-Scripts/blob/master/Reset-KrbTgt-Password-For-RWDCs-And-RODCs.ps1)

## Methodology - Choices

- Reset twice in quick succession
- Reset twice with a pause for the default user and computer ticket lifetime (10 hours)

## Best practices 
- Practice and reherse pre incident (Australian Government ISM Control: [ISM-1847](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/ism/cyber-security-guidelines/guidelines-system-hardening) reccomends performing yearly)
- Know your domain (trusts, RODC's (which require an additional reset for each KRBTGT_123456 account))
- Ensure your domain is healthy
   - Time
   - DNS
   - Replication
- Once reset
   - Domain and Enterprise admins
   - Exchange/SharePoint admins
   - Service Accounts (Has the process for inputting the new password into the affected application been documented?)
   - Domain Users

## References

- [MS-KILE: Kerberos Network Authentication Service (V5) Synopsis](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-kile/b4af186e-b2ff-43f9-b18e-eedb366abf13) 
- [Kerberos Policy - Windows Security](https://learn.microsoft.com/en-us/windows/security/threat-protection/security-policy-settings/kerberos-policy)
- [Kerberos & KRBTGT: Active Directory’s Domain Kerberos Service Account – Active Directory Security (adsecurity.org)](https://adsecurity.org/?p=483)
- [Detecting Forged Kerberos Ticket (Golden Ticket & Silver Ticket) Use in Active Directory – Active Directory Security (adsecurity.org)](https://adsecurity.org/?p=1515)
- [AD Forest Recovery - Resetting the krbtgt password](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/manage/forest-recovery-guide/ad-forest-recovery-reset-the-krbtgt-password)
