# 🔍 Shodan Cheat Sheet

```
╔═══════════════════════════════════════════════════════════════════════╗
║                                                                       ║
║   ░██████╗██╗░░██╗░█████╗░██████╗░░█████╗░███╗░░██╗                   ║
║   ██╔════╝██║░░██║██╔══██╗██╔══██╗██╔══██╗████╗░██║                   ║
║   ╚█████╗░███████║██║░░██║██║░░██║███████║██╔██╗██║                   ║
║   ░╚═══██╗██╔══██║██║░░██║██║░░██║██╔══██║██║╚████║                   ║
║   ██████╔╝██║░░██║╚█████╔╝██████╔╝██║░░██║██║░╚███║                   ║
║   ╚═════╝░╚═╝░░╚═╝░╚════╝░╚═════╝░╚═╝░░╚═╝╚═╝░░╚══╝                   ║
║                                                                       ║
║        ▀█▀ █▀█ ▀█▀ █▀▀ █▀█ █▄░█ █▀▀ ▀█▀   █▀▄▀█ █▀█ █▀█ █▀█ █▀▀ █▀█   ║
║        ░█░ █ █ ░█░ ██▄ █▀▄ █░▀█ ██▄ ░█░   █░▀░█ █▀█ █▀▀ █▀▀ ██▄ █▀▄   ║
║                                                                       ║
║                  ═══[ CYBER RECONNAISSANCE ]═══                       ║
║                                                                       ║
║          ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓                 ║
║          ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░                 ║
║                                                                       ║
║             > Scanning the digital realm...                           ║
║             > Mapping the IoT landscape...                            ║
║             > Discovering vulnerable systems...                       ║
║                                                                       ║
║                  [████████████████████] 100%                          ║
║                                                                       ║
╚═══════════════════════════════════════════════════════════════════════╝
```

> A comprehensive guide to mastering Shodan for reconnaissance, vulnerability research, and security auditing.

---

## 📹 Finding Cameras

> [!NOTE]
> **Common Ports for IP Cameras** 📷
> - **HTTP**: 80, 8080
> - **HTTPS**: 443
> - **RTSP**: 554
> - **Custom Ports**: Vary by manufacturer (e.g., 81, 8888)

### 🎥 Camera Models and Brands

#### Axis Cameras 📹
- **Common Ports**: 80, 443
- **Search Queries**: `title:"AXIS"` | `product:"Axis"`

#### D-Link Cameras 🔗
- **Common Ports**: 80, 8080
- **Search Queries**: `title:"DCS-930L"` | `product:"D-Link"`

#### Foscam Cameras 📷
- **Common Ports**: 80, 88, 443
- **Search Queries**: `title:"Foscam"` | `product:"Foscam"`

#### Linksys Cameras 📹
- **Common Ports**: 80, 1024
- **Search Queries**: `title:"Linksys WVC80N"` | `product:"Linksys"`

#### Panasonic Cameras 🎥
- **Common Ports**: 80, 443
- **Search Queries**: `title:"Panasonic Network Camera"` | `product:"Panasonic"`

#### Sony Cameras 📷
- **Common Ports**: 80, 443
- **Search Queries**: `title:"Sony Network Camera"` | `product:"Sony"`

#### Trendnet Cameras 🔍
- **Common Ports**: 80, 443
- **Search Queries**: `title:"TV-IP"` | `product:"Trendnet"`

#### TP-Link Cameras 📹
- **Common Ports**: 80, 8080
- **Search Queries**: `title:"TP-Link"` | `product:"TP-Link"`

#### Hikvision Cameras 🎬
- **Common Ports**: 80, 443, 554, 8000, 8080
- **Search Queries**: `title:"Hikvision"` | `product:"Hikvision"`

#### Vivotek Cameras 📷
- **Common Ports**: 80, 443
- **Search Queries**: `title:"Vivotek"` | `product:"Vivotek"`

#### AvTech Cameras 🎥
- **Common Ports**: 80, 8888
- **Search Queries**: `title:"AVTech"` | `product:"AvTech"`

#### Wansview Cameras 📹
- **Common Ports**: 80, 8080
- **Search Queries**: `title:"Wansview"` | `product:"Wansview"`

