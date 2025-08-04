# 🔍 Local Network Port Scan 

## 🎯 Objective
To discover open ports on devices within the local network using **Nmap**, and optionally analyze packet captures using **Wireshark**, in order to understand network exposure and identify potential security risks.

---

## 🛠️ Tools Used

- **Nmap 7.95** (Kali Linux)
- **Kali_linux- Terminal**

---

## 📡 IP Range Scanned

- **Local IP Address**: `192.168.83.131`
- **Subnet Range**: `192.168.83.0/24`

---

### 🔧 Command Used:

ifconfig 192.168.83.131

nmap --script=vulners.nse -sV -p 21,22,23 -oN vulnerbaility_machine_ftp.txt 192.168.83.131

---

### 🔐 Key Findings
1 devices responded within the scanned subnet.

Device 192.168.3783.131 had several open ports, including:

| Port     | State | Service      |
| -------- | ----- | ------------ |
| 21/tcp   | open  | ftp          |
| 22/tcp   | open  | ssh          |
| 23/tcp   | open  | telnet       |
| 25/tcp   | open  | smtp         |
| 53/tcp   | open  | domain       |
| 80/tcp   | open  | http         |
| 111/tcp  | open  | rpcbind      |
| 139/tcp  | open  | netbios-ssn  |
| 445/tcp  | open  | microsoft-ds |
| 512/tcp  | open  | exec         |
| 513/tcp  | open  | login        |
| 514/tcp  | open  | shell        |
| 1099/tcp | open  | rmiregistry  |
| 1524/tcp | open  | ingreslock   |
| 2049/tcp | open  | nfs          |
| 2121/tcp | open  | ccproxy-ftp  |
| 3306/tcp | open  | mysql        |
| 5432/tcp | open  | postgresql   |
| 5900/tcp | open  | vnc          |
| 6000/tcp | open  | X11          |
| 6667/tcp | open  | irc          |
| 8009/tcp | open  | ajp13        |
| 8180/tcp | open  | unknown      |


---
### ✅ Conclusion
During this task, I performed a detailed network scan using Nmap to identify live hosts and open ports within my local subnet.

I then extended the scan to a more vulnerable machine and identified multiple open ports such as FTP (21), SSH (22), Telnet (23). These services, if misconfigured or unpatched, can expose systems to critical vulnerabilities like unauthorized access, remote code execution, or data leaks.

This task helped reinforce my understanding of:

Port scanning techniques (-sS, -p, -sV)

Common network services and their risks

The importance of secure configuration and minimal surface exposure

Overall, this was a foundational exercise in network reconnaissance and vulnerability identification, setting the stage for deeper security testing and hardening practices.

---

