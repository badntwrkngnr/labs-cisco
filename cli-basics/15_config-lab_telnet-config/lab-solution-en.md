# Lab Solution

## Commands and Configuration

```cisco
enable
configure terminal
line vty 0 4
 password telnet
 login
 transport input telnet
end
```

## Explanation

Telnet uses a line password for authentication. Note that Telnet sends all data, including passwords, in plaintext. For production networks, SSH should be used instead.

## Verification

```cisco
show line vty 0 4
```
