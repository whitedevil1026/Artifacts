# 🔍 WinForensics — Windows Forensic Artifact Reference

A comprehensive Windows forensic artifacts reference built for investigators, incident responders, and security analysts who need fast, reliable answers during live investigations.

**Live site:** https://windowsartifacts.vercel.app

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Artifacts: 137](https://img.shields.io/badge/Artifacts-137-blue)
![Categories: 21](https://img.shields.io/badge/Categories-21-blue)
![Audit Score: 8.2/10](https://img.shields.io/badge/Audit%20Score-8.2%2F10-brightgreen)

---

## 📖 About This Project

WinForensics is a single-file offline reference tool for Windows digital forensics. During a live investigation you can open it on any device — desktop, laptop, or phone — and instantly find:

- The exact registry path or file location for any artifact
- What the artifact proves forensically and when to look at it
- Which Windows versions contain it (XP through Windows 11)
- Which tools to use to parse it
- Ready-to-run commands you can copy with one click
- Correlated Windows Event IDs

No installation. No internet required. No login. Just open the HTML file in any browser.

---

## 🗂️ What's Covered — 137 Artifacts, 21 Categories

| Category | Count | What's Inside |
|---|---|---|
| 🧹 Anti-Forensics | 14 | CCleaner artifacts, BitLocker, cipher.exe /w, SDelete wipe patterns, VSS deletion evidence, event log manipulation, timestomping detection, MFT anti-forensics, renamed binary detection |
| 🗂️ File System | 11 | Prefetch, LNK shortcut files, Jump Lists, Shellbags, $MFT, $UsnJrnl/$LogFile, Recycle Bin, Volume Shadow Copies, Thumbs.db, Zone.Identifier ADS, Windows Time Rules ($SI vs $FN) |
| 🌐 Browser Deep Dive | 11 | Chrome IndexedDB, browser extensions, incognito/private mode artifacts, browser cache, saved passwords, session & tab recovery, cookies deep dive, favicons, HSTS/network state, browser sync, download history |
| 📜 Event Logs | 10 | Security log, System log, Application log, PowerShell (EID 4103/4104), Sysmon, Windows Defender, Task Scheduler, Windows Services (EID 7034/7035/7036/7040/7045) |
| 📋 Registry MRU | 10 | OpenSaveMRU, LastVisitedMRU, RunMRU, WordWheelQuery, MS Office MRU, TypedPaths, CIDSizeMRU, AppCompatFlags, XP Search ACMRU |
| 📋 Registry | 8 | SAM hive, SYSTEM hive, SOFTWARE hive, NTUSER.DAT, USRCLASS.DAT, AmCache, ShimCache, Timezone |
| 🌐 Browser | 8 | Chrome, Edge, Firefox, Internet Explorer/WebCache, IE/Edge file:// local history, Flash/Super Cookies (LSO), Google Analytics cookies, per-browser cookie breakdown |
| 🐉 LOLBAS | 8 | certutil.exe, mshta.exe, rundll32.exe, wscript/cscript, regsvr32.exe, bitsadmin/BITS, msiexec.exe, wmic.exe |
| 🔑 Credentials | 6 | LSASS memory, Windows Credential Manager, DPAPI master keys, SAM+SYSTEM hash extraction, Kerberos tickets (TGT/TGS), WiFi passwords |
| ▶️ Execution | 6 | UserAssist, BAM/DAM, SRUM (System Resource Usage Monitor), Run/RunOnce keys, CapabilityAccessManager, RecentApps (Win10) |
| 🔌 USB & Devices | 6 | USB device history (USBSTOR), setupapi.dev.log, MountPoints2 user correlation, USB volume serial number, USB drive letter & volume name, PnP events (EID 20001) |
| 📡 Network | 6 | Network connection artifacts, RDP artifacts, DNS cache, Windows Firewall logs, ARP cache/routing table, WLAN event log |
| 👤 User Activity | 5 | Recent documents (RecentDocs), TypedURLs, Windows Timeline (ActivitiesCache), Sticky Notes, Thumbcache |
| 🔒 Persistence | 5 | Scheduled tasks, Windows services, WMI subscriptions, Boot/UEFI/MBR persistence, DLL hijacking/search order |
| 🔧 Misc | 4 | Notepad++ recent files, Windows Search index, Skype history & chat logs, Windows Copilot/AI activity |
| 🔀 Lateral Movement | 4 | PsExec artifacts, SMB/network share artifacts, WinRM/PowerShell remoting, DCOM/MMC lateral movement |
| 🔐 Account Usage | 4 | Logon types reference (EID 4624), success & failure logon events, NTLM & Kerberos authentication events, last login & password change (SAM) |
| 🧠 Memory | 3 | Hibernate file (hiberfil.sys), pagefile/swapfile, crash dumps (MEMORY.DMP) |
| ☁️ Cloud & Sync | 3 | OneDrive artifacts, Dropbox artifacts, Google Drive/Backup & Sync |
| 🏛️ Active Directory | 3 | NTDS.dit (AD database), DCSync artifacts, Group Policy (GPO) artifacts |
| 📧 Email | 2 | Outlook PST/OST files, Outlook attachment cache |

---

## ✨ Features

**Search**
Type anything in the search bar — artifact name, registry path, file path, event ID, tool name, use case, or any keyword from the notes. Results update instantly.

**Category Filter**
21 category buttons at the top. Click any category to show only those artifacts. Combined with search for fast narrowing.

**Sort**
Sort all visible artifacts by:
- Default order
- Name A → Z or Z → A
- Priority: CRITICAL and HIGH first
- Priority: LOW first
- Category alphabetically

**One-Click Copy**
Every registry path, file path, and command has a copy button next to it. Tap once to copy — no selecting text.

**Quick Hives Strip**
A strip at the top of the page with the 10 most critical forensic paths. One tap copies the full path instantly.

**Forensic Value Rating**
Every artifact is rated:
- 🔴 CRITICAL (26) — must check on every investigation
- 🟡 HIGH (80) — very important, check on most investigations
- 🟢 MEDIUM (29) — situational value
- ⚪ LOW (2) — supplementary

**Per-Artifact Details**
Each artifact card shows:
- Definition and forensic significance
- Exact paths for all relevant Windows versions
- Use cases — what questions this artifact answers
- OS version coverage (XP through Windows 11)
- Analysis tools
- Ready-to-run commands
- Correlated Event IDs

**Mobile Optimised**
Works on phone during live investigations. Single column layout, scrollable filter bar, scrollable command blocks, large tap targets on all copy buttons.

---

## 🛠️ Tools Referenced

`Autopsy` `Volatility 3` `RegRipper` `Registry Explorer` `Chainsaw` `Hayabusa` `Hindsight` `MFTECmd` `PECmd` `LECmd` `JLECmd` `AmcacheParser` `AppCompatCacheParser` `SrumECmd` `EvtxECmd` `WxTCmd` `RBCmd` `ShellBagsExplorer` `DB Browser for SQLite` `FTK Imager` `Velociraptor` `Plaso` `log2timeline` `Impacket` `USB Detective` `SkypeLogView` `Nirsoft Suite`

---

## ✅ Accuracy & Audit

This reference was reviewed in a GCFA-style technical audit (May 2026) against authoritative DFIR sources including Microsoft Learn, SANS FOR500/FOR508, Eric Zimmerman tool documentation, MITRE ATT&CK, Velociraptor artifact definitions, Forensics Wiki, and primary research blogs.

**Overall audit score: 8.2 / 10**

| Dimension | Score |
|---|---|
| Coverage | 9 / 10 |
| Accuracy | 8 / 10 |
| Depth | 9 / 10 |
| Currency | 8 / 10 |
| Usability | 9 / 10 |

15 corrections were applied following the audit, including fixes to RecentApps OS coverage, AmCache/ShimCache relationship, certutil CryptnetUrlCache path, Hibernate SSD behavior, DPAPI master key path, Prefetch SSD myth, BAM/DAM command-line capture claim, Kerberos on-disk ticket paths, Sysmon OS support, Jump Lists default item count, UserAssist ROT13 scope, SDelete default pass count, Scheduled Tasks canonical path, and Skype legacy storage annotation.

---

## ⚠️ Disclaimer

This reference is intended for authorized forensic investigations, incident response, and security research only. All information is provided for defensive and educational purposes.
