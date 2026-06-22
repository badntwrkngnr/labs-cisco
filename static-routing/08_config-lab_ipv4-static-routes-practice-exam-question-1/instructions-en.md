# Config Lab: Static Routing - Practice Exam Question 1

This lab is based on a question I saw in an official Cisco practice exam. I only changed the addresses and routes to practice the concepts.

This lab aims to practice IPv4 addressing concepts, static routes, and how routers make forwarding decisions.

## Why Predicting Network Behavior Matters

This lab may seem simple at first glance - after all, it is just a few routers and static routes. But here is the point: the CCNA is the first serious contact with Network Engineering, and one of the skills we need to develop from the beginning is **predicting the behavior** of equipment, protocols, and the network as a whole.

In exams and labs, it is not enough to "configure and hope it works." You must be able, before running a `ping` or `traceroute`, to imagine the path packets will take, which router the forwarding decision will be made on, and what the result will be. This ability to **reason about the network**, rather than just memorize commands, is what separates those who understand from those who merely repeat. Therefore, in this lab, the central question is: based on the topology and configured routes, what is the expected behavior?

![Topology](./assets/img/topology.png)

## Lab Setup

The IP addresses were applied as shown in the topology. Carefully observe the status of router R1 interfaces when you run the command:

```cisco
show ip interface brief
```

![show ip interface brief](./assets/img/01-show-ip-int-brief.png)

The routes were applied as shown below:

![ip route](./assets/img/02-ip-route-commands.png)

## Questions

Based on the information provided, imagine that the link between R1 and R2 fails. When running a ping from PC1 to the servers, what is the expected behavior?

1. Packets sent to server S1 will pass through R1, R3, and onward
2. Packets sent to server S1 will pass through R1, R4, and onward
3. Packets sent to server S1 will be discarded
4. Packets sent to server S2 will pass through R1, R3, and onward
5. Packets sent to server S2 will pass through R1, R4, and onward
6. Packets sent to server S2 will be discarded

## Verification

To verify the answer, access R1 and apply the commands below (interface Ethernet 0/1 simulates the link failure with R2):

```cisco
enable
configure terminal
interface ethernet 0/1
shutdown
```

Then, access PC1 and run traceroute commands to each server:

```cisco
trace 192.168.10.1
```

```cisco
trace 192.168.20.2
```

Observe the command output and compare it with your answer. The lab file is available in this lab's resources - click [here](./assets/lab/08_config-lab_ipv4-static-routes-practice-exam-question-1.zip) to download.
