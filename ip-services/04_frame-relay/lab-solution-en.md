# Lab Solution

## Commands and Configuration

```cisco
interface serial0/0/0
 encapsulation frame-relay
 ip address 172.16.1.1 255.255.255.0
 frame-relay interface-dlci 101
 no shutdown
```

## Explanation

Frame Relay uses DLCI numbers to identify virtual circuits. Static mappings or Inverse ARP map DLCIs to IP addresses.

## Verification

```cisco
show frame-relay pvc
show frame-relay map
```
