# NTP Client and Server

## Objectives

Configure a router as an NTP server and another as an NTP client to synchronize system clocks across the network.

## Instructions

1. Configure the NTP server router with a local clock or stratum value.
2. Configure the NTP client router to point to the NTP server.
3. Verify clock synchronization.

## Verification

- Use `show ntp status` to check synchronization status.
- Use `show ntp associations` to view peer associations.
- Use `show clock` to verify the system time.
