# INC-003: Nginx Web Server Failure

**Status:** Resolved  
**Type:** Simulated Linux Support Incident  
**Priority:** High  
**Environment:** Ubuntu Server 24.04 LTS (VirtualBox)

## Issue
The Nginx web server was deliberately stopped to simulate a website availability issue.

## Symptoms
- Nginx service showed an inactive state.
- The local website did not respond to HTTP requests.
- A connection failure occurred when accessing localhost.

## Investigation
Commands used:

```bash
sudo systemctl status nginx
sudo ss -tlnp | grep :80
curl http://localhost
```

## Root Cause
The Nginx service had been intentionally stopped during the troubleshooting exercise.

## Resolution
Restarted the Nginx service:

```bash
sudo systemctl start nginx
```

## Verification
Checked the service status and tested the local website:

```bash
sudo systemctl status nginx
curl http://localhost
```

Nginx returned to an active state, and the local website responded with the Nginx welcome page.

## Closure
The simulated web server outage was resolved by restarting Nginx and verifying HTTP availability.