#### Dahua Cameras 🔍
- **Common Ports**: 80, 443, 554, 8000, 8080, 8081, 8888
- **Search Queries**: `title:"Dahua"` | `product:"Dahua"` | `html:"Dahua"`

#### Ubiquiti UniFi Cameras 🌐
- **Common Ports**: 80, 443, 8080, 8443, 7080, 7443
- **Search Queries**: `title:"UniFi"` | `product:"Ubiquiti"` | `"UniFi Video"`

#### Reolink Cameras 📷
- **Common Ports**: 80, 443, 8080
- **Search Queries**: `title:"Reolink"` | `product:"Reolink"` | `html:"Reolink"`

#### Wyze Cameras 📹
- **Common Ports**: 80, 443, 8080
- **Search Queries**: `title:"Wyze"` | `product:"Wyze"`

#### Uniview Cameras 🎥
- **Common Ports**: 80, 443, 554, 8080, 8443
- **Search Queries**: `title:"Uniview"` | `product:"Uniview"`

#### Amcrest Cameras 📷
- **Common Ports**: 80, 8080, 8000
- **Search Queries**: `title:"Amcrest"` | `product:"Amcrest"`

#### Lorex Cameras 🔍
- **Common Ports**: 80, 443
- **Search Queries**: `title:"Lorex"` | `product:"Lorex"`

#### Mobotix Cameras 📹
- **Common Ports**: 80, 443, 8080
- **Search Queries**: `title:"Mobotix"` | `product:"Mobotix"`

#### Avigilon Cameras 🎬
- **Common Ports**: 80, 443, 554, 8080
- **Search Queries**: `title:"Avigilon"` | `product:"Avigilon"`

#### GoPro Cameras 📷
- **Common Ports**: 8080
- **Search Queries**: `title:"GoPro"` | `product:"GoPro"`

#### FLIR Cameras 🌡️
- **Common Ports**: 80, 443, 554
- **Search Queries**: `title:"FLIR"` | `product:"FLIR"`

### 💡 Example Queries

<details>
<summary><strong>🇺🇸 Axis Cameras in the United States</strong></summary>

```shodan
title:"AXIS" country:"US"
```
</details>

<details>
<summary><strong>📸 Foscam Cameras with Screenshots</strong></summary>

```shodan
title:"Foscam" has_screenshot:true
```
</details>

<details>
<summary><strong>🏙️ Hikvision Cameras in New York</strong></summary>

```shodan
title:"Hikvision" city:"New York"
```
</details>

<details>
<summary><strong>🔌 TP-Link Cameras on Port 8080</strong></summary>

```shodan
title:"TP-Link" port:8080
```
</details>

<details>
<summary><strong>🌍 Vivotek Cameras Worldwide</strong></summary>

```shodan
title:"Vivotek"
```
</details>

<details>
<summary><strong>⚙️ D-Link Cameras on Custom Ports</strong></summary>

```shodan
title:"DCS-930L" port:8080
```
</details>

<details>
<summary><strong>🌐 Dahua Cameras Worldwide</strong></summary>

```shodan
title:"Dahua"
```
</details>

<details>
<summary><strong>🇪🇺 Reolink Cameras in Europe</strong></summary>

```shodan
title:"Reolink" country:"DE" OR country:"GB" OR country:"FR"
```
</details>

<details>
<summary><strong>📹 UniFi Cameras with Screenshots</strong></summary>

```shodan
"UniFi Video" has_screenshot:true
```
</details>

<details>
<summary><strong>🔗 Amcrest Cameras on Port 8080</strong></summary>

```shodan
title:"Amcrest" port:8080
```
</details>

<details>
<summary><strong>💾 Dahua Cameras with HTML Interface</strong></summary>

```shodan
html:"Dahua" port:80
```
</details>

## 💡 Tips and Tricks for Advanced Shodan Searching

> [!TIP]
> **Query Optimization & Best Practices** 🚀
> Master these techniques to write more effective and efficient Shodan queries.

### ➕ Using Boolean Operators Effectively

**OR Operator** (Find Multiple Brands)
```shodan
title:"Axis" OR title:"Hikvision" OR title:"Dahua"
```

**AND Operator** (Combine Filters)
```shodan
title:"Camera" AND port:8080 AND country:"US"
```

