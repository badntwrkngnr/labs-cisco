# Lab Solution

## Commands and Configuration

```cisco
! Switch
interface gigabitethernet0/1
 switchport mode trunk
!
! Router
interface gigabitethernet0/0.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0
!
interface gigabitethernet0/0.20
 encapsulation dot1Q 20
 ip address 192.168.20.1 255.255.255.0
```

## Explanation

Router-on-a-stick uses subinterfaces with 802.1Q encapsulation to route between VLANs over a single physical link.

## Verification

```cisco
show vlans
show ip interface brief
ping 192.168.20.2 source 192.168.10.1
```
