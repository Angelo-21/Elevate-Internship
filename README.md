# 🔍 Local Network Port Scan 

## 🎯 Objective
To discover open ports on devices within the local network using **Nmap**, and optionally analyze packet captures using **Wireshark**, in order to understand network exposure and identify potential security risks.

---

## 🛠️ Tools Used

- **Nmap 7.95** (Kali Linux)
- **Wireshark** – For capturing and analyzing network traffic
- **Kali_linux- Terminal**

---

## 📡 IP Range Scanned

- **Local IP Address**: `192.168.83.131`
- **Subnet Range**: `192.168.83.0/24`

---

### 🔧 Command Used:

ifconfig 192.168.83.131

nmap --script=vulners.nse -sV -p 21,22,23 -oN vulnerbaility_machine_ftp.txt 192.168.83.131
