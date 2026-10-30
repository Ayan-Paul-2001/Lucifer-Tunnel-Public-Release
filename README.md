<div align="center">
  <img src="lucifer-favicon.svg" alt="Lucifer Tunnel Logo" width="84" height="84" />
  <h1>Lucifer Tunnel</h1>
  <p><strong>Standalone Browser VPN Extension &amp; Native Android Mobile App (.apk) with 82+ Global Countries, Dynamic IP Rotation &amp; Interactive 3D Globe</strong></p>
  <p>
    <img src="https://img.shields.io/badge/Android_App-V2.4.4-A855F7?style=flat-square" alt="App Version V2.4.4" />
    <img src="https://img.shields.io/badge/Extension-V2.4.4-2563EB?style=flat-square" alt="Extension Version V2.4.4" />
    <img src="https://img.shields.io/badge/Countries-82%2B_Verified_%7C_246_ISO-10B981?style=flat-square" alt="82+ Countries" />
    <img src="https://img.shields.io/badge/Desktop-Chrome_%7C_Edge_%7C_Brave-38BDF8?style=flat-square" alt="Supported Browsers" />
    <img src="https://img.shields.io/badge/IP_Rotation-Dynamic_Per_Connect-F59E0B?style=flat-square" alt="Dynamic IP Rotation" />
    <img src="https://img.shields.io/badge/Privacy-Zero_Logs-059669?style=flat-square" alt="Zero Logs" />
  </p>
</div>

---

**Lucifer Tunnel** is a high-performance, zero-logs VPN suite available as a **Native Android Mobile App (`.apk`)** and a **Standalone Browser Extension (`.zip`)** for Chrome, Brave, Microsoft Edge, and Opera.

