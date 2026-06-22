# Lab Solution

## Commands and Configuration

```cisco
interface range gigabitethernet0/1-2
 switchport mode trunk
 channel-group 1 mode active
!
interface port-channel 1
 switchport mode trunk
```

## Explanation

LACP (mode active) is an open standard for EtherChannel negotiation. The port-channel interface inherits the configuration of the physical interfaces.

## Verification

```cisco
show etherchannel summary
show interfaces port-channel 1
```
