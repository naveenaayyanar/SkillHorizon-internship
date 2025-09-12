 **Command used**

```bash
nmap -sV -p 22,80,443 -sC testphp.vulweb.com
```

* `-sV`: Detect service versions
* `-p 22,80,443`: Scan only ports 22 (SSH), 80 (HTTP), and 443 (HTTPS)
* `-sC`: Run Nmap’s default scripts (basic enumeration)
* `testphp.vulweb.com`: Target domain

---

### **Results explained**

#### **General Information**

* **Host is up (0.10s latency):** The server responded in 0.1 seconds. It’s online and reachable.
* **Other addresses:** The domain resolves to multiple IPv4 and IPv6 addresses. Nmap picked one (`139.162.174.209`) for scanning.
* **rDNS record:** Reverse DNS points to `139-162-174-209.ip.linodeusercontent.com` → the host is on **Linode** infrastructure.

---

#### **Port Analysis**

1. **Port 22/tcp → filtered ssh**

   * **State:** `filtered` → Nmap cannot tell if the port is open or closed because a firewall is blocking probes.
   * **Service:** SSH (usually used for remote administration).
   * Means: You can’t access SSH directly; the server likely has a firewall or intrusion prevention system.

---

2. **Port 80/tcp → open http**

   * **State:** `open` → The port is accessible.
   * **Service:** HTTP (web traffic)
   * **Version:** `OpenResty web app server 1.27.1.2`

     * OpenResty is a web platform built on Nginx, often used for dynamic apps.
   * **Script results:**

     * `http-robots.txt: 1 disallowed entry` → A `robots.txt` file exists, and it blocks at least 1 path from web crawlers.
     * `http-title: vulweb.com` → The website title is **vulweb.com**.
     * `http-server-header: openresty/1.27.1.2` → The server explicitly reveals it’s OpenResty.

---

3. **Port 443/tcp → open ssl/http**

   * **State:** `open` → The HTTPS service is accessible.
   * **Service:** HTTPS (SSL/TLS encrypted web traffic)
   * **Version:** OpenResty web app server 1.27.1.2 (same as port 80, but encrypted).
   * **SSL certificate details:**

     * **Subject CommonName:** `vulweb.com`
     * **Subject Alternative Name:** `*.vulweb.com`, `vulweb.com` → The certificate is valid for both the root domain and all subdomains.
   * Suggests the site has a proper SSL setup.

---

### **Summary of findings**

* ✅ Website is running on **OpenResty (Nginx-based)**, both HTTP (80) and HTTPS (443).
* ✅ SSL certificate is valid for domain + wildcard subdomains.
* ⚠️ SSH (22) is **filtered** (likely blocked by firewall).
* ⚠️ `robots.txt` exists and disallows at least one path (could hint at hidden directories).

-