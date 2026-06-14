# NiksonOS

**Built for Hackers, Designed for Power**

NiksonOS is a Debian 13 (Trixie) based Linux distribution purpose-built for penetration testing, security research, network analysis, and OSINT work. It ships with a curated set of custom tools alongside industry-standard security utilities, wrapped in a fast, distraction-free XFCE desktop.

---

## Overview

| | |
|---|---|
| **Version** | 1.0 "Genesis" |
| **Base** | Debian 13 (Trixie) |
| **Desktop Environment** | XFCE 4.20 |
| **Architectures** | ARM64 (aarch64), AMD64 (x86_64) |
| **Installer** | Calamares (GUI) |
| **Theme** | Arc-Dark + Papirus-Dark icons |
| **Default Shell** | Bash |

---

## Features

- **Custom Nikson Toolkit** — a suite of purpose-built tools for monitoring, reconnaissance, password management, and more (see below).
- **Curated security tools** — nmap, Wireshark, tcpdump, Aircrack-ng, Hashcat, John the Ripper, SQLmap, Nikto, Hydra, and more, preinstalled and ready to use.
- **Custom branding** — boot splash (Plymouth), login screen, desktop wallpapers, and a fastfetch system info screen, all themed around the NiksonOS identity.
- **Organized application menu** — all Nikson tools and security utilities grouped under a dedicated "Nikson Tools" category for quick access.
- **Calamares graphical installer** — install NiksonOS to your hard drive directly from the live desktop with a guided, user-friendly installer.
- **Privacy-conscious defaults** — Tor and MAC address spoofing tools included for users who need them.
- **Live + persistent options** — boot into a live session to try before you install.

---

## The Nikson Toolkit

NiksonOS includes a set of custom command-line tools, all prefixed `nikson-` and available from any terminal:

| Tool | Description |
|---|---|
| `nikson-center` | Central hub and dashboard for managing all Nikson tools |
| `nikson-vault` | AES-256 encrypted password manager with password generation |
| `nikson-monitor` | Live network bandwidth monitor, packet sniffer, DNS monitor, ARP scanner, and port scanner |
| `nikson-sysmon` | Real-time system resource monitor (CPU, RAM, disk, network) |
| `nikson-recon` | Network reconnaissance and host discovery tool |
| `nikson-osint` | OSINT lookup tool for usernames, emails, and domains |
| `nikson-crack` | Smart hash identification and cracking utility |
| `nikson-payload` | Reverse shell and payload generator |
| `nikson-install` | One-command installer for 375+ additional security tools |
| `nikson-stealth` | Anonymity toolkit (Tor routing, MAC address randomization) |
| `nikson-ai` | AI-powered terminal assistant |

Each of these tools has an associated entry in the application menu under **Nikson Tools** for users who prefer a graphical launch point.

On first login to a terminal, NiksonOS displays a welcome banner summarizing system information and listing all available tools.

---

## Preinstalled Security Tools

In addition to the Nikson toolkit, the following industry-standard tools are included out of the box:

- **Network analysis**: nmap, Wireshark, tcpdump, netcat, net-tools, wireless-tools
- **Password attacks**: Hashcat, John the Ripper, Hydra
- **Web application testing**: SQLmap, Nikto
- **Wireless security**: Aircrack-ng
- **Privacy & anonymity**: Tor, Macchanger
- **General utilities**: vim, git, curl, wget, htop, fastfetch, Python 3

Run `nikson-install` from a terminal to browse and install from a library of 375+ additional tools.

---

## Installation

### Requirements

- A 64-bit machine (ARM64 or AMD64) with at least:
  - 2 GB RAM (4 GB recommended)
  - 20 GB free disk space
  - A bootable USB drive (8 GB or larger) or a virtual machine

### Download

Download the appropriate ISO for your hardware from the [Releases](../../releases) page:

- `NiksonOS-1.0-arm64.iso` — for ARM64 systems (Apple Silicon VMs, ARM servers, ARM-based laptops)
- `NiksonOS-1.0-amd64.iso` — for AMD64/Intel systems (most desktops, laptops, and virtual machines)

### Creating a bootable USB

**On Linux/macOS:**

```bash
sudo dd if=NiksonOS-1.0-<arch>.iso of=/dev/sdX bs=4M status=progress
sync
```

Replace `/dev/sdX` with your USB device (double-check this — using the wrong device will erase its contents).

**On Windows:**

Use [Rufus](https://rufus.ie/) or [Balena Etcher](https://etcher.balena.io/) to flash the ISO to your USB drive.

### Installing to a hard drive

1. Boot from the USB drive (or attach the ISO to a virtual machine).
2. NiksonOS will boot into a live XFCE desktop — feel free to explore before installing.
3. Double-click the **Install NiksonOS** icon on the desktop.
4. Follow the Calamares installer steps:
   - Choose your language and keyboard layout
   - Set up disk partitioning
   - Create your user account (choose a strong password — dictionary-based passwords will be rejected)
   - Review the summary and click **Install**
5. Once installation completes, reboot and remove the installation media.

---

## Default Customizations

NiksonOS comes pre-configured with:

- **Theme**: Arc-Dark GTK theme with Papirus-Dark icons
- **Font**: JetBrains Mono
- **Boot splash**: Custom Plymouth theme
- **Login screen**: Custom LightDM greeter with NiksonOS branding
- **Terminal banner**: System info and tool list shown on login via `fastfetch`
- **Wallpapers**: A set of NiksonOS-themed wallpapers included in `/usr/share/nikson-os/wallpapers/`

---

## Roadmap

- [ ] Official NiksonOS APT repository for tool updates
- [ ] Raspberry Pi image support
- [ ] Expanded `nikson-ai` capabilities
- [ ] Additional themes and wallpaper packs

---

## Disclaimer

NiksonOS bundles tools intended for security research, penetration testing, and network analysis. These tools should only be used on systems and networks you own or have explicit, written permission to test. The maintainers of NiksonOS are not responsible for any misuse of the included software.

---

## Credits

NiksonOS is built on the shoulders of the open-source community:

- **Linux Kernel** — Linus Torvalds and the Linux community
- **Debian Project** — [debian.org](https://debian.org)
- **Kali Linux** — tooling inspiration, Offensive Security
- **XFCE Desktop Environment** — [xfce.org](https://xfce.org)
- **Arc Theme** — horst3180
- **Papirus Icon Theme** — PapirusDevelopmentTeam
- **JetBrains Mono** — JetBrains
- **fastfetch** — fastfetch-cli contributors
- **Calamares Installer** — [calamares.io](https://calamares.io)

---

## License

NiksonOS itself is distributed as a collection of configurations and custom scripts. Individual bundled packages retain their own licenses as provided by Debian and their respective upstream projects.

---

**NiksonOS 1.0 "Genesis"** — Hack. Build. Explore.