**NOT Operator** (Exclude Results)
```shodan
title:"Camera" NOT "authentication required"
```

### ⚙️ Advanced Query Techniques

**Search by HTTP Header**
```shodan
header:"Server: Boa"
```

**Search by Specific HTTP Status Codes**
```shodan
http.status:200 "admin"
```

**Find Open Web Interfaces**
```shodan
"200 OK" http.title:"Index of"
```

**Search Across Multiple Ports**
```shodan
title:"Camera" (port:80 OR port:8080 OR port:8888)
```

**Combine Product Name with Vulnerable Versions**
```shodan
product:"Apache" "2.2.15"
```

**Find Devices with Outdated Java**
```shodan
java org:*
```

### 🔍 Filtering by Response Content

**Find Pages with Specific Keywords**
```shodan
"username" "password" filetype:html
```

**Search for Default Pages**
```shodan
"It works!" "Apache"
```

**Find Administrative Interfaces**
```shodan
title:"Admin" OR title:"Administration"
```

### 🏢 Organizational & Network Searches

**Find All Devices from a Specific Organization**
```shodan
org:"Company Name"
```

**Search by Autonomous System Number (ASN)**
```shodan
asn:AS12345
```

**Search by IP Range (CIDR Notation)**
```shodan
net:192.168.1.0/24
```

### 🌍 Combining Geographic + Service Filters

**Find a Specific Service in Multiple Countries**
```shodan
title:"Camera" (country:"US" OR country:"CA" OR country:"MX")
```

**Search Specific Regions for Vulnerable Services**
```shodan
"MongoDB Server Information" port:27017 region:"California"
```

**Find Devices in a City with a Specific Product**
```shodan
product:"Cisco" city:"London"
```

### ⚡ Performance Optimization Tips

- **Use Specific Queries**: More specific queries return faster results
- **Avoid Common Keywords Alone**: Instead of just `port:80`, combine with product or title
- **Use has_screenshot Filter Sparingly**: Screenshots slow down queries
- **Limit Geographic Scope**: Searching worldwide takes longer; narrow by country when possible
- **Use Title/Product Filters**: These are indexed and search faster than HTML content

### 📋 Query Syntax Reference

| Filter | Usage | Example |
|:------:|:-----:|:-------:|
| `title:` | Search page title | `title:"Admin Panel"` |
| `product:` | Search product name | `product:"Apache"` |
| `port:` | Search specific port | `port:22` |
| `country:` | Filter by country code | `country:"US"` |
| `city:` | Filter by city | `city:"New York"` |
| `region:` | Filter by state/region | `region:"California"` |
| `org:` | Search by organization | `org:"Google"` |
| `asn:` | Search by ASN | `asn:AS15169` |
| `net:` | Search by IP range | `net:8.8.8.0/24` |
| `geo:` | Search by coordinates | `geo:"40.7128,-74.0060"` |
| `vuln:` | Search by vulnerability | `vuln:heartbleed` |
| `has_screenshot:` | Include/exclude screenshots | `has_screenshot:true` |
| `html:` | Search in HTML content | `html:"server version"` |
| `header:` | Search HTTP headers | `header:"Server: Nginx"` |

## ⚠️ Finding Vulnerable Servers

> [!IMPORTANT]
> **Common Vulnerabilities and Their Shodan Queries** 🔓
>
> These queries help identify common vulnerabilities. Always use findings responsibly and with proper authorization.

### Known Vulnerability Queries

**Heartbleed (CVE-2014-0160)** 🩹
```shodan
vuln:heartbleed
```

**OpenSSL CCS Injection (CVE-2014-0224)** 🔐
```shodan
vuln:CVE-2014-0224
```

**Shellshock (CVE-2014-6271)** 💥
```shodan
vuln:CVE-2014-6271
```

**EternalBlue (MS17-010)** 🛡️
```shodan
vuln:ms17-010
```

### Default Credentials 🔑

**FTP with Anonymous Login**
```shodan
"220" "Anonymous FTP login allowed"
```

**Telnet with Default Credentials**
```shodan
"220" "telnet" "default password"
```

### 📦 Outdated Software

**Outdated Apache Servers**
```shodan
"Apache/2.2.15"
```

