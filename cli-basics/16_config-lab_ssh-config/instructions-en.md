# SSH Configuration

## Objectives

Configure Secure Shell (SSH) access on a Cisco device to enable encrypted remote management.

## Instructions

1. Configure a domain name for the device.
2. Generate an RSA key pair with sufficient modulus size (at least 768 bits, preferably 1024 or 2048).
3. Enable SSH version 2.
4. Create a local username with secret password.
5. Configure VTY lines to accept only SSH connections using local authentication.

## Verification

- Use `show ip ssh` to verify SSH version and settings.
- Use `show crypto key mypubkey rsa` to verify the RSA key.
- Test SSH connectivity from a remote host.
