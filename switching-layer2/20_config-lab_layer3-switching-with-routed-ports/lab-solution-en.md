# Lab Solution

## Commands and Configuration

```cisco
ip routing
!
interface vlan 10
 ip address 192.168.10.1 255.255.255.0
 no shutdown
!
interface vlan 20
 ip address 192.168.20.1 255.255.255.0
 no shutdown
```

## Explanation

Multilayer switches can route between VLANs using SVIs, eliminating the need for an external router for inter-VLAN routing.

## Verification

```cisco
show ip route
show ip interface brief
ping 192.168.20.2 source 192.168.10.1
```
