# Lab Solution

## Commands and Configuration

```cisco
interface serial0/0/0
 encapsulation ppp
 ip address 10.1.1.1 255.255.255.252
 no shutdown
```

## Explanation

PPP supports authentication (PAP/CHAP), error detection, and multiple Layer 3 protocols.

## Verification

```cisco
show interfaces serial0/0/0
ping 10.1.1.2
```
