# Lab Solution

## Commands and Configuration

```cisco
ip domain-name example.com
crypto key generate rsa
! Enter 1024 or higher when prompted
ip ssh version 2
!
username admin secret cisco
!
line vty 0 4
 login local
 transport input ssh
```

## Explanation

SSH requires a domain name for key generation. RSA keys of at least 768 bits are needed for SSHv2. VTY lines must use `login local` for username authentication and `transport input ssh` to restrict access to SSH only.

## Verification

```cisco
show ip ssh
show crypto key mypubkey rsa
```
