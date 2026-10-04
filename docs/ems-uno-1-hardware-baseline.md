# ems-uno-1 Hardware Baseline

## Identity

- Manufacturer: Advantech
- Product: UNO-2372G-J121AU
- Serial number: TPAD240958
- SMBIOS model: UNO-2372G-J121AE
- BIOS: AMI 112
- BIOS date: 2020-09-07
- Boot mode: UEFI
- CSM: Disabled
- Secure Boot: Disabled

## CPU and Memory

- CPU: Intel Celeron J3455
- Cores: 4
- Threads: 4
- Frequency range: 800–2300 MHz
- Intel VT-x: Enabled
- RAM: 8 GB DDR3L

## Storage

- SSD: Advantech SQF-S25V2-128GCSBC
- Capacity: 128 GB
- SATA: 6.0 Gb/s
- SMART overall health: PASSED
- Percentage used endurance: 0%
- Interface CRC errors: 0

## Ethernet

### LAN A

- Linux interface: enp2s0
- MAC: C4:00:AD:E0:3B:3E
- Controller: Intel I210
- Driver: igb
- Link: 1 Gbit/s Full Duplex
- Primary management interface

### LAN B

- Linux interface: enp1s0
- MAC: C4:00:AD:E0:3B:3D
- Controller: Intel I210
- Driver: igb

## Serial Ports

All four physical ports are configured in BIOS for RS-485 mode.

- COM1 -> /dev/ttyS0, I/O 0x3f8, IRQ4
- COM2 -> /dev/ttyS1, I/O 0x2f8, IRQ3
- COM3 -> /dev/ttyS2, I/O 0x3e8, IRQ5
- COM4 -> /dev/ttyS3, I/O 0x2e8, IRQ7

Linux detects all four UARTs as 16550A.

## RTC and Time

- RTC device: /dev/rtc0
- Time zone: Europe/Kyiv
- RTC stored in UTC
- NTP synchronization: active
- Cold power RTC retention: PASS
- BIOS VBAT observed around 2.5 V; battery condition remains an acceptance warning.

## TPM

- TPM 2.0
- Vendor: Infineon
- Linux devices:
  - /dev/tpm0
  - /dev/tpmrm0

## Watchdog

- Linux driver: wdat_wdt
- Device: /dev/watchdog0
- Default timeout: 30 s
- Minimum timeout: 2 s
- Maximum timeout: 613 s
- nowayout: 0
- systemd RuntimeWatchdogSec: disabled
- Functional timeout/reboot test not yet performed.

## Power Recovery

- Hardware SW1 configured for AT mode.
- Automatic boot after DC power restoration: PASS.
- Tailscale and SSH recovery after reboot: PASS.

## Operating System

- Debian GNU/Linux 13.7 (trixie)
- Architecture: amd64
- Kernel: 6.12.111+deb13-amd64
- Hostname: ems-uno-1
- Tailscale IP: 100.88.208.94

## Runtime

- Docker Engine: 29.8.2
- Docker Compose: v5.6.0
- Docker service: enabled and active
- User ems-admin has docker and dialout access.
