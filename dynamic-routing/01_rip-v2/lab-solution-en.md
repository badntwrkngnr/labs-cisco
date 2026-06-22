# Lab Solution

## Commands and Configuration

```cisco
router rip
 version 2
 no auto-summary
 network 192.168.1.0
 network 10.0.0.0
```

## Explanation

RIPv2 sends subnet mask information, supports VLSM, and uses multicast (224.0.0.9). Disabling auto-summary ensures specific subnets are advertised.

## Verification

```cisco
show ip protocols
show ip route
```
