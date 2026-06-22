# Config Lab: OSPF Interface Config 1

Configure OSPF for the lab network shown in the topology. However, do not use the traditional configuration with network commands in OSPF configuration mode. Instead, use interface-level OSPF configuration.

**This is an adaptation of the lab found at:** [CertSkills](https://www.certskills.com/clab519/#1621529957863-520a29fa-582d)

![Original Topology](./assets/img/original-topology.png)

## Objectives

The specific rules for this lab are:

1. Configure each router to use a router-id of x.x.x.x where x equals the router number.
2. Do not rely on interface IP addresses for router-ID definition.
3. Use OSPF area 0 for all interfaces.
4. Enable OSPF directly on each interface, rather than using the indirect method with the OSPF network command.

> Assume that all interfaces shown in the lab are active (up) and working.

## Initial Configuration

![Topology](./assets/img/pnet-topology.png)

The configurations below show the initial state of R1, R2, and R3.

**R1**

```cisco
hostname R1
!
interface ethernet0/0
 no shutdown
 ip address 172.21.1.1 255.255.255.128
!
interface ethernet0/1
 no shutdown
 ip address 172.30.1.1 255.255.255.252
!
interface ethernet0/2
 no shutdown
 ip address 172.30.1.10 255.255.255.252
```

**R2**

```cisco
hostname R2
!
interface ethernet0/0
 no shutdown
 ip address 172.22.2.2 255.255.255.192
!
interface ethernet0/1
 no shutdown
 ip address 172.30.1.5 255.255.255.252
!
interface ethernet0/2
 no shutdown
 ip address 172.30.1.2 255.255.255.252
```

**R3**

```cisco
hostname R3
!
interface ethernet0/0
 no shutdown
 ip address 172.23.3.3 255.255.255.224
!
interface ethernet0/1
 no shutdown
 ip address 172.30.1.9 255.255.255.252
!
interface ethernet0/2
 no shutdown
 ip address 172.30.1.6 255.255.255.252
```

## Lab Files

- [Initial lab file](./assets/lab/config_lab_ospf_interface_config_1_inicial.zip)
- [Solved lab file](./assets/lab/config_lab_ospf_interface_config_1_resolvido.zip)
