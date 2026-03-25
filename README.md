🤖 F.R.I.D.A.Y – AI Desktop Assistant

Your personal Jarvis-like AI assistant built in Python

🚀 Overview

F.R.I.D.A.Y (Female Replacement Intelligent Digital Assistant Youth) is a powerful AI assistant built by Nirupam.
It combines voice recognition, automation, AI responses, and remote control into one system — just like Jarvis from Iron Man.

This assistant can:

Talk with you 🎙️
Control your PC 💻
Automate tasks ⚡
Connect to your phone 📱
Even monitor security 🔐
✨ Features
🎤 Voice & AI
Wake word detection ("Friday")
Speech recognition & voice commands
AI responses using Groq (LLaMA model)
Multiple personality modes:
Friday (default)
Jarvis
Stark
Casual
🔐 Security System
Voice authentication
Face recognition unlock
Session timeout protection
Intruder alerts
Encrypted memory (optional modules)
📱 Remote Control (Phone + Telegram)
Control PC from your phone (Flask server)
Telegram bot integration:
Check system status
Take screenshots
Play music
Lock PC
Shutdown system
🎵 Media & Entertainment
Play music from:
YouTube Music
Spotify
Local files
Auto DJ (time-based music suggestions)
Trivia game & fun features
📊 Productivity Tools
Notes system
Reminders & timers
Weekly reports
Dashboard analytics
Email drafting
🌐 Smart Features
Weather updates
News briefing
Stock & crypto tracking
Flight tracking
Screenshot analysis
🖥️ System Control
Open apps
Take screenshots
Monitor CPU, RAM, battery
File explorer access
ADB phone control (Android)
⚙️ Advanced Features
Heavy task mode (auto-generate files like):
Code
Essays
Stories
Modular system (plug-and-play features)
Ngrok remote access
Multi-threaded architecture
🛠️ Tech Stack
Python
Flask (Web server)
SpeechRecognition
Edge TTS / Amazon Polly
PyAutoGUI
OpenCV (Face recognition)
Porcupine (Wake word)
Groq API (AI)
Telegram Bot API
📦 Installation
1. Clone the repo
git clone https://github.com/Nirupam12345/F.R.I.D.A.Y
cd friday-ai
2. Install dependencies
pip install -r requirements.txt
3. Add your API keys

Edit the script and add:

Groq API key
Weather API key
Telegram bot token
(Optional) AWS Polly keys
4. Run the assistant
python friday.py
📱 Phone Access
Runs on:
http://localhost:5000
Use ngrok for remote access
🧩 Modular Features

You can add extra features by dropping .py files into the project folder:

Example modules:

reminders.py
news_briefing.py
automation_routines.py
personality_modes.py
⚠️ Security Notice
Never upload your API keys to GitHub
Use .env or config files for secrets
Rotate keys if exposed
📸 Future Plans
Full GUI interface
Better mobile app
Smarter AI memory
Offline AI support
Voice cloning
👨‍💻 Creator

Nirupam

“Building my own Jarvis from scratch.”

⭐ Support

If you like this project:

⭐ Star the repo
🍴 Fork it
🚀 Improve it
