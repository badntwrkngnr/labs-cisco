# Telnet Configuration

## Objectives

Configure Telnet access on a Cisco device for remote management and understand its security limitations.

## Instructions

1. Configure a password on the VTY lines for Telnet access.
2. Enable login authentication on the VTY lines.
3. Configure the device IP address for management access.
4. Test Telnet connectivity from a remote host.
5. Observe that Telnet transmits data in plaintext.

## Verification

- Use `show line vty 0 4` to verify VTY configuration.
- Capture Telnet traffic and observe unencrypted passwords.
