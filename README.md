⛅ WeatherGPT
Conversational AI for Weather Forecasting, Alerts, and Climate Information
Built for Smart India Hackathon 2026 — Problem Statement ID: 26068
Organization: Ministry of Earth Sciences (MoES) · Department: India Meteorological Department (IMD)
Theme: Disaster Management · Category: Software
---
📝 Problem Statement
Weather information is often distributed through multiple portals, bulletins, satellite products, and forecast systems, making it difficult for common users, researchers, disaster managers, and government agencies to quickly obtain actionable weather information. WeatherGPT solves this by providing a single conversational interface where users can ask natural-language questions about weather, forecasts, alerts, and climate.
✨ Features
Conversational interface — ask weather questions in plain English
Live data — powered by the free Open-Meteo API (no API key required)
Intent detection — understands queries about temperature, rain, humidity, wind, UV, sunrise/sunset, forecasts, and alerts
Place extraction — automatically detects city names from your question
7-day forecast — daily weather breakdown
Weather alerts — heat wave, heavy rain, thunderstorm, fog, high wind, and extreme UV warnings
Climate information — seasonal context for any location
Responsive design — works on desktop and mobile browsers
🚀 Quick Start (Run on Your Desktop)
Option 1: Double-click (Easiest)
Download `WeatherGPT.html`
Double-click the file — it opens in your default browser
Start asking weather questions!
Option 2: Using a local server (recommended)
A local server avoids browser CORS/security prompts.
Using Python (pre-installed on most systems):
```bash
# Python 3
python -m http.server 8000

# Then open http://localhost:8000/WeatherGPT.html in your browser
```
Using Node.js:
```bash
npx serve .
```
Using VS Code:
Install the "Live Server" extension
Right-click `WeatherGPT.html` → "Open with Live Server"
🔧 How It Works
```
User Question
    │
    ▼
┌─────────────┐     ┌──────────────────┐     ┌────────────────┐
│  NLP Parser  │────▶│  Geocoding API   │────▶│ Forecast API   │
│ (intent +    │     │ (city → lat/lon) │     │ (Open-Meteo)   │
│  place)      │     └──────────────────┘     └────────────────┘
└─────────────┘                                       │
    │                                                  ▼
    ▼                                      ┌───────────────────┐
┌─────────────┐                            │ Response Builder  │
│ Intent Match│──────────────────────────▶ │ (formats answer)  │
└─────────────┘                            └───────────────────┘
```
Parse Query — extracts the user's intent (weather, rain, alerts, etc.) and the place name
Geocode — converts the place name to latitude/longitude via Open-Meteo Geocoding API
Fetch Forecast — gets current conditions, hourly, and 7-day forecast data
Detect Alerts — checks for heat waves, heavy rain, thunderstorms, high winds, extreme UV
Build Response — formats a conversational answer with metrics and warnings
🗣️ Example Questions
"What's the weather in Delhi?"
"Will it rain tomorrow in Mumbai?"
"7-day forecast for Chennai"
"Any weather alerts in Kolkata?"
"Humidity in Bengaluru right now"
"Wind speed in Jaipur"
"Sunrise time in Varanasi"
"UV index in Goa"
🌐 Data Sources
Open-Meteo Forecast API — `https://api.open-meteo.com/v1/forecast`
Open-Meteo Geocoding API — `https://geocoding-api.open-meteo.com/v1/search`
WMO Weather Codes — standard weather interpretation codes
No API key is required. The Open-Meteo API is free for non-commercial use.
📂 Project Structure
```
WeatherGPT/
├── WeatherGPT.html    # Main application (single-file, self-contained)
└── README.md          # This file
```
🛠️ Tech Stack
HTML5 — structure
CSS3 — styling (dark theme, responsive)
Vanilla JavaScript — NLP parsing, API calls, DOM rendering
Open-Meteo API — weather data
No frameworks, no build tools, no dependencies
📤 Adding to Your GitHub Repository
```bash
# 1. Create a new repo on GitHub (e.g., WeatherGPT)

# 2. Clone it locally
git clone https://github.com/<your-username>/WeatherGPT.git
cd WeatherGPT

# 3. Copy the files in
cp /path/to/WeatherGPT.html .
cp /path/to/README.md .

# 4. Stage, commit, and push
git add .
git commit -m "Add WeatherGPT — conversational AI weather tool (SIH 2026)"
git branch -M main
git push -u origin main
```
Optional: Enable GitHub Pages
Go to your repo → Settings → Pages
Source: Deploy from a branch → main → / (root)
Save — your app will be live at `https://<your-username>.github.io/WeatherGPT/WeatherGPT.html`
🗺️ Roadmap / Future Enhancements
[ ] Integrate IMD's official bulletin & cyclone warning feeds
[ ] Add Indian language support (Hindi, Tamil, Bengali, etc.)
[ ] Voice input/output
[ ] Disaster manager dashboard with map overlays
[ ] Historical climate data queries
[ ] Push notification alerts for subscribed locations
[ ] Integration with LLM for more natural conversations
📄 License
This project is built for the Smart India Hackathon 2026. Open-Meteo data is licensed under CC BY 4.0.
---
Built for SIH 2026 · Ministry of Earth Sciences · India Meteorological Department
