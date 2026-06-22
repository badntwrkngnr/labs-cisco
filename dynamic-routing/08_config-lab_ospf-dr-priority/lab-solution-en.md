# Lab Solution

## Commands and Configuration

```cisco
interface gigabitethernet0/0
 ip ospf priority 100
```

## Explanation

The highest OSPF priority wins DR election. A priority of 0 means the router will never become DR/BDR.

## Verification

```cisco
show ip ospf neighbor
show ip ospf interface gigabitethernet0/0
```
