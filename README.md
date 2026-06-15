# Linux Home Lab

A personal Linux home lab setup documented as part of my self-directed learning journey into IT and cybersecurity.

> **Transparency note:** This setup was built and documented with AI assistance (Claude by Anthropic). I'm an IT student learning Linux from the ground up. This repo is an honest record of what I've configured, understood, and explored — not a showcase of expert-level work.

---

## System specs

| Component | Details |
|-----------|---------|
| Distro | Fedora Linux 44 Workstation |
| CPU | Intel Core i5-4690 |
| GPU | NVIDIA GeForce GTX 970 |
| RAM | 16 GB |
| Primary storage | 120 GB SSD (Samsung) — Btrfs, automatic partitioning |
| Secondary storage | 1 TB HDD (Western Digital) — ext4, mounted at `/mnt/HDD` |

---

## What's configured

### Desktop environment
- **GNOME** on **Wayland** (a modern display protocol that replaces the older X11)
- **Xwayland** for legacy app compatibility (allows older apps built for X11 to run under Wayland)

### Version control & remote access
- **Git** configured with ProtonMail identity
- **SSH key** (ED25519) generated and linked to GitHub — authenticated successfully

### Storage
- Primary filesystem: **Btrfs** (a modern Linux filesystem with built-in snapshot support)
- Secondary HDD mounted permanently via `/etc/fstab` using UUID

### Media
- **Strawberry Music Player** installed via RPM (not Flatpak), pointing to local music library on HDD

### Other
- Browser: Firefox with uBlock Origin

---

## In progress

- [ ] Run initial system update (`sudo dnf upgrade`)
- [ ] Configure security tooling (UFW, Wireshark, log analysis)
- [ ] Set up privacy-focused DNS (Quad9)
- [ ] Explore TryHackMe for hands-on cybersecurity practice

---

## Learning context

I'm 37, working at a public library in Patagonia, Argentina, and teaching myself IT systems independently after leaving a university program. My current focus is Linux system administration and cybersecurity.

This repo is part of a broader portfolio being built alongside the **Google Cybersecurity Professional Certificate** on Coursera.

Tools and resources I'm using:
- [Fedora Linux](https://fedoraproject.org/)
- [Quad9 DNS](https://www.quad9.net/) *(planned)*
- [TryHackMe](https://tryhackme.com/) *(planned)*
