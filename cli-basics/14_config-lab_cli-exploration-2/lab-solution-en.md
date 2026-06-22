# Config Lab: CLI Exploration 2 - Lab Solution

## Commands and Configuration

This lab focuses on practicing Cisco IOS CLI navigation, editing, and help commands. Use the following commands to explore the CLI efficiently:

### Navigation Commands

```cisco
enable                    ! Enter privileged EXEC mode
configure terminal        ! Enter global configuration mode
interface gigabitethernet0/0  ! Enter interface configuration mode
end                       ! Return to privileged EXEC mode from any config mode
exit                      ! Move up one level in the command hierarchy
disable                   ! Return to user EXEC mode
```

### Help and Editing Commands

```cisco
?                         ! Display available commands at the current mode
show ?                    ! Display available options for the show command
configure ?               ! Display available options for configure

! Command abbreviation and tab completion
conf t                    ! Abbreviation for configure terminal
int g0/0                  ! Abbreviation for interface gigabitethernet0/0

! Error recovery
no <command>              ! Remove a previously configured command
default <command>         ! Restore a command to its default value
```

### Show Commands for Exploration

```cisco
show version              ! Display IOS version and hardware information
show running-config       ! Display current active configuration
show startup-config       ! Display saved startup configuration
show interfaces           ! Display interface status and statistics
show ip interface brief   ! Summarize interface IP status
show history              ! Display command history
```

### Keyboard Shortcuts

| Shortcut | Function |
|----------|----------|
| Tab | Auto-complete command |
| Ctrl+A | Move cursor to beginning of line |
| Ctrl+E | Move cursor to end of line |
| Ctrl+U | Clear entire line |
| Ctrl+W | Delete previous word |
| Up Arrow | Recall previous command |
| Down Arrow | Recall next command |

## Verification

Practice moving between configuration modes and verify your prompt changes:
- User mode: `Router>`
- Privileged mode: `Router#`
- Global config: `Router(config)#`
- Interface config: `Router(config-if)#`

Use `do show running-config` from configuration mode to verify configuration changes without exiting.
