# Lab Solution

## Commands and Configuration

```cisco
enable
configure terminal
interface vlan 1
 ip address 192.168.1.2 255.255.255.0
 no shutdown
exit
ip default-gateway 192.168.1.1
end
```

## Explanation

The SVI on VLAN 1 is configured with an IP address. The default gateway allows the switch to communicate outside its local subnet.

## Verification

```cisco
show ip interface brief
ping 192.168.1.1
```
