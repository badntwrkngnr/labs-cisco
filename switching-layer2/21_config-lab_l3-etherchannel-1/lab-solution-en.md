# Lab Solution

## Commands and Configuration

```cisco
interface range gigabitethernet0/1-2
 no switchport
 channel-group 1 mode active
!
interface port-channel 1
 no switchport
 ip address 10.1.1.1 255.255.255.252
 no shutdown
```

## Explanation

Layer 3 EtherChannels bundle routed interfaces for increased bandwidth and redundancy without involving VLANs.

## Verification

```cisco
show etherchannel summary
show ip interface brief
ping 10.1.1.2
```
