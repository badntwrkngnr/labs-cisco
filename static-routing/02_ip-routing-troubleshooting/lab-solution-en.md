# Lab Solution

## Commands and Configuration

Fix missing or incorrect routes:

```cisco
! Example fix for a missing route
ip route 192.168.3.0 255.255.255.0 192.168.12.2
```

Enable routing if necessary:

```cisco
ip routing
```

## Explanation

Common issues include: missing routes, wrong next-hop, shutdown interfaces, disabled IP routing, or typo in network/mask.

## Verification

```cisco
show ip route
show ip interface brief
ping <destination>
traceroute <destination>
```
