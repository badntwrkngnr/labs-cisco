# Lab Solution

## Commands and Configuration

```cisco
interface serial0/0/0
 encapsulation hdlc
 ip address 10.1.1.1 255.255.255.252
 no shutdown
```

## Explanation

HDLC is the default serial encapsulation on Cisco routers. It is proprietary and does not support authentication.

## Verification

```cisco
show interfaces serial0/0/0
ping 10.1.1.2
```
