# Lab Solution

## Commands and Configuration

```cisco
access-list 101 permit tcp 192.168.1.0 0.0.0.255 any eq 80
access-list 101 permit tcp 192.168.1.0 0.0.0.255 any eq 443
access-list 101 deny ip any any log
!
interface GigabitEthernet0/1
 ip access-group 101 in
```

## Explanation

Extended ACLs (100-199, 2000-2699) filter on source, destination, protocol, and ports. Place them closest to the source.

## Verification

```cisco
show access-lists 101
show ip interface GigabitEthernet0/1
```
