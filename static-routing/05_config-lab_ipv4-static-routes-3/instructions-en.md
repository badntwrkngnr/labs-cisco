# IPv4 Static Routes

## Objectives

Configure IPv4 static routes to provide connectivity between networks that are not directly connected.

## Instructions

1. Identify the remote networks that need to be reached.
2. Determine the correct next-hop IP address or exit interface for each route.
3. Configure static routes on each router using `ip route`.
4. Verify connectivity to all remote networks.

## Verification

- Use `show ip route` to verify static routes are installed.
- Use `ping` and `traceroute` to test end-to-end connectivity.
