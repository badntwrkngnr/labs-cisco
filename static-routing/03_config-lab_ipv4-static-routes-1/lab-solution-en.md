# Lab Solution

## Commands and Configuration

```cisco
! R1
ip route 192.168.2.0 255.255.255.0 192.168.12.2
ip route 192.168.3.0 255.255.255.0 192.168.12.2

! R2
ip route 192.168.1.0 255.255.255.0 192.168.12.1
ip route 192.168.3.0 255.255.255.0 192.168.23.3

! R3
ip route 192.168.1.0 255.255.255.0 192.168.23.2
ip route 192.168.2.0 255.255.255.0 192.168.23.2
```

## Explanation

Each router needs static routes for networks not directly connected. The next-hop must be reachable.

## Verification

```cisco
show ip route
ping 192.168.3.1 source 192.168.1.1
```
