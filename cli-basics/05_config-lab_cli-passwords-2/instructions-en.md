# Config Lab: CLI Passwords 2

## Objectives

Based on Wendell Odom's blog, author of the official CCNA guides, these labs were created with Packet Tracer and CML. Here is the link to the original lab:

- [Config Lab: CLI Passwords 2](https://www.certskills.com/clab102/)

Configure passwords to access switch SW1 via console and Telnet, using individual local usernames and passwords. Configure the passwords so that users must supply a username to log in from the console and via Telnet.

This lab begins with all interfaces shown in Figure 1 working, with IPv4 addresses configured, and all hosts able to ping other local hosts and hosts throughout the enterprise.

The specific rules for this lab are as follows:

1. Enable the use of the local database for login through Console or Telnet.
2. Create a user: Password "hope" for user "allison".
3. Create a user: Password "love" for user "danielle".
4. Create a user: Password "faith" for user "tyler".

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
 no shutdown
!
```

## Lab Files

To answer, simply think through the lab. Consult your primary CCNA study materials, your notes, and apply the configuration using the [initial lab file](./assets/lab/17_config_lab_cli_passwords_2_inicial.zip). Then check your answer against the [lab solution instructions](./lab-solution-en.md) and the [solved lab](./assets/lab/17_config_lab_cli_passwords_2_resolvido).

| Device | IP Address |
| --- | --- |
| PC | 10.1.1.11 |
| SRV | 10.1.1.22 |
