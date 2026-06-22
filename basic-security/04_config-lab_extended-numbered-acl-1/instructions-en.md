# Extended Numbered ACL

## Objectives

Configure an extended numbered ACL to filter traffic based on source and destination IP addresses, protocols, and port numbers.

## Instructions

1. Analyze the topology to determine which traffic flows should be permitted or denied.
2. Identify the source and destination addresses, protocols, and ports involved.
3. Configure an extended numbered ACL with the specific permit and deny statements.
4. Apply the ACL to the appropriate interface and direction.
5. Verify the ACL is filtering traffic as expected.

## Verification

- Use `show access-lists` to view the ACL entries.
- Use `show ip interface` to confirm ACL placement.
- Test specific protocols (ICMP, TCP, UDP) from source hosts.
