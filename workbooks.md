# 📘 Sentinel Workbooks & Visualizations

This folder contains Azure Workbooks used to visualize metrics from the honeynet lab.

## 1️⃣ Windows RDP Authentication Failures (Map)

This visualization maps failed RDP login attempts on the Windows honeypot using GeoIP data.

**File:** `windows-rdp-auth-fail.json`  
**Query:** Uses GeoIP watchlist and failed RDP (Event ID 4625, Logon Type 10) logs  
🔗 [View JSON file](https://github.com/Vivin001/azure-soc-honeynet/blob/main/windows-rdp-auth-fail.json)

**How it works:**
- Uses SecurityEvent log (Event ID 4625, 4624 Logon Type 10)
- Aggregates location using a custom GeoIP watchlist
- Displays failed login attempts on a world map in Azure Workbooks

To use this:
1. Go to **Azure Sentinel → Workbooks**
2. Click **New → Advanced Editor**
3. Paste the JSON content
4. Save and Run

...


## 2️⃣ NSG Malicious Allowed In (Firewall Analysis)

This visualization shows the malicious network traffic that is allowed by the Network Security Group (NSG) and reached the honeynet.

**File:** `nsg-malicious-allowed-in.json`  
**Query:** Visualizes allowed malicious network traffic and identifies potential inbound attacks.
🔗 [View JSON file](https://github.com/Vivin001/azure-soc-honeynet/blob/main/nsg-malicious-allowed-in.json)

**How it works:**
- Analyzes inbound traffic allowed by NSG rules
- Filters malicious traffic based on pre-defined threat intelligence feeds
- Displays attack origin country and city using the same **GeoIP watchlist** used in other workbooks

To use this:
1. Go to **Azure Sentinel → Workbooks**
2. Click **New → Advanced Editor**
3. Paste the JSON content
4. Save and Run


...


## 3️⃣ MSSQL Authentication Failures (Map View)

This visualization shows failed MSSQL login attempts on the honeypot using GeoIP data.

**File:** `mssql-auth-fail.json`  
**Query:** Uses GeoIP watchlist and failed MSSQL (Event ID `18454`) login attempts  
🔗 [View JSON file](https://github.com/Vivin001/azure-soc-honeynet/blob/main/mssql-auth-fail.json)

**How it works:**
- Uses **SecurityEvent log** (Event ID `18454`) for MSSQL authentication failures
- Aggregates location data using a custom GeoIP watchlist
- Displays failed login attempts on a world map in Azure Workbooks, showing attack origin by **country and city**

To use this:
1. Go to **Azure Sentinel → Workbooks**
2. Click **New → Advanced Editor**
3. Paste the JSON content
4. Save and Run


...


## 4️⃣ Linux SSH Authentication Failures (Map View)

This visualization shows failed SSH login attempts on the Linux honeypot using GeoIP data.

**File:** `linux-ssh-auth-fail.json`  
**Query:** Uses GeoIP watchlist and failed SSH (Event ID `sshd` or `Failed password`) login attempts  
🔗 [View JSON file](https://github.com/Vivin001/azure-soc-honeynet/blob/main/linux-ssh-auth-fail.json)

**How it works:**
- Uses **Syslog** or **Custom Logs** to capture failed SSH login attempts (`sshd` or `Failed password` entries)
- Aggregates location data using a custom GeoIP watchlist
- Displays failed login attempts on a world map in Azure Workbooks, showing attack origin by **country and city**

To use this:
1. Go to **Azure Sentinel → Workbooks**
2. Click **New → Advanced Editor**
3. Paste the JSON content
4. Save and Run






