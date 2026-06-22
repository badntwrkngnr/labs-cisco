# Lab Solution

## Commands and Configuration

```cisco
line console 0
 exec-timeout 5 0
 logging synchronous
line vty 0 4
 exec-timeout 5 0
 logging synchronous
 login local
```

## Explanation

Exec timeout limits idle sessions. Synchronous logging prevents syslog messages from interrupting command entry.

## Verification

```cisco
show running-config | section line
```
