# Basic Switch Configuration

For this lab, we will use Jeremy's IT Lab as our reference. He used Packet Tracer in his video.
Be sure to show some support on his [video](https://www.youtube.com/watch?v=SDocmq1c05s&list=PLxbwE86jKRgMpuZuLBivzlM8s2Dk5lXBQ&index=9) - he created a complete, free course for the CCNA 200-301!

I use PNETLab, but the images are compatible with EVE-NG.

![Topology](./assets/img/topology.png)

## Instructions

1. Change the hostname of the router and switch to R1 and SW1 respectively.
    - Use the `hostname` command in global configuration mode.
2. Configure an unencrypted enable password (CCNA) on both devices.
3. Return to user EXEC mode and test the applied password.
4. View the password with the `show running-configuration` command.
5. Ensure that the current password, and all future passwords, are encrypted.
6. View the password again with the `show running-configuration` command.
7. Configure a more secure encrypted enable password to access privileged EXEC mode on both devices (Cisco).
8. Return to user EXEC mode and test the password to access privileged EXEC mode again. Which password was accepted?
9. View the passwords again with the `show running-configuration` command.
    - What type of encryption is used for the `enable password`?
    - What type of encryption is used for the `enable secret`?
10. Save the current configuration so it is stored in the startup configuration.
