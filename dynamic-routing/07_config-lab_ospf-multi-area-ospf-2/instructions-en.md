# Config Lab: OSPF Multi-Area 2

**This is an adaptation of the lab found at:** [CertSkills](https://www.certskills.com/clab552/)

![Original Topology](./assets/img/00-original-topology.png)

A router configuration can enable OSPF on an interface directly using the ip ospf interface subcommand. In fact, the configuration is more straightforward and obvious than the traditional old use of the OSPF network subcommand. This lab combines interface OSPF configuration with a multi-area OSPF design, with a little extra router ID configuration added for variety.

## Objectives

Configure OSPFv2 multi-area (that is, OSPF for IPv4) on the four routers shown in the figure. Use the area design shown in the figure. The configuration must use the ip ospf interface subcommand to enable OSPF on each interface, and must not use network commands in OSPF configuration mode. The specific rules for this lab are:

- Use OSPF process-ID 50 on all routers
- Use only ip ospf interface subcommands to enable OSPF on an interface
- Use the following OSPF router IDs and make each router use the method listed below when the router chooses its router ID:
  - Core1: 1.1.1.1 (explicitly configured)
  - Core2: 2.2.2.2 (explicitly configured)
  - Branch1: 172.30.99.1 (Based on loopback0 interface address 172.30.99.1/32)
  - Branch2: 172.30.99.2 (Based on loopback0 interface address 172.30.99.2/32)
- Use all default OSPF parameters unless otherwise requested
- Assume that all device interfaces shown in the lab are active, working, and correctly assigned IP addresses

## Initial Configuration

![PNETlab Topology](./assets/img/01-pnet-topology.png)

**CORE1**

```cisco
hostname CORE1
!
interface Ethernet0/1
 ip address 172.30.1.129 255.255.255.252
 no shutdown
!
interface Ethernet0/2
 ip address 172.30.1.193 255.255.255.248
 no shutdown
!
interface Loopback 0
 ip address 1.1.1.1 255.255.255.255
 no shutdown
```

**CORE2**

```cisco
hostname CORE2
!
interface Ethernet0/1
 ip address 172.30.1.130 255.255.255.252
 no shutdown
!
interface Ethernet0/2
 ip address 172.30.1.201 255.255.255.248
 no shutdown
!
interface Loopback 0
 ip address 2.2.2.2 255.255.255.255
 no shutdown
```

**BRANCH1**

```cisco
hostname BRANCH1
!
interface Ethernet0/1
 ip address 172.30.1.194 255.255.255.248
 no shutdown
!
interface Loopback 0
 ip address 172.30.99.1 255.255.255.255
 no shutdown
!
interface Loopback 1
 ip address 172.30.1.1 255.255.255.192
 no shutdown
```

**BRANCH2**

```cisco
hostname BRANCH2
!
interface Ethernet0/1
 ip address 172.30.1.202 255.255.255.248
 no shutdown
!
interface Loopback 0
 ip address 172.30.99.2 255.255.255.255
 no shutdown
!
interface Loopback 1
 ip address 172.30.1.65 255.255.255.192
 no shutdown
```

## Lab Files

- [Initial lab file](./assets/lab/config_lab_ospf_multi_area_2_inicial.zip)
- [Solved lab file](./assets/lab/config_lab_ospf_multi_area_2_resolvido.zip)
