# Config Lab: OSPF Interface Config 2

Configure OSPF for the lab network shown in the topology. However, do not use the traditional configuration with network commands in OSPF configuration mode. Instead, use interface-level OSPF configuration.

**This is an adaptation of the lab found at:** [CertSkills](https://www.certskills.com/clab520/#1621538143010-3327296b-3256)

![Original Topology](./assets/img/original-topology.png)

## Objectives

The specific rules for this lab are:

1. Configure each router to use a router-id of x.x.x.x where x equals the router number.
2. Do not rely on interface IP addresses for the definition of router-IDs.
3. Use OSPF area 0 (zero).
4. Use process-id 50 for the OSPF process.
5. Enable OSPF directly on each interface, rather than using the indirect method with the OSPF network command.

> Assume that all interfaces shown in the lab are active (up) and working.

## Initial Configuration

![Topology](./assets/img/pnet-topology.png)

The configurations below show the initial state of R1 and R2.

**R1**

```cisco
hostname R1
!
interface ethernet0/1
 no shutdown
 ip address 10.50.100.97 255.255.255.224
!
interface loopback0
 no shutdown
 ip address 1.1.1.1 255.255.255.255
!
interface loopback1
 no shutdown
 ip address 10.50.100.129 255.255.255.224
```

**R2**

```cisco
hostname R2
!
interface ethernet0/1
 no shutdown
 ip address 10.50.100.98 255.255.255.224
!
interface loopback0
 no shutdown
 ip address 2.2.2.2 255.255.255.255
!
interface loopback1
 no shutdown
 ip address 10.50.101.1 255.255.255.224
```

## Lab Files

- [Initial lab file](./assets/lab/config_lab_ospf_interface_config_2_inicial.zip)
- [Solved lab file](./assets/lab/config_lab_ospf_interface_config_2_resolvido.zip)
