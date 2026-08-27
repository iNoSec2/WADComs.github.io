---
description: |
  Sift finds credentials, secrets and sensitive files on local filesystems. This command scans the C: drive and writes the findings to a log.

  Command Reference:

    Path: C:\

    Output File: sift-findings.log

command: |
  .\sift.exe local --path C:\ --output sift-findings.log
items:
  - Shell
OS:
  - Windows
attack_types:
  - Enumeration
references:
  - https://github.com/Stratus-Security/Sift
---
