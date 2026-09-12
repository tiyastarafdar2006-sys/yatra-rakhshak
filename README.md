# 🛡️ Yatra Rakshak (यात्रा रक्षक)
### Smart, Safe & Resilient Tourism Intelligence & Emergency Response Platform
> **Smart India Hackathon (SIH 2026)** | **Problem Statement ID:** `SIH26204`  
> **Category:** `SW 72` | **Team:** `Data Drifters`

[![SIH 2026](https://img.shields.io/badge/SIH-2026-orange.svg?style=for-the-badge&logo=india)](https://www.sih.gov.in/)
[![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)](https://fastapi.tiangolo.com/)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=threedotjs&logoColor=white)](https://threejs.org/)
[![Leaflet](https://img.shields.io/badge/Leaflet-199900?style=for-the-badge&logo=leaflet&logoColor=white)](https://leafletjs.com/)
[![PWA Ready](https://img.shields.io/badge/PWA-Ready-blueviolet.svg?style=for-the-badge&logo=pwa)](https://web.dev/progressive-web-apps/)

---

## 📌 Executive Summary

**Yatra Rakshak** is a comprehensive, AI-powered pilgrimage and smart tourism safety ecosystem engineered specifically for India's diverse terrains—from high-altitude Himalayan treks (Kedarnath, Amarnath) to heritage cultural corridors (Jaipur, Varanasi, Hampi, Agra). 

It seamlessly combines **real-time disaster intelligence (NDMA Sachet CAP alerts & Open-Meteo hazard radars)**, **interactive GIS corridor mapping (Leaflet.js & CARTO Voyager)**, **dynamic multi-tab trip context synchronization**, **3D WebGL procedural digital twins with 12 Indian regional language audio lore**, **instant 112 ERSS / 108 EMS emergency dispatch grids with ABHA ID tracking**, and **offline-first PWA survivability**.

---

## 🌟 What Makes Yatra Rakshak Unique?

```
                                  YATRA RAKSHAK
                                        │
     ┌──────────────────┬───────────────┴───────────────┬──────────────────┐
     ▼                  ▼                               ▼                  ▼
🧠 AI Safe Plan    🗺️ GIS Corridor Map             🏛️ 3D Digital Twin   🆘 112/108 SOS
Day-by-Day Route    Leaflet.js + Live Hazards      WebGL Procedural      ABHA ID Linkage
NDMA Risk Radar     108 Trauma Center Pins         12 Indian Languages   Acoustic Siren
Weather & Altitude  Safe Evacuation Polylines      Time-of-Day Lighting  Live GPS Dispatch
```

---

## 🚀 Key Modules & Capabilities

### 1. ⚡ One-Click Popular Indian Circuits & GenAI Planner
- **Curated High-Value Circuits**: Instant 1-click loading for **Jaipur** (Golden Triangle), **Varanasi** (Spiritual Moksha), **Hampi** (Vijayanagara Heritage), **Agra** (Mughal Grandeur), and **Kedarnath** (High-Altitude Sacred Trek).
- **Autonomous Safety Scorer**: Weather-adjusted scheduling, crowd density predictions, altitude acclimatization checkpoints, and carbon eco-scores.
- **Dynamic Context Synchronization**: Selecting any destination automatically syncs data across all sub-modules (Transit, Stays, Satvik Dining, 3D Lore, and SafeRoute Map).

### 2. 🗺️ Interactive GIS Corridor & Hazard Avoidance Mapping
- **Leaflet.js & CARTO Voyager**: Smooth vector-styled interactive maps embedded directly in the planning and safety views.
- **Disaster Hazard Overlay**: Visual representation of active NDMA flood/landslide danger zones with dynamic rerouting around red-flagged corridors.
- **Emergency Infrastructure Pins**: Real-time rendering of nearest 108 Emergency Medical Trauma Centers, Police checkposts, and mountain rescue stations along the selected route.

### 3. 🏛️ 3D Procedural WebGL Digital Twins
- **Interactive 3D Monument Models**: Procedurally rendered architectural twins of iconic monuments (Taj Mahal, Hawa Mahal, Qutub Minar, Kedarnath Temple, Virupaksha).
- **Real-Time Lighting & Shaders**: Dynamic simulation of *Dawn*, *Golden Hour*, *Noon Sun*, and *Cyber Night* lighting with wireframe engineering modes.
- **Multilingual Web Speech Audio Guides**: Native speech synthesis narration across **12 Scheduled Indian Languages**:
  `English`, `Hindi (हिन्दी)`, `Bengali (বাংলা)`, `Telugu (తెలుగు)`, `Marathi (मराठी)`, `Tamil (தமிழ்)`, `Gujarati (ગુજરાતી)`, `Urdu (اردو)`, `Kannada (ಕನ್ನಡ)`, `Odia (ଓଡ଼ିଆ)`, `Malayalam (മലയാളം)`, and `Punjabi (ਪੰਜਾਬੀ)`.

### 4. 🚆 End-to-End Pilgrimage Services Matrix
- **Verified Transit**: IRCTC Vande Bharat Express, electric eco-shuttles, authorized local taxis, and high-altitude pony/palanquin bookings.
- **Verified Safe Stays**: Safety-certified dharamsalas, heritage havelis, and eco-resorts with 24/7 CCTV, women-safety compliance, and ABHA medical tie-ups.
- **Satvik & Hygienic Dining**: FSSAI Clean Street Food Hub certified dining spots with safe drinking water audits and pure vegetarian/satvik dietary tags.

### 5. 🆘 Sovereign Emergency Grid & ABHA Health Integration
- **One-Tap Emergency SOS**: Captures high-precision GPS coordinates, altitude, and heading with zero friction.
- **Acoustic Siren Synthesizer**: Generates a high-decibel local alert siren using the Web Audio API for immediate attention in low-visibility situations.
- **112 Police & 108 Ambulance Dispatch**: Dispatches standardized ERSS rescue payloads with embedded **ABHA ID**, blood group, emergency contacts, and active medical conditions.
- **IRDAI Travel Mediclaim Certificate**: Cashless hospital coverage pass generation with 24/7 helpline integration.

### 6. 📱 Offline-First Progressive Web App (PWA)
- Full service worker caching (`sw.js`) and web app manifest (`manifest.json`) enabling zero-connectivity survivability in remote Himalayan valleys.

---

## 🏗️ System Architecture

```mermaid
graph TD
    User([Tourist / Pilgrim / Rescue Authority]) -->|HTTPS / PWA| UI[Frontend Dashboard - index.html]
    
    subgraph Client-Side Layer
        UI -->|PWA Service Worker| SW[sw.js & manifest.json Cache]
        UI -->|3D WebGL Rendering| ThreeJS[Three.js Engine & Shader Controls]
        UI -->|Multilingual Audio Lore| Speech[Web Speech Synthesis API]
        UI -->|Interactive Corridor Maps| Leaflet[Leaflet.js + CARTO Vector Maps]
        UI -->|Acoustic Alarm| WebAudio[Web Audio API Siren Generator]
    end

    subgraph FastAPI Safety Engine (Port 8000)
        UI -->|POST /api/itinerary/generate| PyAPI[safety_api.py]
        UI -->|POST /api/itinerary/analyze| PyAPI
        UI -->|GET /api/heritage/lore| PyAPI
        UI -->|POST /api/emergency/dispatch| PyAPI
        
        PyAPI --> Geo[Open-Meteo Geocoding & Weather]
        PyAPI --> NDMA[NDMA Sachet CAP Hazard Engine]
        PyAPI --> AIPlanner[GenAI Multi-Day Itinerary Engine]
        PyAPI --> LoreRegistry[12-Language Cultural Lore Store]
        PyAPI --> ERSS[112 ERSS / 108 EMS Dispatch Formatter]
    end

    subgraph Express Backend API (Port 5000)
        UI -->|POST /api/register| NodeAPI[server.js]
        UI -->|POST /api/login| NodeAPI
        UI -->|POST /api/bookings| NodeAPI
        
        NodeAPI --> Auth[Bcrypt Authentication & ABHA Linking]
        NodeAPI --> Booking[Universal Escrow & GST Breakdown]
        NodeAPI --> DB[(PostgreSQL / High-Availability Memory DB)]
    end
```

---

## 📂 Repository Structure

```
.
├── index.html            # Unified Single-Page Application (Tailwind, Leaflet, Three.js)
├── safety_api.py         # Python FastAPI Safety, Weather, NDMA CAP & AI Engine
├── server.js             # Node.js Express Authentication, Booking & Mediclaim Server
├── sw.js                 # PWA Service Worker for offline asset caching
├── manifest.json         # Progressive Web App configuration & install badges
├── package.json          # Node.js project manifest & execution scripts
├── requirements.txt      # Python dependencies (FastAPI, Uvicorn, Requests, Pydantic)
├── README.md             # Project Documentation & Jury Guide
└── .venv/                # Python Virtual Environment
```

---

## 🛠️ Installation & Setup Guide

### 📋 Prerequisites
- **Node.js**: v18.0 or newer
- **Python**: v3.10 or newer (with `pip` and `venv`)
- **Web Browser**: Modern Chromium, Firefox, or Safari browser with WebGL & Geolocation support.

---

### 1️⃣ Clone & Setup Dependencies

#### Windows (PowerShell):
```powershell
# Clone the repository
git clone https://github.com/your-username/yatra-rakshak.git
cd yatra-rakshak

# Install Node.js dependencies
npm install

# Create & activate Python virtual environment
python -m venv .venv
.\.venv\Scripts\Activate.ps1

# Install Python dependencies
pip install -r requirements.txt
```

#### Linux / macOS (Bash):
```bash
# Clone the repository
git clone https://github.com/your-username/yatra-rakshak.git
cd yatra-rakshak

# Install Node.js dependencies
npm install

# Create & activate Python virtual environment
python3 -m venv .venv
source .venv/bin/activate

# Install Python dependencies
pip install -r requirements.txt
```

---

### 2️⃣ Start All Services

Open 3 separate terminal tabs or use your preferred process runner:

#### Terminal 1: Node.js Express Backend
```powershell
npm run start:api
# Running on http://localhost:5000
```

#### Terminal 2: FastAPI Safety & AI Engine
```powershell
npm run start:safety
# Running on http://localhost:8000 (Interactive docs at http://localhost:8000/docs)
```

#### Terminal 3: Web Server / Frontend
```powershell
npm run start:web
# Accessible at http://localhost:3000
```

---

## 📡 API Reference

### 🛡️ Safety & AI Engine (`http://localhost:8000`)

| Endpoint | Method | Description |
| :--- | :---: | :--- |
| `/api/itinerary/generate` | `POST` | Synthesizes an AI day-by-day safety itinerary with weather, crowd index, and altitude tips. |
| `/api/itinerary/analyze` | `POST` | Fetches live Open-Meteo forecasts and scores multi-hazard NDMA risk levels. |
| `/api/heritage/lore` | `GET` | Returns verified historical lore and narration scripts in any of 12 Indian languages. |
| `/api/emergency/dispatch` | `POST` | Formats and transmits a 112 Police / 108 Medical incident with GPS and ABHA metadata. |
| `/docs` | `GET` | Swagger / OpenAPI interactive API explorer. |

#### Sample Request: AI Itinerary Generation
```json
POST /api/itinerary/generate
{
  "origin": "Haridwar",
  "destination": "Kedarnath",
  "days": 4,
  "travelers": 2,
  "travel_style": "pilgrimage",
  "fitness_level": "moderate"
}
```

---

### 💳 Core Backend API (`http://localhost:5000`)

| Endpoint | Method | Description |
| :--- | :---: | :--- |
| `/api/register` | `POST` | Register a new tourist profile with email, phone, and password. |
| `/api/login` | `POST` | Authenticate and retrieve user profile with pre-linked ABHA ID and blood group. |
| `/api/bookings` | `POST` | Book a package, calculate 18% GST + Green Cess, and issue an IRDAI Mediclaim certificate. |
| `/api/test` | `GET` | Health check reporting database and system status. |

---

## 🎯 Jury Demonstration Walkthrough (3-Minute Script)

1. **Quick Destination Selection & Dynamic Tab Sync**:
   - Open `http://localhost:3000`.
   - On the **Explore Destinations** section, click **"Kedarnath"** or **"Varanasi"**.
   - Notice how the entire app dynamically aligns: Transport shows Vande Bharat / Shuttles, Stays shows certified havelis/ashrams, Food shows Satvik dining spots, and 3D Lore loads the respective monument.

2. **AI Safe Itinerary with Live GIS Map**:
   - Click the **"Plan Trip"** tab.
   - Click **"Generate AI Safe Itinerary"**.
   - Review the day-by-day acclimatization schedule, NDMA weather risk score, and inspect the interactive **Leaflet.js route map** with 108 emergency pins.

3. **3D WebGL Digital Twin & 12 Indian Languages**:
   - Switch to the **"Heritage 3D"** tab.
   - Rotate, zoom, and inspect the 3D procedural monument.
   - Toggle lighting to **"Golden Hour"** or **"Cyber Night"**.
   - Switch language to **Hindi**, **Bengali**, or **Tamil** and click **"Play Audio Guide"** to hear authentic Indian speech synthesis.

4. **Universal Escrow Booking & IRDAI Mediclaim**:
   - Navigate to **"Stays"** or packages, click **"Book Now"**.
   - Preview the transparent pricing (Base + GST + Green Eco-Cess) and complete mock UPI checkout.
   - View the generated **IRDAI Travel Mediclaim Certificate** with ₹5,00,000 cashless insurance coverage.

5. **One-Tap 112 / 108 Emergency SOS Drill**:
   - Click the red **"SOS"** button on the navbar or navigate to **"SafeRoute"**.
   - Click **"TRIGGER ONE-TAP SOS RESCUE"**.
   - Hear the simulated acoustic siren, view the exact GPS coordinates and altitude, and observe the live dispatch confirmation linked to the user's **ABHA Health ID (O+ Blood Group)**.

---

## ⚖️ Tech Stack Matrix

| Area | Technologies Used |
| :--- | :--- |
| **Frontend UI** | HTML5, CSS3, Tailwind CSS, Lucide Icons, Vanilla JavaScript |
| **3D Graphics & WebGL** | Three.js (r128), OrbitControls, Procedural Geometry Engine |
| **Mapping & GIS** | Leaflet.js, CARTO Voyager Vector Tiles, OpenStreetMap Geocoding |
| **Speech & Multimodal** | Web Speech Synthesis API (12 Regional Indian Locales), Web Audio API |
| **Safety Engine** | Python 3.10+, FastAPI, Uvicorn, Open-Meteo REST API, NDMA Sachet CAP parser |
| **Backend & Escrow** | Node.js, Express.js, Bcrypt.js, CORS, PostgreSQL with In-Memory fallback |
| **Offline & PWA** | Service Workers (`sw.js`), Web App Manifest (`manifest.json`) |

---

## 👥 Team Data Drifters
- **Smart India Hackathon (SIH 2026)**
- **Theme:** Travel & Tourism / Disaster Resilient Infrastructure

---
*Built with ❤️ for a safer, smarter, and resilient Bharat.*
