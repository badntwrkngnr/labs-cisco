# Lab Solution

## Commands and Configuration

```cisco
spanning-tree mode rapid-pvst
!
! Optional: set root bridge
spanning-tree vlan 1-4094 root primary
```

## Explanation

RSTP (802.1w) converges much faster than legacy STP (802.1D) by eliminating the listening and learning delays for edge ports.

## Verification

```cisco
show spanning-tree
show spanning-tree summary
```
