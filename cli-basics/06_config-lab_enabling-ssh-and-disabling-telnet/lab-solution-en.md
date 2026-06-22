# Config Lab: Enabling SSH and Disabling Telnet - Lab Solution

## Explanation

> Before starting:
It is important to note that the manufacturer recommends using SSH version 2. To satisfy this condition, a cryptographic key with at least 768 bits must be generated!

## Commands and Configuration

### Step 1: Log in to SW1

When clicking on the switch, you will receive the following prompt. Proceed with the previously configured passwords, which are listed in the [instructions](./instructions-en.md):

```cisco
User Access Verification

Password: certskills
SW1>enable
Password: certskills
SW1#
```

### Step 2: Configure the SSH Key for Remote Access

Now we will generate the cryptographic key. You will need to access global configuration mode:

```cisco
configure terminal
ip domain-name example.com
crypto key generate rsa
```

The following prompt will appear. Remember to configure the key with at least 768 bits so we can enable SSH version 2.

```cisco
The name for the keys will be: SW1.example.com
Choose the size of the key modulus in the range of 360 to 4096 for your
  General Purpose Keys. Choosing a key modulus greater than 512 may take
  a few minutes.

How many bits in the modulus [512]: 1024
% Generating 1024 bit RSA keys, keys will be non-exportable...
[OK] (elapsed time was 0 seconds)

SW1(config)#
*Oct  4 20:07:19.892: %SSH-5-ENABLED: SSH 1.99 has been enabled
```

After generating the key, configure SSH version 2:

```cisco
ip ssh version 2
```

To ensure that version 2 was enabled, run the following command in privileged mode:

```cisco
show ip ssh
```

If everything is correct, you will receive the following output in your terminal:

```cisco
SSH Enabled - version 2.0
Authentication methods:publickey,keyboard-interactive,password
Encryption Algorithms:aes128-ctr,aes192-ctr,aes256-ctr,aes128-cbc,3des-cbc,aes192-cbc,aes256-cbc
MAC Algorithms:hmac-sha1,hmac-sha1-96
Authentication timeout: 120 secs; Authentication retries: 3
Minimum expected Diffie Hellman key size : 1024 bits
IOS Keys in SECSH format(ssh-rsa, base64 encoded): SW1.example.com
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAAAgQCSIc1pkQIwnKq7HO85svggvD6iFd4wL0SX6s5F/e/O
b4Xm+66f9Kp+B1UX60xIhFSefz3XkW78xR3BfhRXP2Z0MZaGZJBQrSI80rfI+acR17+UxVfR9CIkh5SN
/max8AqhNb+u0XBUS5t5stwDcHzMVeJrO/ZBLOrJOIcDnO5AZQ==
```

> It is important to mention that the output may vary; the main point of attention should be the protocol version, ok?
Note that above it says **SSH Enabled - version 2.0**

### Step 3: Create User and Password According to Lab Rules

Before we begin, I would like to inform you that there may be a limitation in the image used. I need to investigate further (sorry guys :(), because according to the prompts below, it is not possible to choose the encryption type when creating the user password:

```cisco
SWT1(config)#username Barney secret 9 Rubble
ERROR: The secret you entered is not a valid encrypted secret.
To enter an UNENCRYPTED secret, do not specify type 9 encryption.
When you properly enter an UNENCRYPTED secret, it will be encrypted.

Please set a password for username

SWT1(config)#username Barney secret 8 Rubble
ERROR: The secret you entered is not a valid encrypted secret.
To enter an UNENCRYPTED secret, do not specify type 8 encryption.
When you properly enter an UNENCRYPTED secret, it will be encrypted.

Please set a password for username

SWT1(config)#username Barney secret 5 Rubble
ERROR: The secret you entered is not a valid encrypted secret.
To enter an UNENCRYPTED secret, do not specify type 5 encryption.
When you properly enter an UNENCRYPTED secret, it will be encrypted.

Please set a password for username
```

Now let us create the user Barney with encrypted password Rubble. Access global configuration mode and apply the command below:

```cisco
username Barney secret Rubble
```

### Step 4: Adjust Console and VTY Line Configuration

First, we will adjust console access. We must remove the previous configurations or the new ones will not work:

```cisco
line console 0
no password
no login
login local
exit
```

Now we will adjust access to the VTY lines. We must perform the same process we did when adjusting the console configuration:

```cisco
line vty 0 4
no password
no login
login local
transport input ssh
```

**Important detail:** pay attention so as not to forget the command *transport input ssh*

## Verification

To ensure that the configurations were applied correctly, you can verify the current device configuration:

```cisco
show running-config
```

You should pay attention to the points below:

```cisco
ip domain-name example.com
!
interface Vlan1
 ip address 10.1.1.20 255.255.255.0
!
ip route 0.0.0.0 0.0.0.0 10.1.1.1
ip ssh version 2
!
line con 0
 logging synchronous
 login local
line aux 0
line vty 0 4
 login local
 transport input ssh
!
```

To validate SSH functionality, access router R1 and test the connection:

```cisco
ssh 10.1.1.20
% No user specified nor available for SSH client
```

Note that if you do not specify the user, the command will not work. Run the command as shown below:

```cisco
ssh -l Barney 10.1.1.20
Password: Rubble
```

If the entered password is correct, you will enter user mode (we did not change the user privileges):

```cisco
SW1>
```

If you want to access or apply any configuration, you can access privileged mode:

```cisco
SW1>enable
Password: certskills
SW1#
```
