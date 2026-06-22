# Dynamic NAT

## Objectives

Configure dynamic NAT to translate multiple private IPv4 addresses to a pool of public IPv4 addresses.

## Instructions

1. Define an access control list for the inside local addresses to be translated.
2. Create a NAT pool with public addresses.
3. Configure the inside and outside interfaces.
4. Link the ACL to the NAT pool.
5. Verify dynamic translations are created.

## Verification

- Use `show ip nat translations` to view active translations.
- Use `show ip nat statistics` to verify NAT pool usage.
- Test connectivity from inside hosts to outside networks.
