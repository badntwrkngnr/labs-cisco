# Config Lab: OSPF Multi-Area 1

**This is an adaptation of the lab found at:** [CertSkills](https://www.certskills.com/clab551/)

![Original Topology](./assets/img/00-original-topology.png)

When using the OSPF network command, whether in single-area or multi-area, you must be careful with the wildcard mask used and which interfaces each network command matches. With multiple areas, this concern increases, because an incorrect match can place a router interface in the wrong area. This OSPF lab offers a small multi-area OSPF design and asks you to enable OSPFv2 with network commands, specifically to practice these commands.

## Objectives

Configure OSPFv2 multi-area (that is, OSPF for IPv4) on the four routers shown in the figure. Use the area design shown in the figure. The configuration must use OSPF network commands and must not use the ip ospf interface subcommand. The specific rules for this lab are:

- Use OSPF process-ID 10 on all routers
- Use only the network command to enable OSPF on interfaces
- Use one network command for each router interface shown in the figure. This network command must use a wildcard mask that matches all IP addresses in the subnet connected to the interface. (Note: I added this rule in the lab only so there is a correct way to answer this lab; in real life many different wildcard masks can be used.)
- Configure router-IDs explicitly in OSPF configuration mode, with router IDs as follows:
  - Core1: 1.1.1.1
  - Core2: 2.2.2.2
  - Branch1: 10.10.10.10
  - Branch2: 20.20.20.20
- Use all default OSPF parameters unless otherwise requested
- Assume that all device interfaces shown in the lab are active, working, and correctly assigned IP addresses

## Initial Configuration

![PNETlab Topology](./assets/img/01-pnet-topology.png)

**CORE1**

```cisco
hostname CORE1
!
interface Ethernet0/1
 ip address 100.100.100.1 255.255.255.252
 no shutdown
!
interface Loopback0
 ip address 1.1.1.1 255.255.255.255
 no shutdown
!
interface Ethernet0/2
 ip address 100.100.100.129 255.255.255.192
 no shutdown
```

**CORE2**

```cisco
hostname CORE2
!
interface Ethernet0/1
 ip address 100.100.100.2 255.255.255.252
 no shutdown
!
interface Loopback0
 ip address 2.2.2.2 255.255.255.255
 no shutdown
!
interface Ethernet0/2
 ip address 100.100.100.193 255.255.255.192
 no shutdown
```

**BRANCH1**

```cisco
hostname BRANCH1
!
interface Ethernet0/1
 ip address 100.100.100.130 255.255.255.192
 no shutdown
!
interface Loopback0
 ip address 10.10.10.10 255.255.255.255
 no shutdown
!
interface Loopback1
 ip address 100.100.101.126 255.255.255.128
 no shutdown
```

**BRANCH2**

```cisco
hostname BRANCH2
!
interface Ethernet0/1
 ip address 100.100.100.194 255.255.255.192
 no shutdown
!
interface Loopback0
 ip address 20.20.20.20 255.255.255.255
 no shutdown
!
interface Loopback1
 ip address 100.100.101.254 255.255.255.128
 no shutdown
```

## Lab Files

- [Initial lab file](./assets/lab/config_lab_ospf_multi_area_1_inicial.zip)
- [Solved lab file](./assets/lab/config_lab_ospf_multi_area_1_resolvido.zip)
