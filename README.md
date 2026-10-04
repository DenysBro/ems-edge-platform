# EMS Edge Platform

Provisioning, hardware acceptance, operating system configuration, and runtime host setup for industrial EMS edge controllers.

## Reference platform

- Controller: Advantech UNO-2372G-J121AU
- Architecture: x86_64 / amd64
- Operating system: Debian 13 (trixie)
- Hostname: ems-uno-1
- Runtime: Docker Engine
- Remote access: SSH + Tailscale

## Scope

- Hardware acceptance
- Debian provisioning
- Network configuration
- Persistent Ethernet naming
- RS-485 serial configuration
- RTC and time synchronization
- TPM
- Hardware watchdog
- Docker host configuration
- Development/runtime tooling
- Host acceptance and recovery tests

EMS application code is maintained separately from this platform repository.
