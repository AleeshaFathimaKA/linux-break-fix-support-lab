# INC-004: Backup and Restore

**Status:** Resolved  
**Type:** Simulated Linux Support Incident  
**Priority:** Medium  
**Environment:** Ubuntu Server 24.04 LTS (VirtualBox)

## Issue
A configuration file was deleted intentionally to simulate accidental data loss. The objective was to restore it from a previously created backup.

## Symptoms
- The original configuration file was missing from the data directory.
- The backup archive was available.

## Investigation
Checked the data and backup directories:

```bash
ls -l ~/support-lab/data/
ls -lh ~/support-lab/backup/
tar -tzvf ~/support-lab/backup/config-backup.tar.gz
```

## Root Cause
The configuration file was deliberately deleted during the lab exercise.

## Resolution
Restored the file from the compressed backup archive:

```bash
tar -xzvf ~/support-lab/backup/config-backup.tar.gz -C ~/support-lab/data/
```

## Verification
Checked that the restored file existed and its contents were correct:

```bash
ls -l ~/support-lab/data/
cat ~/support-lab/data/config.txt
```

The file was restored with its expected content.

## Closure
The simulated data-loss scenario was resolved using a previously created tar.gz backup. Restoration was verified successfully.