**Outdated IIS Servers**
```shodan
"Microsoft-IIS/6.0"
```

### 🎯 Example Queries by Service and Vulnerability

**Open MongoDB Instances**
```shodan
"MongoDB Server Information" port:27017
```

**ElasticSearch Instances Without Authentication**
```shodan
"200 OK" "elastic indices" port:9200
```

**Open SMB Shares**
```shodan
port:445 "smb" "NT_STATUS_ACCESS_DENIED"
```

**Exposed RDP Services**
```shodan
port:3389
```

### 🗺️ Advanced Filtering by Location

> [!TIP]
> **Combining Vulnerability Queries with Geographic Filters** 📍
>
> Narrow down vulnerability searches by location for more targeted research.

**EternalBlue in the United States**
```shodan
vuln:ms17-010 country:"US"
```

**Open MongoDB Instances in Germany**
```shodan
"MongoDB Server Information" port:27017 country:"DE"
```

**Shellshock Vulnerable Servers in California**
```shodan
vuln:CVE-2014-6271 region:"California"
```

**Heartbleed Vulnerable Servers in London**
```shodan
vuln:heartbleed city:"London"
```

### 🔗 Combining Multiple Filters for Specific Searches

**Outdated Apache Servers with Screenshots in France**
```shodan
"Apache/2.2.15" country:"FR" has_screenshot:true
```

**Elasticsearch with Screenshots in the UK**
```shodan
"200 OK" "elastic indices" port:9200 country:"GB" has_screenshot:true
```

**FTP Servers with Anonymous Login in Japan**
```shodan
"220" "Anonymous FTP login allowed" country:"JP"
```

## 🌍 Searching by Geographic Filters

> [!NOTE]
> **Common Geographic Filters** 📍
>
> - **Country**: `country:"<country_code>"`
> - **City**: `city:"<city_name>"`
> - **Region/State**: `region:"<region_name>"`
> - **Coordinates**: `geo:"<latitude>,<longitude>"`

### 🌐 Example Queries by Service and Location

**Web Servers in the United States**
```shodan
http country:"US"
```

**FTP Servers in Germany**
```shodan
ftp country:"DE"
```

**Telnet Servers in London, UK**
```shodan
telnet city:"London"
```

**RDP Servers in California, USA**
```shodan
rdp region:"California"
```

**MySQL Servers in Paris, France**
```shodan
mysql city:"Paris"
```

**Elasticsearch Instances in Berlin, Germany**
```shodan
"elastic indices" port:9200 city:"Berlin"
```

### 🔐 Advanced Geographic Queries

**SSH Servers in Specific Countries**
- 🇺🇸 United States:
  ```shodan
  ssh country:"US"
  ```
- 🇯🇵 Japan:
  ```shodan
  ssh country:"JP"
  ```

**HTTP Servers in Specific Cities**
- 🗽 New York:
  ```shodan
  http city:"New York"
  ```
- 🦘 Sydney:
  ```shodan
  http city:"Sydney"
  ```

**Database Servers in Specific Regions**
- 📍 California:
  ```shodan
  "database" region:"California"
  ```
- 🍁 Ontario:
  ```shodan
  "database" region:"Ontario"
  ```

**Specific Services in Coordinated Areas**
- 📍 Within a 10km radius of New York City:
  ```shodan
  http geo:"40.7128,-74.0060"
  ```

### 🧩 Combining Filters

**Apache Servers in Germany with Screenshots**
```shodan
"Apache" country:"DE" has_screenshot:true
```

**Elasticsearch in the UK and Open Ports**
```shodan
"elastic indices" country:"GB" port:9200
```

**FTP Servers in France with Anonymous Login**
```shodan
"FTP" "Anonymous login allowed" country:"FR"
```

### 🎯 Specific Device Searches

**Axis Cameras in the Netherlands**
```shodan
"AXIS" country:"NL"
```

**Hikvision Cameras in Los Angeles**
```shodan
"Hikvision" city:"Los Angeles"
```

**Cisco Devices in California**
```shodan
"cisco" region:"California"
```

## 🎬 Finding Plex Media Servers

> [!NOTE]
> **Common Ports** 🖥️
>
> - **HTTP**: 32400

### 📡 Search Queries

