---
description: |
  Sift can scan SMB hosts without Active Directory discovery. This command scans a subnet using domain credentials.

  Command Reference:

    Target Subnet: 10.10.10.0/24

    Domain: test.local

    Username: john

    Password: password123

command: |
  .\sift.exe network --subnet 10.10.10.0/24 --username john --password password123 --domain test.local --output sift-findings.log
items:
  - Username
  - Password
services:
  - SMB
OS:
  - Windows
attack_types:
  - Enumeration
references:
  - https://github.com/Stratus-Security/Sift
---
