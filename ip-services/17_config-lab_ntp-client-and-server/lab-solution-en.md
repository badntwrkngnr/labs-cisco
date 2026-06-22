# Lab Solution

## Commands and Configuration

```cisco
! Server
ntp master 3

! Client
ntp server 192.168.1.1
```

## Explanation

The NTP master defines the local clock as a stratum source. Clients synchronize to the configured server.

## Verification

```cisco
show ntp status
show ntp associations
show clock
```
