# Lab Solution

## Commands and Configuration

```cisco
interface fa0/1
 switchport mode access
 switchport port-security
 switchport port-security maximum 1
 switchport port-security mac-address sticky
 switchport port-security violation shutdown
```

## Explanation

Port security is enabled with maximum 1 MAC, sticky learning, and shutdown violation mode.

## Verification

```cisco
show port-security
show port-security interface fa0/1
show mac address-table secure
```
