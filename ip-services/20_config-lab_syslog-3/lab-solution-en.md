# Lab Solution

## Commands and Configuration

```cisco
logging 192.168.1.100
logging trap informational
service timestamps log datetime msec
```

## Explanation

Syslog messages are sent to the remote server at 192.168.1.100. The trap level controls which severity levels are forwarded.

## Verification

```cisco
show logging
```
