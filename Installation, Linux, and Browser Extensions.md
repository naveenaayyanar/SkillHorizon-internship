# VM Installation, Linux, and Browser Extensions Usage Guide

---

## 🖥️ Virtual Machine (VM) Installation & Linux

**Need**: A VM provides an isolated environment for testing tools and penetration activities without harming the host system.  
**Usage**: Run Linux distributions such as Kali/Ubuntu inside VirtualBox or VMware.  

**Steps**:  
1. Download and install [VirtualBox](https://www.virtualbox.org/) or VMware Workstation.  
2. Download a Linux ISO (Kali Linux recommended for pentesting).  
3. Create a new VM and allocate RAM (2–4GB) and disk space (20GB+).  
4. Attach ISO and start the VM.  
5. Complete Linux installation and update system packages.  

---

## 🌐 Browser Extensions for Pentesting

### 🔹 FoxyProxy Standard
- **Need**: Easily switch between multiple proxy servers for anonymity and testing.  
- **Steps**:  
  1. Install from Chrome/Firefox Web Store.  
  2. Add new proxy details (IP, port, protocol).  
  3. Enable proxy for browsing.  
  4. Toggle quickly between proxies.  

### 🔹 Wappalyzer
- **Need**: Identify technologies used by a website (CMS, frameworks, databases).  
- **Steps**:  
  1. Install Wappalyzer.  
  2. Visit website → click icon.  
  3. View detected technologies.  

### 🔹 DotGit
- **Need**: Detect exposed `.git` repositories on websites.  
- **Steps**:  
  1. Install DotGit extension.  
  2. Visit a target website.  
  3. Extension auto-detects exposed `.git` directories.  

### 🔹 Gopher
- **Need**: Convert text into URL-encoded payloads.  
- **Usage**: Useful in SSRF and injection attacks.  
- **Steps**:  
  1. Install Gopher.  
  2. Input text/payload.  
  3. Copy encoded URL.  

### 🔹 Knoxss
- **Need**: Automated XSS vulnerability scanner.  
- **Steps**:  
  1. Install Knoxss extension.  
  2. Open target website.  
  3. Run Knoxss scan.  

### 🔹 Cookie-Editor
- **Need**: View, edit, add, or delete cookies.  
- **Steps**:  
  1. Install Cookie-Editor.  
  2. Open any site → view cookies.  
  3. Modify for session hijacking tests.  

### 🔹 JsonWebView
- **Need**: Beautify and view JSON responses.  
- **Steps**:  
  1. Install JsonWebView.  
  2. Open JSON endpoints.  
  3. View formatted JSON.  

### 🔹 HackBar
- **Need**: Manual testing of SQLi, XSS, LFI.  
- **Steps**:  
  1. Install HackBar.  
  2. Enable on target site.  
  3. Inject payloads.  

### 🔹 Hunter.io
- **Need**: Find email addresses associated with domains.  
- **Steps**:  
  1. Sign up at [Hunter.io](https://hunter.io).  
  2. Install extension.  
  3. Visit domain → extension shows emails.  

### 🔹 Trufflehog
- **Need**: Detect exposed secrets (API keys, credentials) in repos.  
- **Steps**:  
  1. Clone repo or visit target site.  
  2. Run Trufflehog scan.  
  3. Identify exposed keys.  

### 🔹 Shodan
- **Need**: Search engine for internet-connected devices.  
- **Steps**:  
  1. Create Shodan account.  
  2. Install extension.  
  3. Search IP/domain/service.  

### 🔹 TouchVPN
- **Need**: Secure browsing with VPN tunneling.  
- **Steps**:  
  1. Install TouchVPN.  
  2. Connect to a country server.  
  3. Browse securely.  

### 🔹 User-Agent Switcher
- **Need**: Change browser User-Agent headers.  
- **Steps**:  
  1. Install extension.  
  2. Select agent (browser/device).  
  3. Reload site.  

### 🔹 Live HTTP Headers
- **Need**: View live HTTP/HTTPS request headers.  
- **Steps**:  
  1. Install Live HTTP Headers.  
  2. Open site → capture requests.  
  3. Inspect headers.  

### 🔹 Retire.js
- **Need**: Detect vulnerable/outdated JavaScript libraries.  
- **Steps**:  
  1. Install Retire.js.  
  2. Visit target site.  
  3. Extension highlights issues.  

### 🔹 BuiltWith
- **Need**: Provides insights about website technologies.  
- **Steps**:  
  1. Install BuiltWith.  
  2. Visit any site.  
  3. View full technology stack.  

---

## 🔒 Managing Extensions in Kali Linux VM

**Need**: Running security-related extensions inside Kali VM ensures isolation and protects your host OS.  
**Usage**: Safely install, configure, and manage penetration testing extensions.  

**Steps**:  
1. Open Firefox/Chromium inside Kali VM.  
2. Navigate: **Menu → Add-ons and Themes → Extensions**.  
3. Search & install extensions (e.g., Wappalyzer, FoxyProxy).  
4. Manage permissions → enable/disable as needed.  
5. Use sidebar (puzzle icon) to access tools quickly.  
6. Keep extensions updated.  
7. Use extensions **only inside VM** for safety.  

---
