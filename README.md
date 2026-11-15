<div align="center">

# Anti-Block Toolkit — Local Windows DPI & DNS Bypass

[![Support Project](https://img.shields.io/badge/SUPPORT%20PROJECT-DONATE%20BNB%20%2F%20USDT-F3BA2F?style=for-the-badge&logo=binance&logoColor=white)](https://phoenixisgame.github.io/AntiBlockToolkit/)
[![Version](https://img.shields.io/badge/VERSION-V1.0-FFD700?style=for-the-badge)](https://github.com/phoenixisgame/AntiBlockToolkit/releases)
[![Platform](https://img.shields.io/badge/PLATFORM-WINDOWS%2010%20%2F%2011-0078D6?style=for-the-badge&logo=windows&logoColor=white)](#)

</div>

---

### ⚙️ Quick Installation / طريقة التشغيل السريعة:

> **English:** Download **`AntiBlockToolkit.exe`** from [Releases](https://github.com/phoenixisgame/AntiBlockToolkit/releases), right-click and **Run as administrator**, then click **ENABLE SHIELD**.  
> **العربية:** حمّل ملف **`AntiBlockToolkit.exe`** من [قسم الإصدارات](https://github.com/phoenixisgame/AntiBlockToolkit/releases)، انقر عليه بالزر الأيمن واختر **تشغيل كمسؤول (Run as administrator)**، ثم اضغط على **ENABLE SHIELD**.

---

## 🇬🇧 English Description

Hey everyone! 🛡️⚡

I'm excited to release **Version 1.0** of **Anti-Block Toolkit**, a fast, lightweight, 100% local Windows anti-censorship utility engineered to bypass Deep Packet Inspection (DPI) and ISP DNS blocks with **zero ping penalty**!

### 🔥 Key Features & Capabilities:

* 🔒 **Built-in Local DoH Engine (`127.0.0.1:53`):** Intercepts standard UDP/TCP DNS queries locally and resolves them securely via DNS-over-HTTPS (Cloudflare, Google, Quad9, AdGuard) with multi-IP bootstrapping to defeat ISP DNS hijacking.
* ⚡ **TLS ClientHello Fragmentation (`127.0.0.1:8881`):** Splits the outgoing TLS 1.2 / 1.3 `ClientHello` record across TCP segments with microsecond pacing so DPI middleboxes fail to inspect the Server Name Indication (SNI) or inject `TCP RST` drops.
* 🎮 **Zero Ping Overhead for Gaming:** Unlike traditional VPNs that add `+50ms` to `+150ms` of latency, everything runs strictly on Windows loopback (`127.0.0.1`), preserving native speeds and `0%` packet loss (verified on **Counter-Strike 2** and **Street Fighter 6**).
* 🛡️ **Safe Auto-Rollback & Recovery:** Captures immutable backups of your active network adapter's DNS and WinINET proxy state before activation, automatically restoring clean system defaults on exit—plus a companion `emergency_restore.bat` script.
* 📊 **Live Diagnostic Console:** Real-time telemetry tracking encrypted domain resolutions, active fragmented TLS tunnels, and connection diagnostics.

The goal is to provide gamers and everyday users with unrestricted, full-speed internet access without relying on paid VPNs, external VPS relays, or virtual network drivers.

* **Tool:** Anti-Block Toolkit
* **Version:** v1.0
* **Platform:** Windows 10 / 11 (64-bit)
* **Creator:** phoenixisgame

---

## 🇸🇦 النسخة العربية

أهلاً بالجميع! 🛡️⚡

يسعدني مشاركة **الإصدار 1.0** من أداة **Anti-Block Toolkit**، وهي أداة خفيفة وسريعة تعمل **محلياً بنسبة 100%** على نظام ويندوز لتجاوز حجب المواقع والألعاب الناتج عن الفحص العميق للحزم (**DPI**) وتسميم الـ **DNS** من مزودي الخدمة، وذلك **بدون أي ارتفاع في البينغ (Zero Ping Penalty)**!

### 🔥 أبرز المميزات والخصائص:

* 🔒 **محرك DoH محلي مدمج (`127.0.0.1:53`):** يلتقط استعلامات DNS محلياً ويشفرها عبر HTTPS (Cloudflare, Google, Quad9, AdGuard) لمنع التلاعب بالـ DNS أو حظر النطاقات.
* ⚡ **تجزئة حزم TLS ClientHello (`127.0.0.1:8881`):** تقسيم حزمة البداية (SNI) بدقة عبر أجزاء TCP لمنع أنظمة الفحص العميق (DPI) من قراءة اسم الموقع وقطع الاتصال.
* 🎮 **أداء مثالي للألعاب بدون أي تأخير (Zero Ping Penalty):** على عكس برامج VPN التي ترفع البينغ، تعمل الأداة محلياً بالكامل على جهازك وتحافظ على مسار اتصالك المباشر (`0%` فقدان حزم).
* 🛡️ **أمان تام واسترجاع تلقائي (Auto-Rollback):** تأخذ نسخة احتياطية لإعدادات الشبكة قبل التشغيل وتعيدها تلقائياً عند الإغلاق، مع توفير ملف `emergency_restore.bat` للطوارئ.
* 📊 **سجل مراقبة مباشر:** عرض حي لعمليات تشفير DNS والاتصالات المجزأة وتشخيص الشبكة في الوقت الفعلي.

* **الأداة:** Anti-Block Toolkit
* **الإصدار:** v1.0
* **النظام:** Windows 10 / 11 (64-bit)
* **المطور:** phoenixisgame

---

## ☕ Support the Project / دعم المشروع

Anti-Block Toolkit is 100% free. Your voluntary support helps maintain and develop future updates!  
المشروع مجاني بالكامل، ومساهمتك الطوعية تساعد في استمرار صيانته وتطوير إصدارات قادمة.

* **Network / الشبكة:** BNB Smart Chain (BEP20)
* **Accepted / العملات:** USDT / BNB (Min: 1.00 USDT)
* **Wallet Address (RedotPay / Crypto) / عنوان المحفظة:**
```text
0x2F8D26b67d8be078A2BE40c1887379232746fD79
```

<div align="center">

<img src="qr.png" width="160" alt="Support QR Code" /><br/>
<sub>Scan with RedotPay / Binance to support development</sub>

<br/><br/>

**Anti-Block Toolkit — Freedom to Connect. Freedom to Play.**  
**حرية الاتصال، وحرية اللعب.**

</div>
