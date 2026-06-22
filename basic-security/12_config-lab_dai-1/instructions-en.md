# Dynamic ARP Inspection (DAI)

## Objectives

Configure Dynamic ARP Inspection to prevent ARP spoofing and man-in-the-middle attacks on the local network.

## Instructions

1. Enable DHCP snooping as a prerequisite (DAI uses the DHCP snooping binding database).
2. Enable Dynamic ARP Inspection on the required VLANs.
3. Configure trusted interfaces (interfaces connecting to other switches or routers).
4. Configure untrusted interfaces (interfaces connecting to end devices).
5. Verify ARP traffic is being inspected and validated.

## Verification

- Use `show ip arp inspection` to verify DAI status.
- Use `show ip arp inspection interfaces` to check trust status.
- Use `show ip arp inspection statistics` to view inspection results.
