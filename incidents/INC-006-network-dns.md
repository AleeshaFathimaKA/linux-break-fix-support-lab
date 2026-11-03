# INC-006: Network and DNS Troubleshooting

**Status:** Resolved  
**Type:** Simulated Linux Support Incident  
**Priority:** Medium  
**Environment:** Ubuntu Server 24.04 LTS (VirtualBox)

## Issue
A network and DNS troubleshooting exercise was performed to verify IP connectivity and name resolution, including a controlled failed DNS query.

## Investigation
Checked network interfaces and IPv4 configuration:

```bash
ip a
ip -4 addr show enp0s3
```

Tested connectivity to an external IP:

```bash
ping -c 10 8.8.8.8
```

Checked DNS resolution:

```bash
getent hosts google.com
resolvectl status
nslookup google.com
```

## Findings
- The network interface had an assigned IPv4 address.
- The repeat connectivity test received all 10 packets.
- Normal DNS resolution returned IP addresses for google.com.
- The DNS lookup through the reserved test address `192.0.2.1` failed as expected.

## Root Cause
A controlled DNS lookup failure was simulated by directing a single query to a non-operational test address. The normal system DNS configuration was not changed.

## Resolution
Repeated the DNS query using the system's normal resolver:

```bash
nslookup google.com
```

Name resolution succeeded.

## Verification
Confirmed successful IP connectivity and normal DNS resolution using the commands above.

## Closure
The network and DNS checks were completed. Normal connectivity and name resolution were verified after the controlled failed-query test.
