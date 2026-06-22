# Lab Solution

## Commands and Configuration

```cisco
vlan 10
 name SALES
vlan 20
 name ENGINEERING
!
interface fastethernet0/1
 switchport mode access
 switchport access vlan 10
!
interface fastethernet0/2
 switchport mode access
 switchport access vlan 20
```

## Explanation

VLANs divide a single broadcast domain into multiple isolated broadcast domains. Devices in different VLANs require a Layer 3 device to communicate.

## Verification

```cisco
show vlan brief
show interfaces switchport
```
