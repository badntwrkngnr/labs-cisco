# Lab Solution

## Commands and Configuration

```cisco
ip dhcp snooping
ip dhcp snooping vlan 10,20
!
interface gigabitethernet0/1
 ip dhcp snooping trust
!
interface range fa0/1 - 24
 ip dhcp snooping limit rate 10
```

## Explanation

Trusted ports connect to DHCP servers; untrusted ports (default) connect to clients. Rate limiting prevents DHCP starvation attacks.

## Verification

```cisco
show ip dhcp snooping
show ip dhcp snooping binding
show ip dhcp snooping statistics
```
