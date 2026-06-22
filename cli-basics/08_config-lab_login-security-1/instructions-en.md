# Login Security

## Objectives

Implement enhanced login security features including login banners, timeouts, and enhanced password policies on Cisco devices.

## Instructions

1. Configure a login banner with a security warning message.
2. Set exec-timeout values on console and VTY lines.
3. Enable synchronous logging to prevent command interruption.
4. Configure enhanced password policies if supported.
5. Verify all login security settings are active.

## Verification

- Use `show running-config | section line` to verify line settings.
- Log out and back in to test the banner and timeout behavior.
