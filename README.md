---

# 🚀 Crypto Trader Pro
### AI-Assisted, Risk-Controlled Trading Backend

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python"/>
  <img src="https://img.shields.io/badge/FastAPI-Backend-green?logo=fastapi"/>
  <img src="https://img.shields.io/badge/OpenAI-AI%20Advisor-black?logo=openai"/>
  <img src="https://img.shields.io/badge/OS-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey?logo=linux"/>
  <img src="https://img.shields.io/badge/License-Educational-orange"/>
</p>

---

## 👨‍💻 Author

**Created, designed and engineered by Ahmad Kassar**  
Computer Science student – Software Engineering focus

This project demonstrates:
- Backend system architecture
- Safe automation principles
- AI integration with human control
- Real-world risk management logic

---

## 📌 What Is Crypto Trader Pro?

Crypto Trader Pro is a **professional trading backend framework**, not a “click and profit” bot.

It is built to:
- Observe live markets
- Track exposure and PnL
- Enforce strict risk rules
- Allow AI to **suggest**, not execute
- Require **explicit human approval**

It can be used for:
- Learning backend engineering
- Studying algorithmic trading systems
- Simulations & paper trading
- Research and experimentation
- Extending into real trading systems

---

## 🧠 Core Philosophy

> **Automation must be controlled**  
> **AI must advise, not decide**  
> **Risk overrides everything**

---

## 🧩 Technologies Used

| Category | Technology |
|-------|-----------|
| Language | 🐍 Python |
| Web API | ⚡ FastAPI |
| Server | 🦄 Uvicorn |
| AI | 🧠 OpenAI API (optional) |
| Data | 📄 JSON (persistent state) |
| Frontend | 🌐 HTML + CSS + JS |
| OS Support | 🖥️ Windows / Linux / macOS |
| Security | 🔐 Environment variables |

---

## 📂 Project Structure

crypto-trader-pro/ │ ├── main.py                  # FastAPI entry point ├── config.py                # Environment configuration ├── logger_setup.py          # Logging │ ├── polymarket_client.py     # Market interface (replaceable) │ ├── risk.py                  # Risk checks ├── risk_profiles.py         # Conservative / Balanced / Aggressive ├── kill_switch.py           # Emergency stop system │ ├── strategy_state.py        # Persistent strategy state │ ├── ai_advisor.py            # AI logic (optional) ├── ai_buffer.py             # Last AI advice ├── ai_history.py            # AI advice history │ ├── requirements.txt         # Python dependencies ├── README.md                # This file └── env.sh                   # Environment variables

---

## 🖥️ Supported Operating Systems

✅ Windows 10 / 11  
✅ Linux (Ubuntu, Debian, Arch, etc.)  
✅ macOS (Intel & Apple Silicon)  
✅ WSL  
✅ Cloud servers / VPS  

---

## 🔧 Requirements

### Mandatory
- Python **3.10 or newer**
- Internet connection
- Terminal / Shell

### Optional
- OpenAI API key (only for AI features)

---

## 🛠️ Installation – From Zero (ALL OS)

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/crypto-trader-pro.git
cd crypto-trader-pro


---

2️⃣ Create Virtual Environment

Linux / macOS

python3 -m venv venv
source venv/bin/activate

Windows (PowerShell)

python -m venv venv
.\venv\Scripts\activate


---

3️⃣ Install Dependencies

pip install -r requirements.txt


---

🔐 Environment Configuration (IMPORTANT)

The project only uses environment variables.
No secrets are hard-coded.

Create env.sh

#!/usr/bin/env bash

# ===============================
# Crypto Trader Pro Environment
# ===============================

# --- SERVER ---
export API_HOST="127.0.0.1"
export API_PORT="8000"

# --- SECURITY ---
export EXEC_PIN="1234"
export LOG_LEVEL="INFO"

# --- RISK LIMITS ---
export MAX_DAILY_LOSS_USDC="50"
export MAX_EXPOSURE_USDC="200"

# --- AI (OPTIONAL) ---
export OPENAI_API_KEY="sk-REPLACE_WITH_YOUR_KEY"
export OPENAI_MODEL="gpt-4.1-mini"

# --- FILE STORAGE ---
export STATE_FILE="strategy_state.json"
export AI_HISTORY_FILE="ai_history.json"
export KILL_SWITCH_FILE="kill_switch.json"

echo "Environment loaded"

Load Environment

Linux / macOS / WSL

source env.sh

Windows (PowerShell)

$env:EXEC_PIN="1234"
$env:MAX_DAILY_LOSS_USDC="50"
$env:MAX_EXPOSURE_USDC="200"


---

▶️ Running the Project

uvicorn main:app --host 127.0.0.1 --port 8000

Open your browser:

http://127.0.0.1:8000


---

🖥️ Web Dashboard Features

📊 Live system state

🔴 Kill-switch (manual & automatic)

⚖️ Risk profile selection

📈 Trailing stop & take-profit

🧠 AI advice (optional)

🔐 PIN-protected execution



---

🤖 AI Advisor – How It Works

AI receives structured JSON

AI outputs structured JSON

AI never executes trades directly

If pricing data is missing → AI returns HOLD


Example output:

{
  "summary": "No reliable pricing, hold",
  "bot_trade_input": {
    "side": "hold",
    "price": null,
    "size": 0
  }
}

This behavior is intentional and safe.


---

🔒 Safety Rules (Hard-Coded)

Kill-switch overrides everything

Risk limits override AI

No auto-loops

No blind execution

Human confirmation required



---

⚠️ Disclaimer

This project is:

Educational

Experimental

Research-oriented


It is NOT financial advice.
You are fully responsible for any use.


---

🏁 Final Notes

Crypto Trader Pro is not a toy.
It is a serious backend system, designed with discipline and control.

Use it to:

Learn

Extend

Research

Build something better



---

© Ahmad Kassar – All rights reserved

---