**Plex Media Servers Worldwide**
```shodan
"X-Plex-Protocol" port:32400
```

**Plex Media Servers in the United States**
```shodan
"X-Plex-Protocol" port:32400 country:"US"
```

**Plex Media Servers in Germany with Screenshots**
```shodan
"X-Plex-Protocol" port:32400 country:"DE" has_screenshot:true
```

---

## 🍓 Finding Raspberry Pi Devices

> [!NOTE]
> **Common Ports** 🔌
>
> - **SSH**: 22
> - **HTTP**: 80

### 📡 Search Queries

**Raspberry Pi Devices via SSH**
```shodan
"Raspbian" port:22
```

**Raspberry Pi Devices via HTTP**
```shodan
"Raspberry Pi" port:80
```

**Raspberry Pi Devices in the United States**
```shodan
"Raspbian" port:22 country:"US"
```

---

## 🖥️ Finding Proxmox Servers

> [!NOTE]
> **Common Ports** 🔐
>
> - **HTTPS**: 8006

### 📡 Search Queries

**Proxmox Servers Worldwide**
```shodan
"Proxmox" port:8006
```

**Proxmox Servers in the United States**
```shodan
"Proxmox" port:8006 country:"US"
```

**Proxmox Servers with Screenshots**
```shodan
"Proxmox" port:8006 has_screenshot:true
```

---

## 🎥 Finding Web Cameras & Video Streaming

> [!NOTE]
> **Common Streaming Protocols & Ports** 📹
>
> - **MJPEG**: 8081, 8082, 8888
> - **RTSP**: 554, 322
> - **HTTP**: 80, 8080

### 📡 Search Queries

**Webcams with MJPEG Streams**
```shodan
"MJPEG Server" port:8081
```

**Devices Streaming Video Content**
```shodan
"Motion JPEG" port:8888
```

**RTSP Protocol Streams**
```shodan
port:554 "rtsp"
```

**Webcams with No Authentication**
```shodan
"200 OK" "webcam" NOT "password"
```

---

## 💡 Finding IoT Devices

> [!NOTE]
> **Common IoT Protocols & Ports** 🌐
>
> - **MQTT**: 1883
> - **CoAP**: 5683
> - **ZigBee**: 6100
> - **Smart Home Hubs**: 8080-8090

### 📡 Search Queries

**IoT Devices via MQTT**
```shodan
port:1883
```

**Smart Home Hubs Worldwide**
```shodan
title:"Home" OR title:"Smart" port:8080
```

**MQTT Brokers with Open Connections**
```shodan
"MQTT" port:1883
```

**IoT Devices from Manufacturers**
```shodan
product:"Arduino" OR product:"Raspberry Pi" OR product:"ESP"
```

---

## 🏭 Finding Industrial Control Systems

> [!NOTE]
> **Common ICS/SCADA Protocols** ⚙️
>
> - **Modbus**: 502
> - **Siemens S7**: 102
> - **Profinet**: 34962-34964
> - **OPC UA**: 4840

### 📡 Search Queries

**Modbus Devices**
```shodan
port:502 "Modbus"
```

**Siemens Control Systems**
```shodan
port:102 "Siemens"
```

**Industrial Devices Worldwide**
```shodan
"Siemens" OR "Modbus" OR "PLC"
```

---

## 💾 Finding Network Attached Storage (NAS)

> [!NOTE]
> **Common NAS Brands & Ports** 📦
>
> - **QNAP**: 8080, 8443
> - **Synology**: 5000, 5001
> - **WD MyCloud**: 80

### 📡 Search Queries

**QNAP NAS Devices**
```shodan
title:"QNAP" port:8080
```

**Synology NAS Devices**
```shodan
"Synology" port:5000
```

**Western Digital MyCloud**
```shodan
"WD MyCloud" port:80
```

**Open NAS Shares**
```shodan
"NAS" "sharing" has_screenshot:true
```

---

## 🗄️ Finding Database Servers

> [!NOTE]
> **Common Database Ports** 📊
>
> - **MySQL**: 3306
> - **PostgreSQL**: 5432
> - **MongoDB**: 27017
> - **Redis**: 6379
> - **Cassandra**: 9042
> - **Elasticsearch**: 9200

### 📡 Search Queries

