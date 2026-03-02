# 🔍 WinForensics

A comprehensive Windows forensic artifacts reference — built for investigators, incident responders, and security analysts who need fast, reliable answers during live investigations.

**Live site:** `https://yourusername.github.io/winforensics`

---

## 📦 What's Inside

| File | Description |
|------|-------------|
| `windows-artifacts.html` | Main cheat sheet — 117 artifacts, 20 categories |

### Coming Soon
- `attack-chain.html` — Kill chain phase → artifact mapping
- `memory-forensics.html` — Full Volatility 3 reference
- `ad-deepdive.html` — Active Directory forensics deep dive

---

## 🗂️ Categories Covered

| Category | Artifacts |
|----------|-----------|
| Registry | SAM, SYSTEM, SOFTWARE, NTUSER.DAT, USRCLASS.DAT, AmCache, ShimCache |
| Event Logs | Security, System, Application, PowerShell, Sysmon, Defender, Task Scheduler |
| File System | Prefetch, LNK, Jump Lists, Shellbags, MFT, UsnJrnl, Recycle Bin, VSS |
| Browser | Chrome, Edge, Firefox, Internet Explorer |
| Browser Deep Dive | IndexedDB, Extensions, Incognito, Cache, Passwords, Sessions, Cookies |
| Network | Network Profiles, RDP, DNS Cache, Firewall Logs, ARP Cache |
| Execution | UserAssist, BAM/DAM, SRUM, Run Keys, CapabilityAccessManager |
| Memory | hiberfil.sys, Pagefile, Crash Dumps |
| User Activity | RecentDocs, TypedURLs, Timeline, Sticky Notes, Thumbcache |
| USB & Devices | USB History, setupapi.dev.log |
| Persistence | Scheduled Tasks, Services, WMI Subscriptions, Bootkits, DLL Hijacking |
| Cloud & Sync | OneDrive, Dropbox, Google Drive |
| Registry MRU | OpenSaveMRU, LastVisitedMRU, RunMRU, WordWheelQuery, Office MRU |
| LOLBAS | certutil, mshta, rundll32, wscript, regsvr32, bitsadmin, msiexec, wmic |
| Credentials | LSASS, Credential Manager, DPAPI, SAM+SYSTEM, Kerberos, WiFi |
| Anti-Forensics | CCleaner, BitLocker, cipher.exe, SDelete, VSS Deletion, Log Manipulation |
| Lateral Movement | PsExec, SMB Shares, WinRM, DCOM |
| Email | Outlook PST/OST, Attachment Cache |
| Active Directory | NTDS.dit, DCSync, GPO Artifacts |
| Misc | Notepad++, Windows Search, Windows Recall/Copilot |

---

## ✨ Features

- **117 artifacts** across **20 categories**
- **Live search** across all fields — paths, notes, event IDs, tools, commands
- **Category filter** tabs for instant filtering
- **428 exact commands** — one click to copy any command or path
- **Forensic value rating** — CRITICAL / HIGH / MEDIUM / LOW per artifact
- **Event ID references** per artifact
- **OS version coverage** per artifact
- **Fully offline** — no external dependencies, works without internet
- **Mobile friendly** — works on phone during live investigations

---

## 🚀 How to Use Locally

Just open `windows-artifacts.html` in any browser. No server needed, no install, no dependencies.

```bash
git clone https://github.com/yourusername/winforensics
cd winforensics
open windows-artifacts.html   # macOS
start windows-artifacts.html  # Windows
```

---

## 📱 Mobile Use

Fully optimized for mobile. Pull it up on your phone mid-investigation to quickly check artifact paths, event IDs, or copy commands.

---

## 🛠️ Tools Referenced

This reference covers artifacts analyzed by tools including:

`Autopsy` `Volatility` `RegRipper` `Chainsaw` `Hayabusa` `Hindsight` `MFTECmd` `PECmd` `LECmd` `JLECmd` `AmcacheParser` `AppCompatCacheParser` `WxTCmd` `RBCmd` `SrumECmd` `Registry Explorer` `ShellBagsExplorer` `DB Browser for SQLite` `FTK Imager` `Velociraptor` `Plaso` `log2timeline` `Impacket` `Mimikatz`

---

## 📌 Quick Reference — Most Important Event IDs

| Event ID | Log | Meaning |
|----------|-----|---------|
| 4624 | Security | Successful logon |
| 4625 | Security | Failed logon |
| 4688 | Security | Process creation (with command line) |
| 4698 | Security | Scheduled task created |
| 4719 | Security | Audit policy changed |
| 7045 | System | New service installed |
| 1102 | Security | Security log cleared |
| 104 | System | System log cleared |
| 5140 | Security | Network share accessed |
| 4662 | Security | AD object accessed (DCSync detection) |
| 1 | Sysmon | Process creation |
| 3 | Sysmon | Network connection |
| 7 | Sysmon | Image/DLL loaded |
| 10 | Sysmon | Process accessed (LSASS dump detection) |

---

## ⚠️ Disclaimer

This reference is intended for **authorized forensic investigations, incident response, and security research only**. All information is provided for defensive and educational purposes.

---

*Built for the forensics community — contributions welcome.*
