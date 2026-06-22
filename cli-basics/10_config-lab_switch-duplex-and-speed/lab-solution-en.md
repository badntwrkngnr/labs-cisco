# Lab Solution

## Commands and Configuration

```cisco
interface fa0/1
 speed 100
 duplex full
```

## Explanation

Manually setting speed and duplex prevents auto-negotiation mismatches. In modern networks, auto-negotiation is usually preferred, but manual settings are required when connected to older devices.

## Verification

```cisco
show interfaces status
show interfaces fa0/1
```
