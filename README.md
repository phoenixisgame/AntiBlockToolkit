# Anti-Block Toolkit 🛡️

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%2F%2011-0078D6.svg)](https://microsoft.com)
[![Python](https://img.shields.io/badge/Python-3.10%2B-brightgreen.svg)](https://python.org)
[![Zero Ping Overhead](https://img.shields.io/badge/Gaming-Zero%20Ping%20Penalty-success.svg)](#gaming-performance)

**Anti-Block Toolkit** is a lightweight, high-performance, local Windows utility designed to bypass Deep Packet Inspection (DPI) and DNS censorship without external VPS proxies, paid VPN subscriptions, or third-party TUN/TAP network drivers.

Everything runs **100% locally on your PC**, preserving your native internet speed and lowest in-game latency (0% packet loss).

---

## 🚀 Key Highlights

* **🔒 Local Dual-Stack DoH Engine (`127.0.0.1:53`):**
  Intercepts standard RFC 1035 UDP/TCP DNS queries and securely resolves them via RFC 8484 DNS over HTTPS (Cloudflare, Google, Quad9, AdGuard) with multi-IP bootstrapping to defeat ISP DNS hijacking.
* **⚡ TLS ClientHello Fragmentation Proxy (`127.0.0.1:8881`):**
  Performs precision Application Write Splitting inside the TLS 1.2 / 1.3 ClientHello record. By dividing the Server Name Indication (SNI) across multiple TCP segments with microsecond delays, DPI middleboxes fail to identify target hosts, preventing connection resets (`TCP RST`) and silent packet drops.
* **🎮 Gaming & Competitive Latency Optimized:**
  Unlike conventional VPNs that route all traffic through distant relay servers (adding +50ms to +150ms of ping), Anti-Block Toolkit operates strictly on loopback. Verified on **Counter-Strike 2** (maintaining `54ms` and `0% loss` to Vienna Valve SDR) and **Street Fighter 6** (bypassing CFN error `50100-20011` with full ranked multiplayer access).
* **🛡️ Zero-Residual Safety & Automatic Rollback:**
  Captures documented immutable backups of your original primary network adapter DNS and WinINET registry configurations before modifying system state. If any component fails verification, an automatic reverse-order rollback restores pristine system settings instantly.
* **📊 Live Diagnostic Traffic & Latency Logger:**
  Real-time inspection console tracking domain resolutions, active TLS tunnels, fragmented byte streams, and connection error diagnoses.

---

## 🖥️ Architecture Overview

```text
  +-------------------------------------------------------------------------+
  |                           USER PC (WINDOWS)                             |
  |                                                                         |
  |  [ Game / Browser ]                                                     |
  |          |                                                              |
  |          +---> (DNS: 127.0.0.1:53) -----> [ Local DoH Engine ]          |
  |          |                                      | (RFC 8484 HTTPS)      |
  |          |                                      v                       |
  |          |                              [ Cloudflare / Google ]         |
  |          |                                                              |
  |          +---> (HTTP/S: 127.0.0.1:8881) -> [ TLS Splitting Proxy ]     |
  |                                                 | (TCP Split SNI)       |
  |                                                 v                       |
  |                                            [ Target Game / Web Server ] |
  +-------------------------------------------------------------------------+
                                      |
                     (Bypasses ISP Deep Packet Inspection)
```

---

## 📦 Download & Quick Start

1. Download the latest standalone **`AntiBlockToolkit.exe`** from the [Releases](../../releases) tab.
2. Right-click `AntiBlockToolkit.exe` and select **Run as administrator** (required to apply local DoH to the active network adapter).
3. Click **ENABLE SHIELD**. All four status indicators will transition to green:
   - `DNS over HTTPS`: **RUNNING**
   - `TLS Proxy Engine`: **RUNNING**
   - `System Adapter DNS`: **APPLIED**
   - `WinINET System Proxy`: **APPLIED**
4. Launch your blocked game or website and enjoy unrestricted, native-speed connectivity.
5. Click **STOP SHIELD** or close the app anytime to automatically revert all system settings to their original state.

> **Emergency Recovery:** Even in the event of an abrupt power loss, the companion `emergency_restore.bat` script safely restores your original Windows network settings with a single double-click.

---

## 🛠️ Building From Source

### Prerequisites
* Windows 10 or 11 (64-bit)
* Python 3.10+
* Git

### Installation
```powershell
# Clone the repository
git clone https://github.com/phoenixisgame/AntiBlockToolkit.git
cd AntiBlockToolkit

# Install dependencies
pip install -r requirements.txt

# Run GUI in development mode
python main.py

# Compile standalone executable
python build_exe.py
```

---

## ☕ Support the Project

If **Anti-Block Toolkit** helped you overcome ISP restrictions, game connection errors, or browsing blocks, consider supporting the development:

<p align="center">
  <img src="qr.png" width="180" alt="Support QR Code" /><br/>
  <b>Scan the QR code or star ⭐ this repository to show your support!</b>
</p>

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.
