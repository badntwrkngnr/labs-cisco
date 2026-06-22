# Lab Solution

## Commands and Configuration

```cisco
interface range fa0/1 - 24
 switchport mode access
 switchport port-security
 switchport port-security maximum 2
 switchport port-security mac-address sticky
 switchport port-security violation restrict
```

## Explanation

Port security limits MAC addresses on access ports. Sticky MAC dynamically learns and saves MAC addresses. Violation modes: shutdown (default), restrict (drops packets and logs), protect (silently drops).

## Verification

```cisco
show port-security
show port-security interface fa0/1
show port-security address
```
