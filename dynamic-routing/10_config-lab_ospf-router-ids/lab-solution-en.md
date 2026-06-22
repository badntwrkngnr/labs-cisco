# Lab Solution

## Commands and Configuration

```cisco
router ospf 1
 router-id 1.1.1.1
end
clear ip ospf process
```

## Explanation

Manually configuring the router ID ensures consistency. The OSPF process must be cleared for the new router ID to take effect.

## Verification

```cisco
show ip ospf
show ip ospf neighbor
```
