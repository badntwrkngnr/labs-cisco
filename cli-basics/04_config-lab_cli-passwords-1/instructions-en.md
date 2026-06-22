# Config Lab: CLI Passwords 1

## Objectives

Based on Wendell Odom's blog, author of the official CCNA guides, these labs were created with Packet Tracer and CML. Here is the link to the original lab:

- [Config Lab: CLI Passwords 1](https://www.certskills.com/clab101/)

Configure passwords to access switch SW1 via console and Telnet. Also configure a password to access privileged mode. Set passwords so all users use the same password to access user mode from the console, without requiring an individual username. Similarly, use a single password for all users accessing the switch via Telnet to reach user mode.

This lab begins with all interfaces shown in Figure 1 working, with IPv4 addresses configured, and all hosts able to ping other local hosts and hosts throughout the enterprise.

The specific rules for this lab are as follows:

1. Use the password "joy" to protect console access for all users of switch SW1.
2. Use the password "peace" to protect Telnet access for all users of switch SW1.
3. Use the password "kindness" to protect privileged mode access for all users, using the most secure configuration option.

## Topology

**Original Topology**
![Original Topology](./assets/img/00-topology.png)

**EVE/PNETLAB Topology**
![EVE/PNETLAB Topology](./assets/img/01-topology.png)

## Initial Configuration

Below is the configuration applied to switch SW1 before you begin working on this lab. Basically, the switch has already been configured with an IP address and a default gateway to allow Telnet access.

```cisco
hostname SW1
ip route 0.0.0.0 0.0.0.0 10.1.1.1
!
interface vlan1
 ip address 10.1.1.20 255.255.255.0
```

## Lab Files

To answer, simply think through the lab. Consult your primary CCNA study materials, your notes, and apply the configuration using the [initial lab file](./assets/lab/16_config_lab_cli_passwords_1_inicial.zip). Then check your answer against the [lab solution instructions](./lab-solution-en.md) and the [solved lab](./assets/lab/16_config_lab_cli_passwords_1_resolvido).

| Device | IP Address |
| --- | --- |
| PC | 10.1.1.11 |
| SRV | 10.1.1.22 |
