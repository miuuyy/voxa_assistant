# Voxa AI — Voice Meets Control

Voxa AI is an **AI-powered voice assistant** that enables people with limited hand mobility to control their entire computer — **precisely, independently, and fully** — using only their voice.  
It’s not a concept or demo — this is a **fully functional, production-ready application** that you can install and start using today.

🔗 **Website:** [https://download-voxa.online/](https://download-voxa.online/)  
🎥 **Video Tutorial:** [YouTube — How to Use Voxa AI](https://www.youtube.com/watch?v=Nz9TFwHUPGk&t=1s)

---

## ✨ Features

- **Click anywhere on screen** using a custom two-step visual recognition grid
- **Natural language understanding** — speak like you normally would
- **Macros & custom actions** — run entire workflows by voice
- **AI-powered UI recognition** using **Gemini 2.5 Flash**
- **Non-smart mode** for manual control without AI
- **Custom themes & settings** for personalization

---

## 🛠 How It Works

Voxa AI runs as a **desktop voice-first agent** with the following tech stack:

- **Python** backend for logic and control
- **Gemini 2.5 Flash** for reasoning and UI analysis
- **PyAutoGUI** for OS-level mouse and keyboard control
- **Google Speech API** for real-time speech recognition

### Dual-Grid Targeting System
1. **Coarse grid overlay** — divides the screen into large sections
2. **Gemini identifies target** — determines which section contains the desired element
3. **Fine grid overlay** — zooms into the section for precise targeting
4. **Pixel-perfect click** — executes the action exactly where needed

This allows cont
