# Basic Router Setup

## Objectives

Configure fundamental settings on a Cisco router including hostname, passwords, banner, and interface addressing to establish basic management connectivity.

## Instructions

1. Connect to the router console and configure the hostname.
2. Set an encrypted privileged mode password using `enable secret`.
3. Configure a console password and enable login.
4. Configure a MOTD banner with an appropriate security message.
5. Assign an IP address to the appropriate interface and enable it.
6. Save the configuration to NVRAM.

## Verification

- Use `show running-config` to verify all settings.
- Use `show ip interface brief` to confirm interface status.
- Test console and privileged mode access.
