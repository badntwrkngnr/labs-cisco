# Standard Numbered ACL

## Objectives

Configure a standard numbered ACL to control traffic based on source IP addresses. This lab is based on standard CCNA curriculum for IPv4 access control lists.

## Instructions

1. Identify the source networks that should be permitted or denied according to the topology.
2. Configure a standard numbered ACL on the router closest to the destination.
3. Apply the ACL to the appropriate interface in the correct direction (inbound or outbound).
4. Verify that permitted hosts can reach their destinations.
5. Verify that denied hosts cannot reach their destinations.

## Verification

- Use `show access-lists` to verify ACL entries.
- Use `show ip interface` to verify ACL application.
- Test connectivity with `ping` from both permitted and denied hosts.
