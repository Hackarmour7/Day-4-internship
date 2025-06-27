# 🔐 Firewall Configuration & Traffic Filtering

## 🛠 Purpose
This guide explains how to configure and manage firewall rules to control network traffic and improve system security.

---

## ✅ Basic Tasks

1. **View Current Rules**
   - Windows: `wf.msc` or `Get-NetFirewallRule`
   - Linux: `sudo ufw status numbered`

2. **Block Inbound Port**
   - Windows: Block port via GUI or PowerShell
   - Linux: `sudo ufw deny 23/tcp` (blocks Telnet)

3. **Allow Critical Ports**
   - Example: `sudo ufw allow 22/tcp` (SSH)

4. **Test Connectivity**
   - Use `telnet <IP> <port>` to verify rules

5. **Remove Rules**
   - UFW: `sudo ufw delete deny 23/tcp`
   - Windows: Delete rule from Inbound list

---

## 🔎 How It Works

- **Windows**: Block rules override allow
- **Linux UFW**: Deny overrides allow
- **iptables**: First match wins (order matters)

---

## 🔐 Best Practices

- Block by default; allow only needed ports
- Log and monitor denied traffic
- Keep rules minimal and organized
