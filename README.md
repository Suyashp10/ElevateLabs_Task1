# 🛡️ Cybersecurity Internship - Task 1

## 🔍 Task: Scan Your Local Network for Open Ports

### 🎯 Objective:
Perform a TCP SYN scan on a local network using Nmap, identify open ports, and understand basic network reconnaissance techniques.

---

## 🧰 Tools Used
- **Nmap** (v7.95)
- **Wireshark** (optional, used for packet-level verification)
- **Environment**: Linux virtual lab on NAT interface (eth0)

---

## 🌐 Network Configuration
- **Device IP**: `10.0.2.15`
- **Scanned Subnet**: `10.0.2.0/24`

*Note: This environment is virtualized and isolated from public networks.*

---

## 📊 Nmap Scan Summary

### ✅ Host: 10.0.2.2
| Port | State | Service      |
|------|-------|--------------|
| 135  | open  | msrpc        |
| 445  | open  | microsoft-ds |
| 843  | open  | unknown      |
| 2222 | open  | EtherNetIP-1 |
| 2869 | open  | icslap       |
| 7070 | open  | realserver   |

### ✅ Host: 10.0.2.3
| Port | State | Service |
|------|-------|---------|
| 53   | open  | domain  |

### ✅ Host: 10.0.2.15
- All ports closed ✅

---

## 📡 Wireshark Insights

- A Wireshark capture was performed in parallel to the Nmap scan using the following packet filter: tcp.flags.syn == 1 && tcp.flags.ack == 0
- The original Wireshark capture file (`.pcapng`) has been excluded from this public repository for privacy and operational security.
