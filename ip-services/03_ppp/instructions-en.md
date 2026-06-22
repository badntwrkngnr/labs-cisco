# PPP Configuration

## Objectives

Configure Point-to-Point Protocol (PPP) encapsulation on serial links and understand its advantages over HDLC.

## Instructions

1. Change the serial interface encapsulation from HDLC to PPP.
2. Verify that both sides of the link use PPP.
3. Configure IP addresses if not already set.
4. Verify Layer 2 connectivity with PPP.

## Verification

- Use `show interfaces serial` to verify PPP encapsulation.
- Use `debug ppp negotiation` to observe PPP negotiation (use with caution).
- Use `ping` to test end-to-end connectivity.
