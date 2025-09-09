# 🔎 Passive Reconnaissance (PASSIVE_RECON)

This repository contains my **Cybersecurity Internship Assignment 2** on **Passive Footprinting & Reconnaissance** using Kali Linux tools.  
It demonstrates how to gather publicly available information about a target without active interaction — the **first step in penetration testing**.

---

## 📌 Scope
- Legal & educational use only.
- Target domains must be **approved bug bounty programs, personal labs, or authorized test domains**.

---

## 🚀 Steps Performed

### 1️⃣ DOMAIN_INFO_GATHERING
- `whois`
- `dig`
- `nslookup`

### 2️⃣ SUBDOMAIN_ENUMERATION
- `subfinder`
- `assetfinder`
- `amass (passive mode)`

### 3️⃣ EMAIL & EMPLOYEE INFO
- `theHarvester`

### 4️⃣ METADATA EXTRACTION
- `metagoofil`
- `exiftool`
- `strings`

### 5️⃣ GOOGLE DORKING
- `site:example.com filetype:pdf`
- `site:example.com intitle:"index of"`

### 6️⃣ SOCIAL MEDIA_INFO_GATHERING
- Maltego CE
- SpiderFoot

### 7️⃣ URL & JS FILE COLLECTION
- `gau`
- `katana`

### 8️⃣ JS SECRETS LEAKS
- `JSleak`

---

## 📂 Repository Contents
- **scripts/** → Shell scripts & notes for tools used.  
- **findings/** → Example outputs from scans.  
- **reports/** → Passive Recon Report template for submission.  

---

## 📊 Deliverables
- WHOIS & DNS findings  
- Subdomains discovered  
- Emails / Employee info  
- Metadata extracted  
- Google dorks used & results  
- OSINT summary  
- URLs & JS leaks  
- Conclusion → Identified possible attack surfaces  

---

## ⚠️ Disclaimer
This project is for **educational purposes only**. Do not use against unauthorized targets.
