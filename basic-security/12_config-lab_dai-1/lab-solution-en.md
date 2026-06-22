# Lab Solution

## Commands and Configuration

```cisco
ip arp inspection vlan 10,20
!
interface gigabitethernet0/1
 ip arp inspection trust
!
interface range fa0/1 - 24
 ip arp inspection limit rate 15
```

## Explanation

DAI validates ARP packets against the DHCP snooping binding table. Trusted interfaces bypass inspection. Rate limiting prevents ARP flooding.

## Verification

```cisco
show ip arp inspection
show ip arp inspection interfaces
show ip arp inspection statistics
```
