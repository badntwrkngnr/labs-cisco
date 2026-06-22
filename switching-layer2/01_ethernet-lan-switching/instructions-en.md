# Ethernet LAN Switching

For this lab, we will use Jeremy's IT Lab as our reference. He used Packet Tracer in his video.
Be sure to show some support on his [video](https://www.youtube.com/watch?v=Ig0dSaOQDI8&list=PLxbwE86jKRgMpuZuLBivzlM8s2Dk5lXBQ&index=12) - he created a complete, free course for the CCNA 200-301!

I use PNETLab, but the images are compatible with EVE-NG.

![Topology](./assets/img/topology.png)

## Instructions

To ensure that both switches have their MAC address tables empty, clear dynamically learned MAC addresses.
All PCs have an empty ARP table.

The PC IP addresses are in the lab file.

1. If PC1 pings PC3, what messages will be sent across the network and which devices will receive them?

2. Open Wireshark, on any switch's ethernet 0/0 interface, and run a ping from PC1 to PC3 to verify the traffic flow.

3. Use pings to generate traffic on the network and allow the switches to learn the MAC addresses of all PCs on the network.

4. Use show commands on the switches to identify each PC's MAC address.

5. Clear the dynamic MAC addresses from each switch's MAC address table.

6. Now you can repeat the procedure for any PC, as long as you monitor the correct port, ok?
