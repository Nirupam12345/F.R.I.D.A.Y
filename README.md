# F.R.I.D.A.Y — Personal AI Assistant
> *"Hello sir. Friday online. All systems nominal."*

A fully local, voice-controlled AI assistant inspired by Tony Stark's F.R.I.D.A.Y, built in Python. Powered by Groq AI (free, fast, no rate limits). Includes a phone interface accessible from your Android browser and Telegram bot control from anywhere in the world.

![Version](https://img.shields.io/badge/version-7.0-gold)
![Python](https://img.shields.io/badge/python-3.11-blue)
![License](https://img.shields.io/badge/license-MIT-green)

---

## ✨ Features

- 🎙️ **Wake word detection** — Say "Friday" to wake her up (Porcupine or Google fallback)
- 🧠 **Groq AI brain** — Powered by llama3 70B, completely free and insanely fast
- 🔄 **Ollama fallback** — Switches to local AI when internet is unavailable
- 🗣️ **British male voice** — Edge TTS with en-GB-RyanNeural
- 🎵 **Music control** — Spotify, YouTube Music, or local files
- 📱 **Phone interface** — Control Friday from your Android browser on the same WiFi
- 🌍 **Remote access** — Access Friday from anywhere via Ngrok
- 📲 **ADB app launcher** — Open any app on your Android phone by voice
- 🖼️ **Image sharing** — Send photos from phone to PC
- 🤖 **Telegram bot** — Push notifications + two way PC control from anywhere
- 🌤️ **Live weather** — OpenWeatherMap integration
- ⏰ **Reminders & timers** — Voice-set countdowns
- 🧠 **Memory system** — Remembers your last 100 conversations
- 💬 **WhatsApp** — Open and send messages by voice
- 🖥️ **Desktop UI** — Live conversation interface in the browser
- 📊 **System monitoring** — CPU, RAM, disk stats in the UI
- 🔒 **Voice authentication** — Only responds fully to your voice
- 🌙 **Night mode** — Reminds you to sleep after 10pm
- 📝 **Voice notes** — Save and read back notes by voice
- 📧 **Gmail alerts** — Notifies you of important emails
- 🎮 **Fun mode** — Jokes, roasts, easter eggs

---

## 📁 Project Structure

```
Jarvis/
│
├── friday.py            # Main assistant — all logic lives here
├── phone_ui.html        # Mobile web interface (open on phone browser)
├── friday_ui.html       # Desktop UI (auto-opens on startup)
├── friday_status.json   # Live state shared between Python and UI
├── friday_memory.json   # Conversation memory (auto-generated)
├── friday_prefs.json    # User preferences (auto-generated)
├── requirements.txt     # All Python dependencies
└── phone_uploads/       # Images sent from phone (auto-generated)
```

---

## 🛠️ Requirements

### System
- Windows 10/11
- Python 3.11+
- [Ollama](https://ollama.com) (optional, for offline fallback)
- [Android Platform Tools](https://developer.android.com/tools/releases/platform-tools) (for ADB phone app launching)
- [Ngrok](https://ngrok.com) (for remote access)

### Python packages
```bash
pip install -r requirements.txt
```

---

## 🚀 Setup

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/friday-ai.git
cd friday-ai
```

### 2. Create virtual environment
```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Get your free API keys

| Service | Where | What for |
|---|---|---|
| Groq | console.groq.com | AI brain (free) |
| Picovoice | picovoice.ai | Wake word (free) |
| OpenWeatherMap | openweathermap.org | Weather (free) |
| Telegram BotFather | @BotFather on Telegram | Notifications (free) |

### 4. Configure your keys in friday.py
```python
GROQ_API_KEY        = "your_groq_key"
PORCUPINE_KEY       = "your_porcupine_key"
WEATHER_API_KEY     = "your_openweather_key"
WEATHER_CITY        = "your_city"
MUSIC_DIR           = r"C:\path\to\your\music"
TELEGRAM_TOKEN      = "your_telegram_bot_token"
TELEGRAM_CHAT_ID    = "your_chat_id"
TELEGRAM_PASSPHRASE = "your_secret_passphrase"
```

### 5. Run Friday
```bash
python friday.py
```

The desktop UI opens automatically. Your phone URL is printed in the terminal:
```
📱 Phone UI available at: http://192.168.x.x:5000
```
Open that in your **Android Chrome** browser (type `http://` explicitly).

---

## 📱 Phone Setup (ADB App Launching)

To let Friday open apps on your Android phone:

1. On your phone: **Settings → Developer Options → Enable USB Debugging**
2. Connect phone via USB and run:
```bash
adb devices
adb tcpip 5555
```
3. Disconnect USB — ADB now works over WiFi automatically

---

## 🌍 Remote Access (Ngrok)

To access Friday from anywhere in the world:

1. Sign up at ngrok.com
2. Add your auth token:
```bash
ngrok config add-authtoken YOUR_TOKEN
```
3. Friday auto-starts Ngrok on launch
4. Public URL is sent to your Telegram on startup

---

## 🎙️ Voice Commands

| Command | Action |
|---|---|
| `"play [song] on spotify"` | Play on Spotify |
| `"play [song] on youtube"` | Play on YouTube Music |
| `"next song"` / `"skip"` | Skip track |
| `"volume up"` / `"louder"` | Increase volume |
| `"stop music"` | Stop playback |
| `"get weather"` | Weather for your city |
| `"get weather in [city]"` | Weather anywhere |
| `"timer for 10 minutes"` | Set a countdown timer |
| `"remind me in 5 minutes"` | Set a reminder |
| `"open youtube"` | Open website |
| `"open chrome"` / `"open discord"` | Open desktop app |
| `"search for [topic]"` | Google search |
| `"take a note [text]"` | Save a voice note |
| `"read my notes"` | Read back notes |
| `"lock my pc"` | Lock computer |
| `"shutdown pc"` | Shutdown computer |
| `"what's playing"` | Current song info |
| `"what did I set last"` | Recall memory |
| `"tell me a joke"` | Friday tells a joke |
| `"roast me"` | Friday roasts you 😂 |
| `"Friday shutdown"` | Exit Friday |

---

## 🤖 Telegram Bot Commands

| Command | Action |
|---|---|
| `lock` | Lock your PC |
| `shutdown` | Shutdown PC |
| `screenshot` | Send PC screenshot |
| `status` | CPU, RAM, battery info |
| `play [song]` | Play music on PC |
| `stop` | Stop music |
| `note [text]` | Save a note |

---

## 📊 Changelog

| Version | Changes |
|---|---|
| 1.0 | Basic voice recognition and TTS |
| 2.0 | Gemini AI brain |
| 3.0 | Custom visual interface |
| 4.0 | Music from computer, YouTube, Spotify |
| 4.1 | Wake word in music mode |
| 5.0 | Smart platform selection |
| 6.0 | Porcupine, Edge TTS, memory, weather, reminders, WhatsApp |
| 7.0 | Ollama local AI, phone bridge, image sharing, ADB app control |
| **8.0** | **Groq AI, Telegram bot, remote access, voice auth, file browser, night mode, voice notes, dashboard** |

---

## 🔮 Upcoming

- 🗣️ ElevenLabs realistic voice (V8.1)
- 🧠 Full personality overhaul (V8.1)
- 📱 PWA phone app (V8.2)

---

## Credits

Built by [Nirupam](https://github.com/YOUR_USERNAME)
Inspired by F.R.I.D.A.Y from the Marvel universe
