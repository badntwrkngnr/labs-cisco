# PAT with a Pool

## Objectives

Configure PAT using a pool of public addresses, allowing multiple private hosts to share multiple public addresses with port-based translation.

## Instructions

1. Define an ACL for the inside local addresses.
2. Create a NAT pool with multiple public addresses.
3. Configure overload (PAT) using the pool.
4. Assign inside and outside interfaces.
5. Verify translations and connectivity.

## Verification

- Use `show ip nat translations` to verify PAT entries.
- Use `show ip nat statistics` to check pool utilization.
