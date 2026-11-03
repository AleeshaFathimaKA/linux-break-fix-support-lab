# INC-001: SSH Service Failure

**Status:** Resolved  
**Type:** Simulated Linux Support Incident  
**Priority:** Medium  
**Environment:** Ubuntu Server 24.04 LTS (VirtualBox)

## Issue
The SSH service was stopped during a controlled troubleshooting exercise, making the SSH daemon unavailable.

## Symptoms
- SSH service showed an inactive state.
- No SSH process was listening on port 22.

## Investigation
Commands used:

```bash
sudo systemctl status ssh
sudo systemctl is-enabled ssh
sudo ss -tlnp | grep :22
```

## Root Cause
The SSH service had been deliberately stopped to simulate a service outage.

## Resolution
Restarted the SSH service:

```bash
sudo systemctl start ssh
```

Enabled it to start automatically at boot:

```bash
sudo systemctl enable ssh
```

## Verification
Checked the service and port again:

```bash
sudo systemctl status ssh
sudo systemctl is-enabled ssh
sudo ss -tlnp | grep :22
```

The service was active, enabled, and listening on port 22.

## Closure
The simulated SSH service issue was resolved and service availability was verified.
