---
description: |
  Sift supports NTLMv2 pass-the-hash for targeted SMB scans. This command scans one Windows host using a username and NT hash.

  Command Reference:

    Target IP: 10.10.10.1

    Domain: test.local

    Username: john

    Hash: 5fbc3d5fec8206a30f4b6c473d68ae76

command: |
  .\sift.exe network --device 10.10.10.1 --username john --nt-hash 5fbc3d5fec8206a30f4b6c473d68ae76 --domain test.local --output sift-findings.log
items:
  - Username
  - Hash
services:
  - SMB
  - NTLM
OS:
  - Windows
attack_types:
  - Enumeration
references:
  - https://github.com/Stratus-Security/Sift
---