**Unprotected MongoDB Instances**
```shodan
"MongoDB Server Information" port:27017 -"authentication"
```

**Redis Servers**
```shodan
"redis_version" port:6379
```

**Open PostgreSQL Servers**
```shodan
port:5432 "PostgreSQL"
```

**Elasticsearch Clusters**
```shodan
"elasticsearch" port:9200
```

**MySQL Servers with Default Credentials**
```shodan
"MySQL" port:3306 -"Access denied"
```

---

## 🔒 Finding VPN & Remote Access Services

> [!NOTE]
> **Common Remote Access Ports** 🌐
>
> - **OpenVPN**: 1194
> - **WireGuard**: 51820
> - **IPSec VPN**: 500, 4500
> - **RDP**: 3389
> - **VNC**: 5900-5999

### 📡 Search Queries

**OpenVPN Servers**
```shodan
"OpenVPN" port:1194
```

**RDP Services with Screenshots**
```shodan
port:3389 has_screenshot:true
```

**VNC Servers**
```shodan
port:5900 "RFB"
```

**Citrix Servers**
```shodan
"Citrix" port:1494
```

---

## 🖨️ Finding Printers & Multifunction Devices

> [!NOTE]
> **Common Printer Ports** 📄
>
> - **HP/Canon/Xerox**: 80, 443, 9100 (JetDirect)
> - **Ricoh**: 80, 443, 8080

### 📡 Search Queries

**HP Printers**
```shodan
"HP" port:9100
```

**Canon Printers**
```shodan
title:"Canon" port:80
```

**Xerox Devices**
```shodan
"Xerox" OR "WorkCentre"
```

**Open Printer Interfaces**
```shodan
"printer" port:80 has_screenshot:true
```

---

## 🔍 Advanced Filtering Techniques

> [!TIP]
> **Pro Tips for Finding Specific Vulnerabilities** 🎯
>
> Master these techniques for precise vulnerability discovery.

**Finding Weak SSL/TLS Configurations** 🔐
```shodan
ssl:"OpenSSL/1.0" "weak"
```

**Finding Devices with Exposed Information** 📤
```shodan
"Basic realm" port:80
```

**Finding CVE-Specific Vulnerabilities** 🐛
```shodan
"CVE-2021-21315"
```

**Finding Devices by HTTP Response Headers** 📋
```shodan
"X-Powered-By: PHP" port:80
```

**Finding Devices Running Custom Applications** ⚙️
```shodan
header:"X-Custom-Header"
```

**Geographic Proximity Search** 📍
```shodan
geo:"40.7128,-74.0060" _geo:5000
```

---

## ⌨️ Using Shodan CLI for Advanced Queries

> [!NOTE]
> **Shodan CLI Commands** 💻
>
> Command-line interface for powerful Shodan interactions.

### 📥 Installation
```bash
pip install shodan
```

### 🔑 Initialize Shodan CLI
```bash
shodan init API_KEY
```

### 🔎 Basic Search
```bash
shodan search "apache"
```

### 📊 Export Results to CSV
```bash
shodan search "title:Camera" --fields ip_str,port,org,country,html
```

### 📥 Download Bulk Data
```bash
shodan download camera-results "title:Camera"
```

### 🖥️ Host Information Lookup
```bash
shodan host 8.8.8.8
```

### 🔄 Stream Shodan Data
```bash
shodan stream
```

### 📈 Query with Count
```bash
shodan count "apache"
```

---

## 🎯 Practical Search Strategies

**Strategy 1: Finding Devices by Vulnerability Chain**
```shodan
product:"Cisco" "privilege" "escalation"
```

**Strategy 2: Finding Default Installation Instances**
```shodan
"default username is" OR "default password is"
```

**Strategy 3: Finding Recently Indexed Devices**
```shodan
"200 OK" updated:>2024-11-01
```

**Strategy 4: Finding Devices with Known CVEs**
```shodan
"Apache/2.4.49" OR "Apache/2.4.50"
```

**Strategy 5: Finding Devices in Critical Infrastructure**
```shodan
"SCADA" OR "HMI" OR "historian"
```

---

## 📚 Resources and References

