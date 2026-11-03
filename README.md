# Linux Break-Fix Support Lab

A hands-on Linux troubleshooting project built using Ubuntu Server 24.04 LTS in VirtualBox.

This lab demonstrates practical Linux system administration, service troubleshooting, disk space investigation, backup and recovery, file permissions, and network/DNS diagnostics.

## Project Objectives

- Practise Linux command-line administration.
- Investigate and resolve common service failures.
- Identify disk usage issues and perform cleanup.
- Create and restore file backups.
- Troubleshoot Linux file permissions and ownership.
- Diagnose basic network connectivity and DNS resolution.

## Environment

| Component | Details |
|---|---|
| Operating System | Ubuntu Server 24.04 LTS |
| Virtualisation | Oracle VirtualBox |
| Shell | Bash |
| Services | OpenSSH, Nginx |
| Tools | systemctl, journalctl, df, du, tar, chmod, chown, ip, ping, nslookup |

## Simulated Incidents

| Incident | Scenario | Outcome |
|---|---|---|
| INC-001 | SSH service failure | Service restarted and verified |
| INC-002 | High disk usage | Test file identified and removed |
| INC-003 | Nginx service outage | Web service restored |
| INC-004 | Backup and restore | Deleted file recovered |
| INC-005 | Permissions and ownership | File access settings corrected |
| INC-006 | Network and DNS troubleshooting | Connectivity and DNS resolution verified |

## Repository Structure

```text
linux-break-fix-support-lab/
├── README.md
├── incidents/
│   ├── INC-001-ssh-service-failure.md
│   ├── INC-002-high-disk-usage.md
│   ├── INC-003-nginx-outage.md
│   ├── INC-004-backup-and-restore.md
│   ├── INC-005-permissions-ownership.md
│   └── INC-006-network-dns.md
└── screenshots/
    ├── INC-001/
    ├── INC-002/
    ├── INC-003/
    ├── INC-004/
    ├── INC-005/
    └── INC-006/
```

## Skills Demonstrated

- Linux command-line troubleshooting
- Service management with systemd
- Disk space analysis and cleanup
- Backup and recovery using tar
- File permissions and ownership management
- Network connectivity and DNS diagnostics
- Basic incident documentation and verification

## Disclaimer

All incidents in this repository are controlled lab simulations performed in a local Ubuntu Server virtual machine. They are not production incidents.

## Author

Created as a practical Linux support and troubleshooting portfolio project.
