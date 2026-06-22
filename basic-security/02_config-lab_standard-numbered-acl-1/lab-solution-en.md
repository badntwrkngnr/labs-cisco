# Lab Solution

## Commands and Configuration

```cisco
! On the router closest to the destination
access-list 10 permit 192.168.1.0 0.0.0.255
access-list 10 deny any
!
interface GigabitEthernet0/1
 ip access-group 10 out
```

## Explanation

Standard ACLs (1-99, 1300-1999) filter based on source IP only. They should be placed closest to the destination. The `deny any` at the end is implicit but shown for clarity.

## Verification

```cisco
show access-lists
show ip interface GigabitEthernet0/1
```