Designed and engineered by **[Ayan Paul](https://ayanpaul.me)**, Lucifer Tunnel combines an interactive **3D Holographic Earth Globe & Cyber Shield** interface with **82 Official Verified Gateways**, **Dynamic Per-Connection IP Rotation**, and **Real-Time Exit-IP & Leak Verification**.

---

## Release Packages in This Repository

| Package | File | Platform | Version |
| :--- | :--- | :--- | :--- |
| **Android Mobile App** | `Lucifer-Tunnel.apk` | Android 7.0 – Latest | `V2.4.4` (Build `1062`) |
| **Browser Extension** | `Lucifer-Tunnel-Extension.zip` | Chrome, Brave, Edge, Opera (MV3) | `V2.4.4` |
| **Live OTA & Update Manifest** | `version.json` | Auto-Update & OTA Routing Sync | App `V2.4.4` / Ext `V2.4.4` |

---

## Core Features

### 1. Native Android Mobile App (`Lucifer-Tunnel.apk`)

- **System-Wide `VpnService` (`TUN0`) Protection**: Establishes a hardware-isolated Android `VpnService` tunnel with a local loopback authenticated relay (`127.0.0.1`), protecting traffic across your device.
- **Dynamic Per-Connection IP Rotation**: Every time you connect to a country, Lucifer Tunnel automatically rotates to a fresh exit IP from that country's server pool so repeated connections never reuse the same IP back-to-back.
- **Live Foreground VPN Notification**: Displays connection duration (`HH:MM:SS`) and real-time download/upload throughput (`Down: KB/s | Up: KB/s`) strictly while the VPN is connected, with a one-tap **Disconnect** action.
- **Interactive 3D WebGL Globe & Cyber Shield**: Smooth 60 FPS hardware-accelerated Three.js Earth globe with animated great-circle packet arcs and three camera modes (`3D Globe`, `3D Shield`, and `Auto-Orbit`).
- **Seamless In-Place App Updates**: Built-in **App Auto-Update** downloads and installs newer versions directly on top of your existing installation without requiring you to uninstall first.
- **Android Safety & Play Protect Verified**: Multi-scheme cryptographic signing (`v1 JAR + v2 APK Scheme + v3 Key Rotation`), strict TLS 1.3 enforcement (`usesCleartextTraffic="false"`), and zero dangerous permissions.

### 2. Standalone Browser Extension (`Lucifer-Tunnel-Extension.zip`)

- **Zero-Dependency Browser Tunnel**: Works completely standalone inside Chrome, Brave, Edge, and Opera using Manifest V3 service workers, mandatory PAC proxy routing, and automatic `Proxy-Authorization` handshakes.
- **4-Segment Compact Popup & Full-Screen 3D Dashboard**:
  - **Tunnel**: Interactive 3D globe, origin-to-exit route bar, live connection timer, and encrypted throughput counters.
  - **Countries**: Instant search across 82 Official Verified Gateways and 246 ISO countries, regional filters (`Americas`, `Europe`, `Asia Pacific`, `Middle East & Africa`), and **4K Streaming** optimization.
  - **IP & Log**: One-click **Verify IP Now** geolocation auditor (verifies active exit IP, ISP, ASN, and DNS leak protection) and filterable real-time engine logs.
  - **Settings**: Protocol selector (`Auto`, `WireGuard LinkX`, `OpenVPN UDP/TCP`), Startup Auto-Connect, LAN Bypass, and Dark/Light themes.
- **Permanent Extension ID & Built-In Auto-Update**: Uses a locked cryptographic manifest key so your Extension ID and saved preferences stay permanent across updates, paired with automatic background update detection and one-click runtime reload.

---

## How Lucifer Tunnel Works

1. **4-Step Authenticated Gateway Handshake**:
   - When you select a country and tap **Connect**, Lucifer Tunnel performs an authenticated handshake with its global cloud catalog, filters out mis-geolocated nodes, and selects a fresh server IP from the country's rotation pool.
2. **Encrypted Tunnel Establishment**:
   - **On Android**: Starts `LuciferVpnService` (`TUN0`, `10.7.1.134/32`) and binds an isolated loopback relay on `127.0.0.1` that injects ephemeral session credentials and protects outbound sockets against routing loops.
   - **On Browser Extension**: Generates a high-availability multi-node PAC routing script (`chrome.proxy.settings`) with automatic failover across up to 3 gateway nodes per country.
3. **Live Multi-Provider Exit-IP Verification**:
   - Immediately audits the active tunnel route to confirm your public exit IP, city, country, ISP, and ASN match the selected country gateway.
4. **Over-The-Air (OTA) Gateway Synchronization**:
   - Both the Mobile App and Browser Extension periodically sync with `version.json` to receive live gateway pool optimizations and version update alerts automatically.

---

## Installation & Update Guide

### A. Installing & Updating the Android Mobile App (`Lucifer-Tunnel.apk`)

1. Download **`Lucifer-Tunnel.apk`** to your Android phone.
2. Tap the downloaded `.apk` file to open the Android Package Installer and tap **Install** (or **Update** if a previous version is already installed).
3. Open **Lucifer Tunnel**, select any country from the **Countries** tab (or keep **Auto / United States**), and tap the central **Connect** button.
4. Approve the standard Android VPN connection prompt when requested on first connect.
5. **Updating to Newer Versions**:
   - Open **Settings → About → App Auto-Update** and tap **Check Update** (or **Update to V2.4.4** when available), or simply install the new `Lucifer-Tunnel.apk` directly over your current app — no uninstall required.

---

### B. Installing & Updating the Browser Extension (`Lucifer-Tunnel-Extension.zip`)

1. Download **`Lucifer-Tunnel-Extension.zip`** and extract (unzip) it to a permanent folder on your computer (for example, `Documents/Lucifer-Tunnel-Extension`).
2. Open your Chromium browser's Extensions page:
   - **Chrome**: `chrome://extensions`
   - **Brave**: `brave://extensions`
   - **Edge**: `edge://extensions`
   - **Opera**: `opera://extensions`
3. Enable **Developer mode** (toggle in the top-right corner).
4. Click **Load unpacked** and select the extracted folder (the folder containing `manifest.json`).
5. Pin **Lucifer Tunnel** to your browser toolbar, click the shield icon, and click **Connect**.
6. **Updating to Newer Versions**:
   - When a new version is released, the extension icon displays an `UPD` badge and an **Update Available** banner appears inside the popup.
   - Click **Download** (or **Settings → Check Update**), extract the downloaded `.zip` into your existing extension folder (replacing the old files), and click the **Reload** button inside Extension Settings.

---

## Privacy & Security Commitment

- **Strict Zero-Logs Policy**: Lucifer Tunnel never logs, records, or tracks your browsing history, DNS queries, or network traffic destinations.
- **Multi-User Isolation**: Every device and browser installation generates its own independent cryptographic identity and rotates across country gateway pools without interfering with other concurrent users.

---

Developed and maintained by **[Ayan Paul](https://ayanpaul.me)**.

