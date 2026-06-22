# OSPF Router IDs

## Objectives

Understand how OSPF router IDs are determined and manually configure router IDs for stability and predictability.

## Instructions

1. Determine the current router ID on each router using `show ip ospf`.
2. Manually configure a router ID using `router-id` in OSPF configuration mode.
3. Clear the OSPF process to force the new router ID to take effect.
4. Verify the new router ID is used in neighbor relationships and LSAs.

## Verification

- Use `show ip ospf` to verify the router ID.
- Use `show ip ospf neighbor` to confirm consistent router IDs.
