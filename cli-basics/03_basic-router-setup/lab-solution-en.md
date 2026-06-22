# Lab Solution

## Commands and Configuration

```cisco
enable
configure terminal
hostname R1
enable secret cisco
!
banner motd # Authorized Access Only #
!
line console 0
 password console
 login
!
interface gigabitethernet0/0
 ip address 192.168.1.1 255.255.255.0
 no shutdown
!
end
write memory
```

## Explanation

The router hostname, enable secret, console password, banner, and interface IP are configured. The configuration is saved to NVRAM.

## Verification

```cisco
show running-config
show ip interface brief
```
