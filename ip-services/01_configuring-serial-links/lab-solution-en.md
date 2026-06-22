# Lab Solution

## Commands and Configuration

```cisco
! DCE side
interface serial0/0/0
 clock rate 64000
 ip address 192.168.12.1 255.255.255.252
 no shutdown
```

## Explanation

The DCE interface provides the clocking. Both sides need IP addresses in the same subnet.

## Verification

```cisco
show controllers serial0/0/0
show ip interface brief
ping 192.168.12.2
```
