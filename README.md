# Linux Home Lab
A personal Linux home lab setup documented as part of my self-directed learning journey into IT and cybersecurity.

> **Transparency note:** This setup was built and documented with AI assistance (Claude and Gemini). I'm an IT student learning Linux from the ground up. This repo is an honest record of what I've configured, understood, and explored — not a showcase of expert-level work.

---

## System specs

| Component | Details |
|-----------|---------|
| Distro | Fedora Linux 44 Workstation |
| CPU | Intel Core i5-4690 |
| GPU | NVIDIA GeForce GTX 970 (running on open-source `nouveau` driver) |
| RAM | 16 GB |
| Primary storage | 120 GB SSD (Samsung) — Btrfs, automatic partitioning |
| Secondary storage | 1 TB HDD (Western Digital) — ext4, mounted at `/mnt/hdd` |

---

## What's configured

### Desktop environment
- **GNOME** on **Wayland** (a modern display protocol that replaces the older X11)
- **Xwayland** for legacy app compatibility (allows older apps built for X11 to run under Wayland)

### Version control & remote access
- **Git** 
- **SSH key** generated and linked to GitHub — authenticated successfully

### Storage
- Primary filesystem: **Btrfs** (a modern Linux filesystem with built-in snapshot support)
- Secondary HDD mounted permanently via `/etc/fstab` using UUID

### Security & networking
- **firewalld** active (zone: FedoraWorkstation — services allowed: SSH, dhcpv6-client, samba-client)
- **Wireshark** installed and configured — user added to `wireshark` group for non-root capture
- **Quad9 DNS** configured via NetworkManager — privacy-focused, no logging, malware blocking

### Performance
- **RPM Fusion** (free + nonfree) enabled — multimedia codecs installed (gstreamer, ffmpeg)
- **CPU governor** set to `performance` via kernel-tools
- **Boot time** optimized (~20s): `NetworkManager-wait-online` disabled, Plymouth set to details mode

### Media
- **Strawberry Music Player** installed via RPM (not Flatpak), pointing to local music library on HDD

### Other
- Browser: Firefox with uBlock Origin

---

## In progress

- [x] Run initial system update (`sudo dnf upgrade`)
- [x] Configure firewall (`firewalld` — native Fedora)
- [x] Set up privacy-focused DNS (Quad9)
- [x] Install Wireshark
- [ ] Log analysis workflow
- [ ] Explore TryHackMe for hands-on cybersecurity practice

---

## Known hardware notes

- **NVIDIA GTX 970 (GM204, PCI ID 10de:13c2):** proprietary driver 595.80 does not support this GPU on Fedora 44. Driver branch 470xx initializes correctly but is incompatible with GDM. System runs stably on `nouveau` open-source driver.

---

## Learning context

I'm 37, working at a public library in Patagonia, Argentina, and teaching myself IT systems independently after leaving a university program. My current focus is Linux system administration and cybersecurity.

This repo is part of a broader portfolio being built alongside the **Google Cybersecurity Professional Certificate** on Coursera.

Tools and resources I'm using:
- [Fedora Linux](https://fedoraproject.org/)
- [Quad9 DNS](https://www.quad9.net/)
- [TryHackMe](https://tryhackme.com/) *(planned)*
