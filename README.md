<div align="center">

<img src="https://raw.githubusercontent.com/krishghosh21/NiksonOS/main/assets/logo.png" alt="NiksonOS Logo" width="180"/>

# NiksonOS

### v1.0 "Genesis"

**Built for Hackers, Designed for Power**

[![Download ISO](https://img.shields.io/badge/⬇%20Download%20ISO-Google%20Drive-blue?style=for-the-badge&logo=googledrive)](https://drive.google.com/drive/folders/1NajtwFFHTxoYmykEI8sPFAqmJwnEY48t?usp=sharing)
[![Base](https://img.shields.io/badge/Base-Debian%2013%20Trixie-red?style=for-the-badge&logo=debian)](https://debian.org)
[![Arch](https://img.shields.io/badge/Arch-ARM64%20%7C%20AMD64-green?style=for-the-badge&logo=linux)](https://github.com/krishghosh21/NiksonOS)
[![License](https://img.shields.io/badge/License-Open%20Source-orange?style=for-the-badge)](LICENSE)

---

*A purpose-built Linux distribution for penetration testers, security researchers, hardware hackers, and CTF players.*

</div>

---

## Table of Contents

- [What is NiksonOS?](#what-is-niksonos)
- [Screenshots](#screenshots)
- [System Specifications](#system-specifications)
- [Download](#download)
- [Installation](#installation)
- [The Nikson Toolkit](#the-nikson-toolkit)
- [Preinstalled Security Tools](#preinstalled-security-tools)
- [Default Customizations](#default-customizations)
- [Roadmap](#roadmap)
- [Credits](#credits)
- [Disclaimer](#disclaimer)

---

## What is NiksonOS?

NiksonOS is a custom Linux distribution built from scratch on **Debian 13 (Trixie)** for ARM64 and AMD64 architectures. It is not a remaster or reskin — it was designed and developed with a clear philosophy:

> **Install only what you need. Keep it fast. Keep it lean.**

Unlike other security distributions that ship with hundreds of pre-installed tools bloating the system, NiksonOS gives you a clean, fast XFCE desktop with a curated set of custom tools and lets you install additional tools on demand using `nikson-install` from a library of 375+ security utilities.

NiksonOS was created by **Krish Ghosh** as part of an internship project at Netrinix Academy (Track 5: AI Hacking & Security).

---

## Screenshots

> *Boot screen, desktop, terminal, and tool screenshots coming soon.*

---

## System Specifications

| Field | Value |
|---|---|
| **OS Name** | NiksonOS |
| **Version** | 1.0 "Genesis" |
| **Base** | Debian 13 (Trixie) |
| **Kernel** | Linux 6.12.x (deb13) |
| **Architectures** | ARM64 (aarch64), AMD64 (x86_64) |
| **Desktop Environment** | XFCE 4.20 |
| **Display Manager** | LightDM |
| **GTK Theme** | Arc-Dark |
| **Icon Theme** | Papirus-Dark |
| **Font** | JetBrains Mono |
| **Default Shell** | Bash |
| **Installer** | Calamares (GUI) |
| **ISO Size** | ~1.8 GB (ARM64) |
| **Idle RAM Usage** | ~530 MB |

---

## Download

> ISO files are hosted on Google Drive due to GitHub's file size limits.

<div align="center">

[![Download NiksonOS ISO](https://img.shields.io/badge/⬇%20Download%20NiksonOS%20ISO-Google%20Drive-blue?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/drive/folders/1NajtwFFHTxoYmykEI8sPFAqmJwnEY48t?usp=sharing)

</div>

| File | Architecture | Description |
|---|---|---|
| `NiksonOS-1.0-arm64.iso` | ARM64 | For Apple Silicon (M1/M2/M3/M4) VMs, ARM servers |
| `NiksonOS-1.0-amd64.iso` | AMD64 | For Intel/AMD desktops, laptops, and VMs |

---

## Installation

### Minimum Requirements

| Component | Minimum | Recommended |
|---|---|---|
| RAM | 2 GB | 4 GB |
| Disk Space | 20 GB | 40 GB |
| USB Drive | 4 GB | 8 GB |
| CPU | 64-bit (ARM64 or AMD64) | Dual-core or better |

---

### Step 1 — Create a Bootable USB

**On Linux / macOS:**

```bash
sudo dd if=NiksonOS-1.0-<arch>.iso of=/dev/sdX bs=4M status=progress
sync
```

> ⚠️ Replace `/dev/sdX` with your actual USB device path. Double-check using `lsblk` — wrong device will erase its contents.

**On Windows:**

Use [Rufus](https://rufus.ie/) or [Balena Etcher](https://etcher.balena.io/) to flash the ISO.

---

### Step 2 — Boot from USB (or attach ISO to VM)

- For physical hardware: Boot from USB via BIOS/UEFI boot menu.
- For VMware / VirtualBox: Attach the ISO as a CD-ROM drive and boot.

---

### Step 3 — Try the Live Session

NiksonOS boots into a **live XFCE desktop**. You can explore the OS, run tools, and test your hardware compatibility before committing to installation.

---

### Step 4 — Install NiksonOS

1. Double-click the **Install NiksonOS** icon on the live desktop.
2. The **Calamares GUI installer** will launch.
3. Follow the guided steps:
   - Select language and keyboard layout
   - Configure disk partitioning (auto or manual)
   - Create your user account
   - Review the installation summary
   - Click **Install**
4. Once complete, reboot and remove the installation media.

---

## The Nikson Toolkit

NiksonOS ships with a suite of **12 custom-built tools**, all available as `nikson-*` commands from any terminal and accessible from the application menu under **Nikson Tools**.

| Tool | Description |
|---|---|
| `nikson-center` | Central hub and GUI dashboard for managing all Nikson tools |
| `nikson-recon` | Advanced automated reconnaissance — nmap, whois, DNS, Shodan, ffuf, WAF detection, GeoIP |
| `nikson-osint` | OSINT lookup for usernames (20+ platforms), emails, domains, and GitHub deep scan |
| `nikson-sysmon` | Real-time system monitor — CPU, RAM, disk, network speed, temperature, top processes |
| `nikson-monitor` | Live network traffic monitor — bandwidth, packet sniffer, DNS monitor, ARP scanner |
| `nikson-crack` | Smart hash cracker — auto-detects hash type, wraps hashcat and John the Ripper |
| `nikson-payload` | Reverse shell and payload generator for bash, python, php, ruby, perl, and netcat |
| `nikson-vault` | AES-256 encrypted password manager with password generation |
| `nikson-stealth` | Anonymity toolkit — Tor routing, MAC address spoofing, hostname spoofing, log cleaning |
| `nikson-ai` | AI-powered terminal assistant with cybersecurity context (requires Ollama) |
| `nikson-install` | Interactive installer for 375+ additional security tools across 8 categories |
| `nikson-menu-update` | Auto-updates the security application menu when new tools are installed |

### nikson-stealth — Anonymous Mode

`nikson-stealth` provides a full anonymity mode by combining:

- **Tor routing** — routes all TCP traffic through the Tor network
- **MAC address spoofing** — randomizes your MAC address using macchanger
- **Auto rotation** — automatically rotates Tor IP and MAC address at set intervals
- **Hostname spoofing** — generates a random hostname
- **Log cleaning** — wipes system logs, bash history, temp files, and login records
- **DNS securing** — routes DNS through Tor

Stopping stealth mode automatically restores everything to normal.

### nikson-install — 375+ Tools on Demand

Run `nikson-install` to browse and install from a library of 375+ security tools organized into 8 categories:

```
1. Information Gathering    (30+ tools)
2. Web Application Testing  (20+ tools)
3. Password Attacks         (15+ tools)
4. Wireless Attacks         (12+ tools)
5. Exploitation             (10+ tools)
6. Reverse Engineering      (11+ tools)
7. Forensics                (12+ tools)
8. Sniffing & Spoofing      (9+ tools)
```

When you install any tool via `apt install`, a dpkg hook automatically detects the tool's category and adds it to the correct security menu section — no manual configuration needed.

---

## Preinstalled Security Tools

In addition to the Nikson toolkit, these industry-standard tools are included out of the box:

**Network Analysis**
- nmap, Wireshark, tcpdump, netcat, net-tools, wireless-tools

**Password Attacks**
- Hashcat, John the Ripper, Hydra

**Web Application Testing**
- SQLmap, Nikto

**Wireless Security**
- Aircrack-ng

**Privacy & Anonymity**
- Tor, Macchanger

**General Utilities**
- vim, git, curl, wget, htop, fastfetch, Python 3, Docker

**System Security**
- UFW (firewall), Fail2Ban, AppArmor

---

## Default Customizations

NiksonOS comes pre-configured with a consistent hacker-themed aesthetic:

| Setting | Value |
|---|---|
| GTK Theme | Arc-Dark |
| Icon Theme | Papirus-Dark |
| Font | JetBrains Mono |
| Boot Splash | Custom Plymouth theme |
| Login Screen | Custom LightDM greeter with NiksonOS branding |
| Terminal Banner | System info + tool list on every terminal open |
| Wallpapers | 5 custom NiksonOS wallpapers in `/usr/share/nikson-os/wallpapers/` |
| Security Menu | Kali-style categorized menu under "Nikson Security" |

The terminal welcome banner displays:
- A large NiksonOS ASCII banner in a randomly selected color
- Hostname, date, IP address, kernel version, and uptime
- A full list of available Nikson tools with descriptions

---

## Security Hardening

NiksonOS ships with security hardening enabled by default:

- **UFW** — firewall active, denying all incoming connections by default
- **Fail2Ban** — active, banning IPs with excessive failed login attempts
- **AppArmor** — mandatory access control enabled and enforced

---

## Roadmap

- [ ] Official NiksonOS APT repository (`repo.niksonos.dev`)
- [ ] AMD64 ISO release
- [ ] Raspberry Pi image
- [ ] Calamares installer full branding
- [ ] Expanded `nikson-ai` with local model support
- [ ] NiksonOS website (`niksonos.dev`)
- [ ] Additional wallpaper packs and themes
- [ ] v2.0 — ESP32/NRF24 hardware hacking toolkit
- [ ] v2.0 — RTL-SDR software defined radio toolkit
- [ ] v2.0 — Custom kernel optimizations

---

## Credits

NiksonOS is built on the shoulders of the open-source community:

| Project | Credit |
|---|---|
| **Linux Kernel** | Linus Torvalds and the Linux community |
| **Debian Project** | [debian.org](https://debian.org) |
| **Kali Linux** | Tooling inspiration — Offensive Security |
| **XFCE Desktop** | [xfce.org](https://xfce.org) |
| **Arc Theme** | horst3180 |
| **Papirus Icons** | PapirusDevelopmentTeam |
| **JetBrains Mono** | JetBrains |
| **fastfetch** | fastfetch-cli contributors |
| **Calamares** | [calamares.io](https://calamares.io) |
| **Tor Project** | [torproject.org](https://torproject.org) |

**Created by:** Krish Ghosh 

---

## Disclaimer

NiksonOS bundles tools intended for security research, penetration testing, and network analysis. These tools must only be used on systems and networks you own or have **explicit, written permission** to test.

The maintainers of NiksonOS are not responsible for any misuse of the included software. Use responsibly and ethically.

---

## License

NiksonOS configurations and custom scripts are open source. Individual bundled packages retain their own licenses as provided by Debian and their respective upstream projects.

---

<div align="center">

**NiksonOS 1.0 "Genesis"**

*Hack. Build. Explore.*

[![Download](https://img.shields.io/badge/⬇%20Download%20ISO-Google%20Drive-blue?style=for-the-badge&logo=googledrive)](https://drive.google.com/drive/folders/1NajtwFFHTxoYmykEI8sPFAqmJwnEY48t?usp=sharing)

</div>
