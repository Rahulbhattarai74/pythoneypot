
# 🕵️ Python Honeypot

A **realistic honeypot system** built in Python to simulate vulnerable network services and capture potential attacks for research, monitoring, and analysis.  
This project is designed for **educational use**, allowing students, researchers, and cybersecurity enthusiasts to observe attacker behavior in a safe, controlled environment.

---

## 📖 Project Description

The Python Honeypot listens on a specified port (default: `2222`) and mimics a vulnerable service.  
When an attacker connects, their input (commands, payloads, attempts) is **captured and logged** for later analysis.  
This provides visibility into intrusion attempts and helps understand how attackers probe systems.

Key aspects:
- Lightweight and customizable Python-based honeypot
- Safe for **deployment inside VMs or lab environments**
- Can be extended to simulate multiple services (e.g., SSH, HTTP)
- Helps in **log analysis, intrusion detection training, and cyber research**

---

## ⚙️ Components

1. **Main Honeypot Script (`main.py`)**  
   - Handles socket communication  
   - Listens on configurable port (default: 2222)  
   - Logs all attacker inputs into files

2. **Configuration (`config/honeypot.conf`)**  
   - Stores runtime configurations like:
     - Listening port  
     - Log file path  
     - Service banner (to mimic real systems)

3. **Logging System (`logs/`)**  
   - Stores captured intrusion attempts  
   - Each log entry contains:
     - Timestamp  
     - Attacker IP  
     - Input/command sent

4. **Dependencies (`requirements.txt`)**  
   - Lists Python libraries required for the project

5. **README.md**  
   - Documentation for setup, usage, and project description

---

## 🚀 Features

- 🎯 Simulates a **fake vulnerable service**  
- 📝 Captures **all attacker commands and payloads**  
- 📂 Saves logs in structured format (`logs/honeypot.log`)  
- ⚡ Lightweight and written in **pure Python**  
- 🔧 Configurable service banner and port  
- 🛡️ Safe for controlled environments (e.g., Virtual Machines)

---

## 📂 Project Directory Structure

```
pyhoneypot/
│-- main.py               # Honeypot core script
│-- requirements.txt      # Python dependencies
│-- config/
│   └── honeypot.conf     # Configuration file
│-- logs/
│   └── honeypot.log      # Sample log file
│-- README.md             # Project documentation
```

---

## 🛠️ Technologies & Libraries Used

- **Language:** Python 3.x  
- **Core Libraries:**  
  - `socket` → For creating TCP server (listening for connections)  
  - `logging` → For structured log management  
  - `os`, `datetime` → For handling files & timestamps  
- **Optional Tools:**  
  - Can be extended with `paramiko` (SSH simulation)  
  - `http.server` (for HTTP honeypot module)

---

## ⚙️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR-USERNAME/pyhoneypot.git
   cd pyhoneypot
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python3 -m venv venv
   source venv/bin/activate    # On Linux/Mac
   venv\Scripts\activate     # On Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the honeypot**
   ```bash
   python main.py
   ```

---

## 🔍 Usage

- Default listening port → **2222**  
- Logs stored in: `logs/honeypot.log`  
- Modify `config/honeypot.conf` to change settings

Example log output:
```
[2025-08-24 12:15:32] Connection from 192.168.1.10
[2025-08-24 12:15:34] Received: uname -a
[2025-08-24 12:15:37] Received: cat /etc/passwd
```

---

## ⚠️ Disclaimer

This honeypot is for **educational and research purposes only**.  
Running a honeypot on open networks may attract **real-world attackers**.  
Deploy it **only in isolated environments** (VM, test lab, internal network).  
The authors are **not responsible for misuse**.

---

## 📜 License

This project is licensed under the **MIT License** – free to use, modify, and share.

---

## 👨‍💻 Author
Developed by *[Your Name]* – Cybersecurity Enthusiast  

