# INC-005: Linux Permissions and Ownership

**Status:** Resolved  
**Type:** Simulated Linux Support Incident  
**Priority:** Medium  
**Environment:** Ubuntu Server 24.04 LTS (VirtualBox)

## Issue
A file was made inaccessible by changing its permissions and ownership during a controlled troubleshooting exercise.

## Symptoms
- The file initially had no permissions.
- File ownership was changed to the root user.

## Investigation
Commands used:

```bash
ls -l ~/support-lab/secret.txt
```

The file permission symbols and ownership details were inspected.

## Root Cause
Incorrect file permissions and ownership were deliberately introduced to simulate an access issue.

## Resolution
Restored owner read/write permissions:

```bash
chmod 600 ~/support-lab/secret.txt
```

Restored ownership to the current user:

```bash
sudo chown "$(whoami):$(whoami)" ~/support-lab/secret.txt
```

## Verification
Checked permissions and ownership:

```bash
ls -l ~/support-lab/secret.txt
```

The expected result was owner-only read/write access and ownership assigned to the current user.

## Closure
The simulated file access issue was addressed by correcting permissions and ownership.
