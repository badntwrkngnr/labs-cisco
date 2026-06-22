# OSPF Metrics

## Objectives

Understand and manipulate OSPF cost metrics to influence path selection across the network.

## Instructions

1. Examine the default OSPF cost on each interface.
2. Manually configure interface cost using `ip ospf cost`.
3. Alternatively, change the reference bandwidth using `auto-cost reference-bandwidth`.
4. Verify that routing table entries reflect the modified metrics.
5. Test end-to-end connectivity and observe the preferred path.

## Verification

- Use `show ip ospf interface` to view interface costs.
- Use `show ip route` to verify the selected paths.
