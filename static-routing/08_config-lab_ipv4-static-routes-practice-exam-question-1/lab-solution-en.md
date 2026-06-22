# Lab Solution: Static Routing - Practice Exam Question 1

## Explanation

This lab tests your ability to **predict network behavior** based on configured static routes and interface states. The key to understanding this scenario is to analyze what happens when the link between R1 and R2 fails (simulated with `shutdown` on Ethernet 0/1).

## Route Analysis

When R1's Ethernet 0/1 interface is shut down:
- The static route pointing to the next-hop through that interface **is not automatically removed** from R1
- However, the next-hop becomes **unreachable**
- Router R1 must find other valid routes for the destinations

## Expected Behavior

After the R1-R2 link failure:

- **For Server S1** (192.168.10.0/24): Packets are forwarded via R1 -> R3, as this is the valid alternative static route.
- **For Server S2** (192.168.20.0/24): Packets are discarded because there is no valid alternative static route after the direct link fails.

## Verification

### Simulate the Link Failure

```cisco
enable
configure terminal
interface ethernet 0/1
shutdown
```

### Check Routes on R1

```cisco
show ip route
```

### Test Traceroute from PC1

```cisco
trace 192.168.10.1
trace 192.168.20.2
```

## Conclusion

The correct answer depends on the specific routes configured in your topology. The objective of this lab is to develop the ability to **reason about packet forwarding** before running commands, training your analysis of the routing table and understanding of next-hop reachability.
