# Lab Solution

## Commands and Configuration

```cisco
interface gigabitethernet0/0
 ip address dhcp
 no shutdown
```

## Explanation

The router acts as a DHCP client, obtaining its IP configuration dynamically.

## Verification

```cisco
show ip interface brief
show dhcp lease
```
