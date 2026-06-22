# Lab Solution

## Commands and Configuration

```cisco
interface gigabitethernet0/1
 ip helper-address 192.168.1.10
```

## Explanation

The `ip helper-address` command forwards UDP broadcasts (including DHCP) to the specified server. By default it forwards port 67/68 DHCP traffic among other UDP services.

## Verification

```cisco
show running-config | include helper
```
