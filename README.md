---
banner: https://miro.medium.com/v2/resize:fit:832/0*YoUxebMYVClVqOSf.png
sticker: lucide//eye
---
## Finding Cameras

> [!NOTE] **Common Ports for IP Cameras** `fas:Camera`
> - **HTTP**: 80, 8080
> - **HTTPS**: 443
> - **RTSP**: 554
> - **Custom Ports**: Vary by manufacturer (e.g., 81, 8888)

### Camera Models and Brands

#### Axis Cameras
- **Common Ports**: 80, 443
- **Search Queries**:
  - `title:"AXIS"`
  - `product:"Axis"`

#### D-Link Cameras
- **Common Ports**: 80, 8080
- **Search Queries**:
  - `title:"DCS-930L"`
  - `product:"D-Link"`

#### Foscam Cameras
- **Common Ports**: 80, 88, 443
- **Search Queries**:
  - `title:"Foscam"`
  - `product:"Foscam"`

#### Linksys Cameras
- **Common Ports**: 80, 1024
- **Search Queries**:
  - `title:"Linksys WVC80N"`
  - `product:"Linksys"`

#### Panasonic Cameras
- **Common Ports**: 80, 443
- **Search Queries**:
  - `title:"Panasonic Network Camera"`
  - `product:"Panasonic"`

#### Sony Cameras
- **Common Ports**: 80, 443
- **Search Queries**:
  - `title:"Sony Network Camera"`
  - `product:"Sony"`

#### Trendnet Cameras
- **Common Ports**: 80, 443
- **Search Queries**:
  - `title:"TV-IP"`
  - `product:"Trendnet"`

#### TP-Link Cameras
- **Common Ports**: 80, 8080
- **Search Queries**:
  - `title:"TP-Link"`
  - `product:"TP-Link"`

#### Hikvision Cameras
- **Common Ports**: 80, 443, 554, 8000, 8080
- **Search Queries**:
  - `title:"Hikvision"`
  - `product:"Hikvision"`

#### Vivotek Cameras
- **Common Ports**: 80, 443
- **Search Queries**:
  - `title:"Vivotek"`
  - `product:"Vivotek"`

#### AvTech Cameras
- **Common Ports**: 80, 8888
- **Search Queries**:
  - `title:"AVTech"`
  - `product:"AvTech"`

#### Wansview Cameras
- **Common Ports**: 80, 8080
- **Search Queries**:
  - `title:"Wansview"`
  - `product:"Wansview"`

### Example Queries

#### Axis Cameras in the United States
```shodan
title:"AXIS" country:"US"
```

#### Foscam Cameras with Screenshots
```shodan
title:"Foscam" has_screenshot:true
```

#### Hikvision Cameras in New York
```shodan
title:"Hikvision" city:"New York"
```

#### TP-Link Cameras on Port 8080
```shodan
title:"TP-Link" port:8080
```

#### Vivotek Cameras Worldwide
```shodan
title:"Vivotek"
```

#### D-Link Cameras on Custom Ports
```shodan
title:"DCS-930L" port:8080
```

## Finding Vulnerable Servers

> [!IMPORTANT] **Common Vulnerabilities and Their Shodan Queries** `fas:Bug`
> - **Heartbleed (CVE-2014-0160)**:
>   ```shodan
>   vuln:heartbleed
>   ```
> - **OpenSSL CCS Injection (CVE-2014-0224)**:
>   ```shodan
>   vuln:CVE-2014-0224
>   ```
> - **Shellshock (CVE-2014-6271)**:
>   ```shodan
>   vuln:CVE-2014-6271
>   ```
> - **EternalBlue (MS17-010)**:
>   ```shodan
>   vuln:ms17-010
>   ```
> - **Default Credentials**:
>   - **FTP with Anonymous Login**:
>     ```shodan
>     "220" "Anonymous FTP login allowed"
>     ```
>   - **Telnet with Default Credentials**:
>     ```shodan
>     "220" "telnet" "default password"
>     ```

### Outdated Software

- **Outdated Apache Servers**:
  ```shodan
  "Apache/2.2.15"
  ```
- **Outdated IIS Servers**:
  ```shodan
  "Microsoft-IIS/6.0"
  ```

### Example Queries by Service and Vulnerability

#### Open MongoDB Instances
```shodan
"MongoDB Server Information" port:27017
```

#### ElasticSearch Instances Without Authentication
```shodan
"200 OK" "elastic indices" port:9200
```

#### Open SMB Shares
```shodan
port:445 "smb" "NT_STATUS_ACCESS_DENIED"
```

#### Exposed RDP Services
```shodan
port:3389
```

### Advanced Filtering by Location

