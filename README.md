# 🔥 Windows Firewall Configuration

## 📘 Objective

Configure and test basic firewall rules to allow or block network traffic using **Windows Defender Firewall with Advanced Security** on Windows.

---

## 🛠 Tools Used

- Windows Defender Firewall with Advanced Security
- PowerShell (`Test-NetConnection`)
- Optional: OpenSSH Server for Windows

---


---


### 1. Open Firewall Settings

- Opened **Windows Defender Firewall**.
- Navigated to **Advanced Settings** to manage rules.

📷 `screenshots/01-firewall-main-screen.png`

---

### 2. View Current Inbound Rules

- Listed active inbound rules from Advanced Security console.

📷 `screenshots/02-inbound-rules.png`

---

### 3. Block Inbound Traffic on Port 23 (Telnet)

- Created a new inbound rule:
  - Type: Port
  - Protocol: TCP
  - Port: 23
  - Action: Block the connection
  - Profile: Domain, Private, Public

📷 `screenshots/03-block-port-23-rule.png`

---

### 4. Test Blocked Port with PowerShell

```powershell
Test-NetConnection -ComputerName localhost -Port 23

# PowerShell script to test connection to port 23
Test-NetConnection -ComputerName localhost -Port 23



