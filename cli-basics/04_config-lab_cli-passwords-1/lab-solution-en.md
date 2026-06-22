# Config Lab: CLI Passwords 1 - Lab Solution

## Commands and Configuration

Access switch SW1 and apply the following configurations:

```cisco
enable
configure terminal
enable secret kindness

line con 0
password joy
login
exit

line vty 0 4
password peace
login
end
```

## Explanation

- The `enable secret kindness` command sets the encrypted privileged mode password. This is more secure than `enable password` because it uses MD5 hashing.
- The `line con 0` block configures the console line with password "joy" and requires login authentication.
- The `line vty 0 4` block configures the first five virtual terminal lines for Telnet access with password "peace" and requires login authentication.
- No username database is required because `login` (without `local`) uses the line password for authentication.

## Verification

```cisco
show running-config | section line
```

Expected output should show:
- `enable secret 5` followed by the hashed password
- Console line with `password joy` and `login`
- VTY lines 0-4 with `password peace` and `login`

Test console access by exiting to user mode and re-entering privileged mode.
Test Telnet from PC1 with: `telnet 10.1.1.20`
