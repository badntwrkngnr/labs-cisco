# Static NAT

## Objectives

Configure static NAT to create a one-to-one mapping between a private internal address and a public external address.

## Instructions

1. Identify the inside local and inside global addresses.
2. Configure the static NAT mapping.
3. Designate the inside and outside NAT interfaces.
4. Verify the static translation works bidirectionally.

## Verification

- Use `show ip nat translations` to verify the static entry.
- Test connectivity from outside to the inside global address.