> [!TIP] **Combining Vulnerability Queries with Geographic Filters** `fas:Filter`
> - **EternalBlue in the United States**:
>   ```shodan
>   vuln:ms17-010 country:"US"
>   ```
> - **Open MongoDB Instances in Germany**:
>   ```shodan
>   "MongoDB Server Information" port:27017 country:"DE"
>   ```
> - **Shellshock Vulnerable Servers in California**:
>   ```shodan
>   vuln:CVE-2014-6271 region:"California"
>   ```
> - **Heartbleed Vulnerable Servers in London**:
>   ```shodan
>   vuln:heartbleed city:"London"
>   ```

### Combining Multiple Filters for Specific Searches

#### Outdated Apache Servers with Screenshots in France
```shodan
"Apache/2.2.15" country:"FR" has_screenshot:true
```

#### Elasticsearch with Screenshots in the UK
```shodan
"200 OK" "elastic indices" port:9200 country:"GB" has_screenshot:true
```

#### FTP Servers with Anonymous Login in Japan
```shodan
"220" "Anonymous FTP login allowed" country:"JP"
```

## Searching by Geographic Filters

> [!NOTE] **Common Filters** `fas:Map`
> - **Country**: `country:"<country_code>"`
> - **City**: `city:"<city_name>"`
> - **Region/State**: `region:"<region_name>"`
> - **Coordinates**: `geo:"<latitude>,<longitude>"`

### Example Queries by Service and Location

#### Web Servers in the United States
```shodan
http country:"US"
```

#### FTP Servers in Germany
```shodan
ftp country:"DE"
```

#### Telnet Servers in London, UK
```shodan
telnet city:"London"
```

#### RDP Servers in California, USA
```shodan
rdp region:"California"
```

#### MySQL Servers in Paris, France
```shodan
mysql city:"Paris"
```

#### Elasticsearch Instances in Berlin, Germany
```shodan
"elastic indices" port:9200 city:"Berlin"
```

### Advanced Queries

#### SSH Servers in Specific Countries
- **United States**:
  ```shodan
  ssh country:"US"
  ```
- **Japan**:
  ```shodan
  ssh country:"JP"
  ```

#### HTTP Servers in Specific Cities
- **New York**:
  ```shodan
  http city:"New York"
  ```
- **Sydney**:
  ```shodan
  http city:"Sydney"
  ```

#### Database Servers in Specific Regions
- **California**:
  ```shodan
  "database" region:"California"
  ```
- **Ontario**:
  ```shodan
  "database" region:"Ontario"
  ```

#### Specific Services in Coordinated Areas
- **Within a 10km radius of New York City (Approx. coordinates)**:
  ```shodan
  http geo:"40.7128,-74.0060"
  ```

### Combining Filters

#### Apache Servers in Germany with Screenshots
```shodan
"Apache" country:"DE" has_screenshot:true
```

#### Elasticsearch in the UK and Open Ports
```shodan
"elastic indices" country:"GB" port:9200
```

#### FTP Servers in France with Anonymous Login
```shodan
"FTP" "Anonymous login allowed" country:"FR"
```

### Specific Device Searches

#### Axis Cameras in the Netherlands
```shodan
"AXIS" country:"NL"
```

#### Hikvision Cameras in Los Angeles
```shodan
"Hikvision" city:"Los Angeles"
```

#### Cisco Devices in California
```shodan
"cisco" region:"California"
```

## Finding Plex Media Servers

> [!NOTE] **Common Ports** `fas:Server`
> - **HTTP**: 32400

### Search Queries

#### Plex Media Servers Worldwide
```shodan
"X-Plex-Protocol" port:32400
```

#### Plex Media Servers in the United States


```shodan
"X-Plex-Protocol" port:32400 country:"US"
```

#### Plex Media Servers in Germany with Screenshots
```shodan
"X-Plex-Protocol" port:32400 country:"DE" has_screenshot:true
```

## Finding Raspberry Pi Devices

> [!NOTE] **Common Ports** `fas:Microchip`
> - **SSH**: 22
> - **HTTP**: 80

### Search Queries

#### Raspberry Pi Devices via SSH
```shodan
"Raspbian" port:22
```

#### Raspberry Pi Devices via HTTP
```shodan
"Raspberry Pi" port:80
```

#### Raspberry Pi Devices in the United States
```shodan
"Raspbian" port:22 country:"US"
```

## Finding Proxmox Servers

> [!NOTE] **Common Ports** `fas:NetworkWired`
> - **HTTPS**: 8006

### Search Queries

#### Proxmox Servers Worldwide
```shodan
"Proxmox" port:8006
```

#### Proxmox Servers in the United States
```shodan
"Proxmox" port:8006 country:"US"
```

#### Proxmox Servers with Screenshots
```shodan
"Proxmox" port:8006 has_screenshot:true
```

### Ethical Considerations

> [!IMPORTANT] **Ethical Considerations** `fas:BalanceScale`
> - **Permission**: Always have explicit permission to search and access devices.
> - **Responsibility**: Use the information to help improve security and report vulnerabilities responsibly.
> - **Legal Compliance**: Ensure compliance with all legal regulations and guidelines.
