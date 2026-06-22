# OSPF Network Type

## Objectives

Configure and verify different OSPF network types (broadcast, point-to-point, non-broadcast) and understand their impact on DR/BDR election and neighbor relationships.

## Instructions

1. Verify the default OSPF network type on each interface.
2. Manually change the OSPF network type on serial and Ethernet interfaces.
3. Observe how network type affects neighbor adjacency formation.
4. Verify neighbor relationships and routing table entries.

## Verification

- Use `show ip ospf interface` to check the configured network type.
- Use `show ip ospf neighbor` to verify adjacencies.
