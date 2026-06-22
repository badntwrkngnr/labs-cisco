# Lab Solution

## Commands and Configuration

```cisco
ip nat inside source static 192.168.1.100 203.0.113.100
!
interface gigabitethernet0/0
 ip nat inside
!
interface gigabitethernet0/1
 ip nat outside
```

## Explanation

Static NAT creates a permanent one-to-one mapping, allowing bidirectional traffic between the inside local and inside global addresses.

## Verification

```cisco
show ip nat translations
```
