# Lab Solution

## Commands and Configuration

```cisco
access-list 1 permit 192.168.1.0 0.0.0.255
!
ip nat pool PUBLIC 203.0.113.10 203.0.113.12 netmask 255.255.255.248
!
ip nat inside source list 1 pool PUBLIC overload
!
interface gigabitethernet0/0
 ip nat inside
!
interface gigabitethernet0/1
 ip nat outside
```

## Explanation

PAT with a pool combines multiple public addresses with port translation, providing more capacity than a single interface address.

## Verification

```cisco
show ip nat translations
show ip nat statistics
```
