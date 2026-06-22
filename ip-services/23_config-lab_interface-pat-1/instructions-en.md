# Interface PAT

## Objectives

Configure Port Address Translation (PAT) using a router's outside interface IP address to allow multiple internal hosts to share a single public IP.

## Instructions

1. Define an ACL identifying the inside local addresses.
2. Configure NAT overload on the outside interface.
3. Designate inside and outside interfaces.
4. Verify multiple inside hosts can access external networks simultaneously.

## Verification

- Use `show ip nat translations` to verify PAT entries with port numbers.
- Use `show ip nat statistics` to check translation counts.
