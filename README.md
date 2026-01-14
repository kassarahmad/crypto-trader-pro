# 🚀 Crypto Trader Pro

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python">
  <img src="https://img.shields.io/badge/FastAPI-Backend-green?logo=fastapi">
  <img src="https://img.shields.io/badge/Uvicorn-ASGI-orange?logo=uvicorn">
  <img src="https://img.shields.io/badge/OpenAI-AI%20Advisor-black?logo=openai">
  <img src="https://img.shields.io/badge/REST-API-lightgrey?logo=swagger">
</p>

**Crypto Trader Pro** is a modular backend dashboard for algorithmic & AI-assisted trading.  
It focuses on **risk management**, **manual control**, and **AI suggestions (never auto-trading)**.

> Educational & experimental project  
> Created by **Ahmad Kassar**

---

## ✨ Features

- 📊 Web dashboard (FastAPI)
- 🛑 Kill-switch (emergency stop)
- ⚖️ Risk profiles (Conservative / Balanced / Aggressive)
- 📉 Global & per-market take-profit
- 🔁 Trailing stop logic
- 🤖 AI trade advisor (optional, read-only)
- 💾 Persistent strategy state
- 🔐 Secure environment-based configuration

---

## 📦 Requirements

- Python **3.10 or newer**
- Git
- Internet connection (for APIs)

---

## 🛠️ Setup (From Zero)

### 1️⃣ Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/crypto-trader-pro.git
cd crypto-trader-pro


---

2️⃣ Create & activate virtual environment

Linux / macOS

python3 -m venv venv
source venv/bin/activate

Windows (PowerShell)

python -m venv venv
.\venv\Scripts\activate


---

3️⃣ Install dependencies

pip install -r requirements.txt


---

🔐 Environment Configuration

The project uses environment variables only (no secrets in code).

Example variables

# Server
API_HOST=127.0.0.1
API_PORT=8000

# Security
EXEC_PIN=1234

# Risk limits
MAX_DAILY_LOSS_USDC=50
MAX_EXPOSURE_USDC=200

# AI (optional)
OPENAI_API_KEY=your_openai_api_key
OPENAI_MODEL=gpt-4.1-mini

Load variables

Linux / macOS

source env.sh

Windows (PowerShell)

$env:EXEC_PIN="1234"
$env:MAX_DAILY_LOSS_USDC="50"


---

▶️ Run the Dashboard

uvicorn main:app --host 127.0.0.1 --port 8000

Open your browser:

http://127.0.0.1:8000


---

🖥️ Dashboard Overview

🔹 Live State

Total PnL

Exposure

Active risk profile

Kill-switch status


🔹 Risk Profiles

Conservative

Balanced

Aggressive
(affects size & exposure limits)


🔹 Protection Controls

Global take-profit

Trailing stop

Per-market take-profit


🔹 AI Advisor (Optional)

Insert token_id

Optional market/news context

AI returns suggestion only

Manual confirmation required with PIN


🔹 Positions

View current positions

PnL & exposure per market



---

🤖 AI Usage Example

1. Insert token_id in AI section


2. Click “Ask AI”


3. Review suggestion:

side (buy / sell / hold)

price

size



4. Enter PIN


5. Click “Execute AI Advice”



⚠️ AI never trades automatically
⚠️ If pricing data is missing → AI will return HOLD


---

🧠 How It Works (In Short)

FastAPI serves the dashboard

Strategy state is saved on disk

Risk checks run before every trade

Kill-switch blocks everything instantly

AI is advisory-only

Manual control is always required



---

⚠️ Disclaimer

This project is:

❌ NOT financial advice

❌ NOT an auto-trading bot

✅ Educational & experimental


You are fully responsible for how you use it.


---

👨‍💻 Author

Ahmad Kassar
Computer Science / Software Engineering
Built with clarity, safety, and discipline

