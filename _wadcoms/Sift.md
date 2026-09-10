---
description: |
  Sift finds credentials, secrets and sensitive files on accessible SMB shares. This command discovers domain computers over LDAP and scans their shares using the supplied account.

  Command Reference:

    Domain: test.local

    Domain Controller: 10.10.10.1

    Username: john

    Password: password123

command: |
  .\sift.exe domain --username john --password password123 --domain test.local --domain-controller 10.10.10.1 --output sift-findings.log
items:
  - Username
  - Password
services:
  - SMB
  - LDAP
OS:
  - Windows
attack_types:
  - Enumeration
references:
  - https://github.com/Stratus-Security/Sift
---
