# Layer 3 EtherChannel

## Objectives

Create a Layer 3 EtherChannel bundle for routed traffic between multilayer switches or routers.

## Instructions

1. Use `no switchport` on the physical interfaces to make them routed ports.
2. Bundle the interfaces into a PortChannel.
3. Configure an IP address on the port-channel interface.
4. Verify the EtherChannel operates at Layer 3.

## Verification

- Use `show etherchannel summary`.
- Use `show ip interface brief`.
- Use `ping` across the Layer 3 EtherChannel.
