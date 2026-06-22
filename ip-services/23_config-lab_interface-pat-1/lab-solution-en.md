# Lab Solution

## Commands and Configuration

```cisco
access-list 1 permit 192.168.1.0 0.0.0.255
!
ip nat inside source list 1 interface gigabitethernet0/1 overload
!
interface gigabitethernet0/0
 ip nat inside
!
interface gigabitethernet0/1
 ip nat outside
```

## Explanation

Overload enables PAT, translating many inside addresses to the single outside interface IP using unique source port numbers.

## Verification

```cisco
show ip nat translations
show ip nat statistics
```
