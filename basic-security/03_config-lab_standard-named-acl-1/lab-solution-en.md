# Lab Solution

## Commands and Configuration

```cisco
ip access-list standard BLOCK_GUEST
 permit 192.168.10.0 0.0.0.255
 deny 192.168.20.0 0.0.0.255
!
interface GigabitEthernet0/1
 ip access-group BLOCK_GUEST out
```

## Explanation

Named ACLs use descriptive names and allow easier editing of individual entries. Standard named ACLs only filter on source address.

## Verification

```cisco
show access-lists BLOCK_GUEST
show ip interface GigabitEthernet0/1
```
