## Distribution

- **Distro:** Lubuntu
- **Version:** 24.04 LTS (Noble Numbat)
- **Desktop Environment:** LXQt
- **Architecture:** amd64

## Why Lubuntu 24.04

I chose the Lubuntu distro specifically because I wanted an especially lightweight Linux environment that could coexist with my main operating system in a **dual-boot setup**.

Primary constraints:
- Very limited disk-space allocation (<25 gigabytes)
- Minimal background resource usage
- Long-term stability (LTS)

Lubuntu fit better than standard Ubuntu because:
- LXQt has significantly smaller RAM footprint
- Fewer default services
- Better suited for small partitions and older hardware (although I didn't have that particular issue)

## Storage allocation strategy

**Not my primary OS** so I kept the disk footprint small.

### Partition layout
- **Root (`/`):** 20GB
- **Swap:** 4GB
No separate `/home` partition created, since this system is meant for:
- Learning linux fundamentals
- Learning the kernel in general
- Lightweight development and easy access to gcc
- Issues with programming on windows (logged later)

## Swap Size Rationale
My system already has 16GB of memory. I allocated **4GB of swap** for the following reasons:
- LXQt is lightweight but swap provides safety in-case of memory pressure
- Helps prevent system freeze in-case of package building
- Basic multitasking without a potential for OOM
- 16GB is more than enough, but better safe than sorry when experimenting for the first time
Did not configure hibernation, so swap was sized conservatively compared to RAM.

## Boot mode and firmware

- **Boot mode:** UEFI
- **Disabled secure boot to avoid issues with drivers and modules, although windows creates quite a bit of an issue with Bitlocker and new windows 11 features**
- **Bootloader:** GRUB
GRUB worked as intended during loading, allowing for a relatively seamless dual-boot process.

## Installation Notes
- Default Lubuntu installer was used
- Automatic partitioning was avoided in favour of manual size control, so as to not damage the windows 11 partition
- Network connection was seamlessly used during installation
The new install booted succesfully on the first attempt.

## Initial Observations
- Idle RAM usage after boot is very low compared to standard Ubuntu or Mint
- Desktop is extremely responsive
- Minimal preinstalled software, which aligns well with my learning goals
First order of business was to install GCC, Python3, Java, nvim and vscode.
