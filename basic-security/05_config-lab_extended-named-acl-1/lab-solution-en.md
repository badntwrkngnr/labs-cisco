# Lab Solution

## Commands and Configuration

```cisco
ip access-list extended FILTER_WEB
 permit tcp 10.1.1.0 0.0.0.255 any eq 80
 permit tcp 10.1.1.0 0.0.0.255 any eq 443
 deny ip 10.1.2.0 0.0.0.255 any
 permit ip any any
!
interface GigabitEthernet0/0
 ip access-group FILTER_WEB in
```

## Explanation

Extended named ACLs provide granular control over traffic types and directions. Always place extended ACLs as close to the source as possible.

## Verification

```cisco
show access-lists FILTER_WEB
show ip interface GigabitEthernet0/0
```
