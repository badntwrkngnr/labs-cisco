# Lab Solution

## Commands and Configuration

```cisco
interface gigabitethernet0/1
 switchport mode trunk
 switchport trunk allowed vlan 10,20,30
```

## Explanation

Restricting allowed VLANs on a trunk improves security and reduces unnecessary broadcast traffic.

## Verification

```cisco
show interfaces trunk
```
