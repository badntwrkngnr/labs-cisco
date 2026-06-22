# Standard Named ACL

## Objectives

Configure a standard named ACL to filter traffic based on source IP addresses. Named ACLs provide better readability and management compared to numbered ACLs.

## Instructions

1. Identify the traffic filtering requirements based on the topology.
2. Create a standard named ACL with a descriptive name.
3. Configure permit and deny entries for the required source addresses.
4. Apply the named ACL to the appropriate interface in the correct direction.
5. Verify the ACL behavior from each host.

## Verification

- Use `show access-lists` to display the named ACL.
- Use `show running-config` to verify the complete configuration.
- Test connectivity with `ping` and `traceroute`.
