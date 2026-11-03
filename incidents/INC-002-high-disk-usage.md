# INC-002: High Disk Usage

**Status:** Resolved  
**Type:** Simulated Linux Support Incident  
**Priority:** Medium  
**Environment:** Ubuntu Server 24.04 LTS (VirtualBox)

## Issue
A controlled increase in disk usage was simulated by creating a large test file.

## Symptoms
- Disk usage increased after creating the test file.
- The root filesystem showed increased used space.

## Investigation
Commands used:

```bash
df -h /
du -sh /largefile
```

The `df` command was used to check filesystem usage, while `du` identified the space occupied by the test file.

## Root Cause
A large test file created for the lab exercise consumed additional disk space.

## Resolution
Removed the test file:

```bash
sudo rm /largefile
```

## Verification
Checked filesystem usage again:

```bash
df -h /
```

Disk usage returned to its previous level after the file was removed.

## Closure
The simulated disk usage increase was resolved through file identification and cleanup. No persistent disk issue was observed.
