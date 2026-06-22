# Basic Switch Setup

![Topology](./assets/img/topology.png)

## Objectives

This lab will test your ability to configure basic settings such as **hostname**, **banner motd**, **access passwords**, and **terminal options** on a Cisco switch running on an IOL image in PNETLab or EVE-NG.

**This is an adaptation of the lab found at:** [Packet Tracer Network](https://www.packettracernetwork.com/labs/lab1-basicswitchsetup.html)

## Instructions

1. Connect to the switch console (double-click the device) and configure the **hostname** as `sw-1`.

2. Configure the **message of the day (MOTD)** as `"Access is prohibited to unauthorized persons!"`.

3. Configure the **enable password** as `"cisco"`. The password must be in plain text.
    - Verify the current device configuration.
    - **What was observed in the enable password configuration?**

4. Configure **console access** with the following settings:
    - Password: `console`
    - History size: 15 commands
    - Timeout: 6 minutes and 45 seconds
    - Synchronous logging

5. Configure **Telnet access** with the following settings:
    - Password: `telnet`
    - History size: 15 commands
    - Timeout: 8 minutes and 20 seconds
    - Synchronous logging

6. Configure the **SVI (VLAN 1) IP address** as `192.168.1.2/24` and its **default gateway** as `192.168.1.1`.

7. Using Wireshark, monitor the switch port connected to the router.

8. Test Telnet connectivity from VPC1 using the CLI.
    - Observe the Telnet protocol traffic.
    - Apply some commands to better observe the protocol behavior.

9. Configure the **password encryption service** on the switch.
    - Verify the current device configuration.
    - **What was observed, and what are the issues with this configuration?**

10. Configure the **enable password** as `"c15c0"`. The password must be encrypted with **MD5**.
    - Access privileged mode and answer the questions below:
    - **What password was accepted when accessing the device?**
    - **Can you explain what happened for the device to accept that password?**

11. Change the **console access** settings to the following:
    - Username: `console`
    - Password: `c0ns0l3`

12. Configure **SSH access** with the following settings:
    - Username: `ssh`
    - Password: `s3cur3sh3ll`

13. Observe the behavior of SSH traffic and compare it with Telnet traffic.
    - **Could you briefly explain the difference in how the protocols work?**
