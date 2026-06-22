# Lab Solution

## Commands and Configuration

```cisco
interface gigabitethernet0/0
 ip ospf cost 100
!
router ospf 1
 auto-cost reference-bandwidth 10000
```

## Explanation

OSPF cost = reference bandwidth / interface bandwidth. On modern networks, the default reference bandwidth (100 Mbps) is too low, so it should be adjusted to accurately reflect Gigabit and faster links.

## Verification

```cisco
show ip ospf interface
show ip route
```
