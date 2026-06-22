# Lab Solution

## Commands and Configuration

```cisco
interface serial0/0/0
 ip ospf network point-to-point
```

## Explanation

Point-to-point network types skip DR/BDR election. Changing network types can resolve adjacency issues in certain topologies.

## Verification

```cisco
show ip ospf interface
show ip ospf neighbor
```
