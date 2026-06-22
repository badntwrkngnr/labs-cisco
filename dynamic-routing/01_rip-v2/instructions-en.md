# RIPv2 Configuration

## Objectives

Configure Routing Information Protocol version 2 (RIPv2) to provide dynamic routing in a small IPv4 network.

## Instructions

1. Enable RIPv2 routing on all routers.
2. Disable auto-summary to propagate specific subnet routes.
3. Advertise the directly connected networks using the `network` command.
4. Verify that all routers have learned routes via RIP.
5. Analyze the routing table and verify end-to-end connectivity.

## Verification

- Use `show ip protocols` to verify RIPv2 is running.
- Use `show ip route` to check for RIP-learned routes (R).
- Use `debug ip rip` to observe RIP updates (use with caution).
