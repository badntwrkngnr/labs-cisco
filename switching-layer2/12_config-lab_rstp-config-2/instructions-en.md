# RSTP Configuration

## Objectives

Configure Rapid Spanning Tree Protocol (RSTP - 802.1w) for faster convergence compared to legacy STP.

## Instructions

1. Enable RSTP on all switches.
2. Verify the spanning-tree mode is set to rapid-pvst.
3. Identify the root bridge and verify port roles.
4. Optionally configure root bridge priority.

## Verification

- Use `show spanning-tree` to verify RSTP mode.
- Use `show spanning-tree summary`.
- Test failover by shutting down a root port and observing reconvergence time.