### 🔗 Official Documentation
- [Shodan Official Website](https://www.shodan.io)
- [Shodan CLI Documentation](https://cli.shodan.io)
- [Shodan API Documentation](https://developer.shodan.io)
- [Shodan Query Cheat Sheet](https://cheatsheet.shodan.io)

### 🛠️ Related Tools
- **Shodan Dorking**: Use complex queries to find specific devices
- **Censys**: Alternative internet scan database
- **Shodan Scripts**: Official GitHub repository with helpful scripts
- **Shodan Maps**: Geographic visualization of devices

### 📖 Learning Resources
- **Security Research**: Use Shodan for vulnerability research
- **Threat Intelligence**: Monitor for exposed company devices
- **Network Discovery**: Map your organization's external footprint
- **Compliance**: Identify devices not in compliance with policies

---

## 💼 Common Use Cases

### 🔬 Security Researchers
- Identify vulnerable devices
- Track exploitation of CVEs
- Monitor emerging threats

### 🔐 Penetration Testers
- Recon targets (with authorization)
- Find internet-facing services
- Identify tech stacks

### 🖥️ System Administrators
- Audit exposed services
- Monitor your organization's external presence
- Identify rogue devices

### 🏢 Organizations
- Monitor brand/product mentions
- Identify misconfigurations
- Track shadow IT

---

## ⚖️ Ethical Considerations

> [!IMPORTANT]
> **Ethical Considerations** 🛡️
>
> - **Permission**: Always have explicit permission to search and access devices before attempting any kind of access or testing.
> - **Responsibility**: Use the information to help improve security and report vulnerabilities responsibly.
> - **Legal Compliance**: Ensure compliance with all legal regulations and guidelines (CFAA, GDPR, etc.).
> - **No Malicious Intent**: Do not use Shodan searches for illegal activities, unauthorized access, or data theft.

---

## 📝 Responsible Vulnerability Disclosure

> [!TIP]
> **Best Practices for Reporting Found Issues** 🎯
>
> Responsible disclosure is essential for ethical security research.

### ✅ Steps for Responsible Disclosure

**1. Identify the Vulnerability** 🔍
   - Confirm the vulnerability exists
   - Document your findings with evidence
   - Note the affected systems and versions

**2. Find Contact Information** 📧
   - Look for security.txt file at `/.well-known/security.txt`
   - Check the organization's website for security contacts
   - Search for published vulnerability disclosure policies
   - Use reverse DNS or whois for contact details

**3. Report Responsibly** 📨
   - Send detailed technical report to security contact
   - Provide reasonable timeline for patching (typically 90 days)
   - Do not publicly disclose before vendor has patched
   - Offer to assist with verification of the fix

**4. Document Everything** 📋
   - Keep records of all communications
   - Note dates and responses received
   - Track patch releases and updates

### ⏰ Sample Disclosure Timeline
| Timeline | Action |
|:--------:|:-------|
| **Day 1** | Discover and confirm vulnerability |
| **Day 1** | Contact vendor with details |
| **Day 30** | Follow up if no response |
| **Day 60** | Consider escalation |
| **Day 90** | Coordinate public disclosure after patch |

---

## ✅ Quick Reference Checklist

> [!NOTE]
> **Pre-Search Checklist** 📋
>
> Before conducting any Shodan search, ensure you've covered these items:

- [ ] Do you have authorization to perform this search?
- [ ] Is your search for legitimate security purposes?
- [ ] Have you reviewed the legal implications in your jurisdiction?
- [ ] Are you prepared to responsibly disclose any vulnerabilities?
- [ ] Have you understood Shodan's Terms of Service?
- [ ] Will you report findings to the appropriate parties?

---

## ❌ Common Mistakes to Avoid

- **Over-Broad Searches**: Refine queries to reduce false positives
- **Ignoring False Positives**: Not every result is actually vulnerable
- **Unauthorized Testing**: Never attempt to access systems without permission
- **Public Disclosure**: Never publicly disclose before the vendor has patched
- **Assuming Ownership**: Just because a service is exposed doesn't mean you should access it
- **Ignoring Honeypots**: Some honeypots are intentionally exposed for research

---

<div align="center">

### 🙏 Remember

**With great power comes great responsibility.**

Always conduct your Shodan research ethically, legally, and responsibly.

</div>
