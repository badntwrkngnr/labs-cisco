# Config Lab: OSPF Network Config 1

Configure legacy (traditional) OSPF (using network commands) between R1 and R2.

**This is an adaptation of the lab found at:** [CertSkills](https://www.certskills.com/clab521/#1621532681263-db181298-6349)

![Original Topology](./assets/img/original-topology.png)

## Objectives

This lab presents two sets of requirements. Both use the following rules:

1. Configure each router with a router-id of x.x.x.x where x equals the router number.
2. Use OSPF area 0 (zero).
3. Use process-id 20 for the OSPF process.
4. Provide a complete answer for both Scenario 1 and Scenario 2, as follows:
    - Scenario 1: Each network command must match only classful networks (class A, B, and C networks).
    - Scenario 2: Each network command must match the subnets of the router interfaces.

## Initial Configuration

![Topology](./assets/img/pnet-topology.png)

The configurations below show the initial state of R1 and R2.

**R1**

```cisco
hostname R1
!
interface ethernet0/1
 no shutdown
 ip address 192.168.4.1 255.255.255.240
!
interface ethernet0/2
 no shutdown
 ip address 192.168.4.129 255.255.255.240
```

**R2**

```cisco
hostname R2
!
interface ethernet0/1
 no shutdown
 ip address 192.168.4.2 255.255.255.240
!
interface ethernet0/2
 no shutdown
 ip address 192.168.2.193 255.255.255.240
```

## Lab Files

**Scenario 1**
- [Initial lab file](./assets/lab/config_lab_ospf_network_config_1_cenario-1_inicial.zip)
- [Solved lab file](./assets/lab/config_lab_ospf_network_config_1_cenario-1_resolvido.zip)

**Scenario 2**
- [Initial lab file](./assets/lab/config_lab_ospf_network_config_1_cenario-2_inicial.zip)
- [Solved lab file](./assets/lab/config_lab_ospf_network_config_1_cenario-2_resolvido.zip)
