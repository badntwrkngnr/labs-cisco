# Basic Switch Setup - Lab Solution

![Topology](./assets/img/topology.png)

## Commands and Configuration

### Step 1: Configure Hostname

```cisco
enable
configure terminal
hostname sw-1
```

The prompt should appear as follows after applying the configuration:

```cisco
sw-1(config)#
```

### Step 2: Configure MOTD Banner

```cisco
banner motd # Access is prohibited to unauthorized persons! #
```

![Banner MOTD](./assets/img/banner-motd.png)

### Step 3: Configure Enable Password (Plain Text)

```cisco
enable password cisco
```

```cisco
show running-config
```

![Plain Text Password](./assets/img/plain-text-enable.png)

### Step 4: Configure Console Access

```cisco
line console 0
password console
login
history size 15
exec-timeout 6 45
logging synchronous
```

### Step 5: Configure Telnet Access

```cisco
line vty 0 4
password telnet
login
transport input telnet
history size 15
exec-timeout 8 20
logging synchronous
```

### Step 6: Configure SVI and Default Gateway

```cisco
interface vlan 1
ip address 192.168.1.2 255.255.255.0
no shutdown
```

```cisco
ip route 0.0.0.0 0.0.0.0 192.168.1.1
```

### Step 7: Monitor Port Traffic

![Monitoring SW-1 Ethernet 0/0 Port](./assets/img/wireshark-monitor.png)

### Step 8: Test Telnet and Observe Traffic

![Telnet Packets](./assets/img/telnet-packets.png)

![Telnet Traffic](./assets/img/telnet-0.png)

### Step 9: Enable Password Encryption

```cisco
service password-encryption
show running-config
```

![Weak Encrypted Password](./assets/img/enable-password.png)

### Step 10: Configure Secure Enable Password

```cisco
enable secret c15c0
```

![Enable Mode Passwords](./assets/img/secret-password-enable.png)

### Step 11: Configure Console Username

```cisco
username console secret c0ns0l3
```

### Step 12: Configure SSH Access

```cisco
username ssh secret s3cur3sh3ll
```

### Step 13: Generate SSH Key and Configure SSH

```cisco
ip domain-name example.dev
```

> Be careful when generating keys: to meet SSH v2 requirements, the RSA key modulus must be at least 768 bits.

```cisco
crypto key generate rsa
```

The following prompt will appear:

```cisco
The name for the keys will be: RT-1.example.dev
Choose the size of the key modulus in the range of 360 to 4096 for your
  General Purpose Keys. Choosing a key modulus greater than 512 may take
  a few minutes.

How many bits in the modulus [512]: (Enter a value equal to or greater than 768)
```

```cisco
ip ssh version 2
```

Now access the console and remote terminal configurations:

```cisco
line console 0
no password
login local
```

```cisco
line vty 0 4
no password
login local
```

## Verification

After completing all steps, verify with:

```cisco
show running-config
```

Ensure that:
- The hostname is `sw-1`
- The MOTD banner displays correctly
- Password encryption is enabled
- The enable secret is configured
- Console and VTY lines use local login
- SSH version 2 is active
- VLAN 1 has the correct IP address and default gateway
