# OSPF DR Priority

## Objectives

Understand and manipulate OSPF Designated Router (DR) and Backup Designated Router (BDR) election using interface priority settings.

## Instructions

1. Verify the current DR/BDR election on the multi-access segment.
2. Change the OSPF priority on interfaces to influence DR/BDR election.
3. Observe that the router with the highest priority becomes the DR.
4. Force a new election by clearing the OSPF process or using `ip ospf priority` on a new router.
5. Verify the new DR/BDR roles.

## Verification

- Use `show ip ospf neighbor` to view DR/BDR status.
- Use `show ip ospf interface` to check priority and neighbor state.
