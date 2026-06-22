# Lab Solution

## Commands and Configuration

```cisco
ipv6 route 2001:db8:acad:2::/64 2001:db8:acad:12::2
ipv6 route 2001:db8:acad:3::/64 2001:db8:acad:12::2
```

## Explanation

IPv6 static routes use the same logic as IPv4 but with IPv6 addresses and prefixes.

## Verification

```cisco
show ipv6 route
ping ipv6 2001:db8:acad:3::1 source 2001:db8:acad:1::1
```
