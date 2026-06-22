# DHCP Relay

## Objectives

Configure the IP Helper Address (DHCP Relay) on a router to forward DHCP requests from clients to a remote DHCP server.

## Instructions

1. Identify the subnet that does not have a local DHCP server.
2. Configure the `ip helper-address` command on the router interface serving that subnet.
3. Verify DHCP clients can obtain leases from the remote server.

## Verification

- Use `show running-config | include ip helper` to verify helper addresses.
- Check DHCP client lease acquisition.
- Use `show ip dhcp server statistics` on the server if available.
