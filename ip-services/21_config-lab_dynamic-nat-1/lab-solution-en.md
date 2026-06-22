# Lab Solution

## Commands and Configuration

```cisco
access-list 1 permit 192.168.1.0 0.0.0.255
!
ip nat pool PUBLIC 203.0.113.10 203.0.113.20 netmask 255.255.255.0
!
ip nat inside source list 1 pool PUBLIC
!
interface gigabitethernet0/0
 ip nat inside
!
interface gigabitethernet0/1
 ip nat outside
```

## Explanation

Dynamic NAT maps internal addresses to a pool of public addresses without port translation. Each inside host gets a unique public IP when active.

## Verification

```cisco
show ip nat translations
show ip nat statistics
```
