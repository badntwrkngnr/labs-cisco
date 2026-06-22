# Config Lab: OSPF Network Config 2

Configure legacy (traditional) OSPF (using network commands) among R1, R2, and R3. As a means of allowing you to practice the network command, this lab varies the requirements for the network commands on each router.

**This is an adaptation of the lab found at:** [CertSkills](https://www.certskills.com/clab522/)

![Original Topology](./assets/img/original-topology.png)

## Objectives

The specific rules for this lab, for all three routers, are:

1. Configure each router with a router-id of x.x.x.x where x equals the router number.
2. Use OSPF area 0 (zero).
3. Use process-id 5 for the OSPF process.
4. Additionally, because the network command can use many different wildcard masks, use the following rules when choosing the wildcard masks to be used on each router:
    - Router R1: Each network command must match only classful networks (class A, B, and C networks).
    - Router R2: Each network command must match the specific IPv4 addresses of the router interfaces.
    - Router R3: Each network command must match the subnets of the router interfaces.

> Note that in a real network, you would likely choose one style over another and use it on all routers. This lab uses a variety only to give you a variety of practice.

## Initial Configuration

![Topology](./assets/img/pnet-topology.png)

The configurations below show the initial state of R1, R2, and R3.

**R1**

```cisco
hostname R1
!
interface GigabitEthernet0/0
 no shutdown
 ip address 172.16.1.1 255.255.255.0
!
interface GigabitEthernet0/1
 no shutdown
 ip address 172.30.1.1 255.255.255.252
!
interface GigabitEthernet0/2
 no shutdown
 ip address 172.30.1.10 255.255.255.252
```

**R2**

```cisco
hostname R2
!
interface GigabitEthernet0/0
 no shutdown
 ip address 172.16.2.2 255.255.255.0
!
interface GigabitEthernet0/1
 no shutdown
 ip address 172.30.1.5 255.255.255.252
!
interface GigabitEthernet0/2
 no shutdown
 ip address 172.30.1.2 255.255.255.252
```

**R3**

```cisco
hostname R3
!
interface GigabitEthernet0/0
 no shutdown
 ip address 172.16.3.3 255.255.255.0
!
interface GigabitEthernet0/1
 no shutdown
 ip address 172.30.1.9 255.255.255.252
!
interface GigabitEthernet0/2
 no shutdown
 ip address 172.30.1.6 255.255.255.252
```

## Lab Files

- [Initial lab file](./assets/lab/config_lab_ospf_network_config_2_inicial.zip)
- [Solved lab file](./assets/lab/config_lab_ospf_network_config_2_resolvido.zip)
