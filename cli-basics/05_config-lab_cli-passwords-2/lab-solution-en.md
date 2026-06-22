# Config Lab: CLI Passwords 2 - Lab Solution

## Commands and Configuration

### Step 1: Access Switch SW1 and Apply the Following Configurations

```cisco
enable
configure terminal

username allison password hope
username danielle password love
username tyler password faith

line console 0
login local

line vty 0 4
login local
```

## Verification

### Step 2: To Validate the Configurations, Access R1 and Apply the Following Commands

```cisco
telnet 10.1.1.20 /source-interface loopback 0
```

### Step 3: If You Applied the Configurations Correctly, the Following Prompt Will Appear

```cisco
Trying 10.1.1.20 ... Open


User Access Verification

Username:
```

### Step 4: Enter the Username, Press ENTER, Enter the Created Password, and Press ENTER Again, as Shown in the Example Below

```cisco
Username: allison
Password: hope
```

> When typing the password, pay attention because the terminal remains static!

### Step 5: Log Out

```cisco
exit
```

The following prompt will appear:

```cisco
[Connection to 10.1.1.20 closed by foreign host]
```

### Step 6: Repeat Step 4 Until You Have Tested All Created Users

## Explanation

This lab demonstrates the use of a **local user database** (local login) instead of shared line passwords. When `login local` is configured on a line, the device checks the locally configured usernames and passwords for authentication.

In a real network, using individual usernames provides better accountability than shared passwords, because each session can be associated with a specific user account.
