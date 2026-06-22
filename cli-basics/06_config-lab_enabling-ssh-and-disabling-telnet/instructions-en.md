# Config Lab: Enabling SSH and Disabling Telnet

## Objectives

You will configure a Cisco switch to support SSH and not support Telnet. From the user's perspective, an attempt to connect via Telnet must be rejected so the user never sees a password or username prompt. SSH users must be granted access if they provide a correct username and password. For this lab, the switch has already been configured to support IP and basic passwords; your task is to update the configuration to support only SSH for remote users.

The specific rules for this lab are as follows:

1. Configure SSH to use a cryptographic key.
2. Create the SSH key so that it uses the domain name 'example.com' as input.
3. Create a username/password pair Barney/Rubble with the best possible password encryption.
4. Enable support for SSH, and only SSH, using the locally created usernames/passwords.

## Topology

**Original Topology**
![Original Topology](./assets/img/00-topology.png)

**EVE/PNETLAB Topology**
![EVE/PNETLAB Topology](./assets/img/01-topology.png)

## Initial Configuration

This lab begins with a switch that has been configured to allow both Telnet and SSH connections, both using a simple IP address. The management IP address and CLI access passwords for user mode and privileged (enable) mode have already been set. Below we can observe this configuration:

```cisco
hostname SW1
enable secret 5 certskills
ip route 0.0.0.0 0.0.0.0 10.1.1.1
!
interface Ethernet0/0
 switchport trunk allowed vlan 1
 switchport trunk encapsulation dot1q
 switchport mode trunk
!
interface vlan1
 ip address 10.1.1.20 255.255.255.0
 no shutdown
!
line con 0
 password certskills
 logging synchronous
 login
line aux 0
line vty 0 4
 password certskills
 login
```

## Lab Files

To answer, simply think through the lab. Consult your primary CCNA study materials, your notes, and apply the configuration using the [initial lab file](./assets/lab/18_config_lab_enabling_ssh_and_disabling_telnet_inicial.zip). Then check your answer against the [lab solution instructions](./lab-solution-en.md) and the [solved lab](./assets/lab/18_config_lab_enabling_ssh_and_disabling_telnet_resolvido).

| Device | IP Address |
| --- | --- |
| PC | 10.1.1.11 |
| SRV | 10.1.1.22 |
