# BusBuddy – Smart Public Transport Assistant
> **"Know Your Bus. Beat the Crowd. Reach on Time."**

---

### Project Identity & Academic Context
* **Project Name:** BusBuddy
* **Tagline:** *"Know Your Bus. Beat the Crowd. Reach on Time."*
* **Course:** B.Tech CSE (AI/ML), Chandigarh University
* **Design Thinking Subject:** Overcrowding & Unpredictability of Public Transport
* **Team:** **Team TechKnights**
* **Team Members:**
  1. **Aagaaz Nanda** — `26BAI70691` (Team Lead,System Architect and Algorithm Design)
  2. **Arpit Sharma** — `26BAI70159` (AI/ML Heuristics)
  3. **Aayan Hashmi** — `26BAI70244` (UI/UX & Design Thinking Researcher)
  4. **Avinash Sharma** — `26BAI70675` (Frontend & State Management)
  5. **Priyanshu Singh** — `26BAI70677` (Data Modeling & Usability Testing)

---

## 1. Problem Statement & Design Thinking Alignment

Based directly on our university project presentation (*Overcrowding & Unpredictability of Public Transport*):

### Commuter Pain Points Addressed:
1. **Severe Overcrowding:** Extreme passenger volume during peak hours (08:00–10:00 AM & 04:00–06:00 PM), footboards packed, uncomfortable and suffocating rides.
2. **Unpredictable Bus Arrival Times:** Absence of reliable live arrival status leading to wasted waiting time.
3. **Boarding vs Waiting Dilemma:** Commuters do not know whether to squeeze into a packed bus or wait for the next one.
4. **Unpredictable Journey Duration:** Traffic congestion at corridor bottlenecks (e.g., Kharar Highway Flyover) causing students to arrive late.
5. **Commuter Anxiety & Stress:** Representative commuter **Meera Nair** (19, B.Tech CSE 1st Year) travelling ~45 minutes to Chandigarh University, feeling anxious about missing lectures or attendance penalties.

---

## 2. Solution Architecture & Key Features

### 🚀 1. Smart Home Dashboard
* Commuter welcome banner customized for **Meera Nair** and daily college route.
* Live ticking synchronized clock with real-time peak-hour commute indicator (`Critical Peak`, `Moderate`, `Off-Peak`).
* Boarding stop selector (Kharar, ISBT 43, Sector 35, Mohali Phase 7, Landran, Desu Majra, CU Gates).
* Real-time ETA countdowns, delay indicators (`+4m late`, `On Time`), and crowd badges (**LOW**, **MEDIUM**, **HIGH**).
* Quick access to **Reach On Time** mini-planner, pinned favourite stops, and recent journeys.

### 🗺️ 2. Interactive Bus Tracking Map
* Interactive Leaflet map centered on the Chandigarh–Mohali–Kharar–Chandigarh University corridor.
* Animated bus markers moving smoothly along real waypoint paths using simulated GPS interpolation.
* Color-coded route polylines reflecting vehicle crowd density (Green = Low, Amber = Medium, Red = High).
* Interactive stop popups with "Set as Boarding Stop" and "Set Destination" controls.
* Bus detail popups with speed (km/h), delay status, audio announcement triggers, and quick comparison shortcuts.

### 👥 3. Smart Crowd Detection & Intelligence System
* 3 clearly categorized crowd states:
  * **LOW (<45%):** Comfortable boarding, guaranteed empty seats.
  * **MEDIUM (45–75%):** Some crowding, limited seating, comfortable standing.
  * **HIGH (>75%):** Severe overcrowding, difficult boarding; recommend alternative bus.
* **Bus Interior Occupancy Schematic:** Visual representation of 36 seating positions and aisle standing areas showing exact passenger distribution.
* **Crowd Alert Subscription Switches:** Set instant alerts when a vehicle exceeds 80% occupancy.
* **Community Crowd Reporting:** Quick reporting of overcrowding, delays, and broken AC.

### 🧠 4. AI-Based Arrival & Crowd Prediction (AI Insights)
* **Explainable AI (XAI) Heuristics:** Transparent multi-feature prediction model built for CSE (AI/ML) demonstration:
  $$\text{Predicted ETA} = \text{Scheduled ETA} + (\beta_1 \cdot \text{BottleneckIndex}) + (\beta_2 \cdot \text{PeakMultiplier}) + \Delta\text{ReportVariance}$$
* Feature impact breakdown: Time-of-Day curve, spatial bottleneck index (Kharar roadworks), and crowdsourced signal velocity.
* **Autonomous Commuter Guidance:** Explains *why* a commuter should wait 5 minutes for Bus 115 rather than boarding packed Bus 204.
* **Future ML Architecture Blueprint:** Outlines edge IoT sensors, Spatio-Temporal Graph Convolutional Networks (ST-GCN), and XGBoost regressors for live enterprise scaling.

### ⚖️ 5. Smart Bus Comparison Matrix
* Side-by-side comparison of 3 to 5 buses simultaneously.
* Metrics evaluated: ETA countdown, Delay status, Crowd occupancy %, Seating chance %, Total travel time, and Coach features.
* **Top Recommendation Badge:** Automatically identifies the optimal trade-off between waiting duration and boarding comfort with plain-English reasoning.

### ⏱️ 6. Smart Journey Planner ("Reach On Time")
* Reverse-calculates optimal departure based on destination deadline (e.g., `09:00 AM` lecture).
* Configurable traffic buffer cushion (5 to 30 minutes).
* Step-by-step travel itinerary with boarding alerts and arrival margin before attendance cutoff.

### 🔔 7. Smart Notification System & Toast Alerts
* Bell drawer with unread counters and priority categories (`High Crowd Spike`, `Traffic Jam Alert`, `Bus Approaching`).
* Demo triggers to simulate crowd surges or delay warnings during university presentations.
* Non-blocking modern toast notifications with Web Audio synthesized chimes.

### 📊 8. Analytics & Trends Dashboard
* 4 interactive Chart.js visualizations connected to dynamic application datasets:
  1. **24-Hour Corridor Crowd Profile** (Line chart with peak rush highlighting).
  2. **Average Route Delays** (Bar chart illustrating Kharar bottleneck impact).
  3. **Fleet Crowd Distribution** (Doughnut chart).
  4. **Weekly Intensity Pattern** (Grouped Bar chart comparing morning rush vs evening student dispersal).
* Dynamic period filtering: *Today*, *Yesterday*, *Weekly*, *Peak Commute*.

### 🧪 9. Design Thinking & User Testing Mode (University Exhibition)
* Full presentation alignment across the 5 Design Thinking stages: **Empathize → Define → Ideate → Prototype → Test**.
* **Interactive Guided Testing Tasks** (from Slide 10):
  * **Task 1:** Find Bus Arrival & Crowd Level.
  * **Task 2:** Compare Nearby Buses.
  * **Task 3:** Reach On Time Planner.
* **Live Stopwatch Runner:** Measures exact task completion duration with confetti celebration.
* **Live Evaluation Form:** Captures Tester Name, Ease-of-Use Rating (1–5 Stars), Task completion status, and Thinking-Aloud observations.
* **Live Aggregated Usability Metrics:** Total evaluations, Average ease rating, System task success rate, and historical observation log persisted in `localStorage`.

### ♿ 10. Accessibility & Extra Innovations
* **Voice Announcements:** Web Speech API integration that speaks arrival times, vehicle numbers, and crowd conditions out loud.
* **High Contrast Mode:** Instant high-contrast accessible color scheme for visually impaired commuters.
* **Dark / Light Theme:** Modern dark SaaS navy palette with smooth light theme toggle.
* **Time Simulator Controller:** Allows evaluators to switch between *8 AM Morning Peak*, *1 PM Off-Peak*, and *5 PM Evening Rush* to observe live algorithmic updates.
* **Emergency Contacts Directory:** Quick access to Chandigarh University Control Room, Transport Office, Women's Helpline (`1091`), and CTU Control Room (`112`).

---

## 3. Project File Structure

```text
busbuddy/
├── index.html                  # Main responsive single-page web application
├── README.md                   # Comprehensive project documentation & guide
├── css/
│   └── styles.css              # Custom styling, glassmorphism, themes & high contrast
└── js/
    ├── data.js                 # Complete Tricity & CU route data, stops, buses & historical stats
    ├── state.js                # Central reactive store & localStorage persistence layer
    ├── crowdAiEngine.js        # AI prediction heuristics, peak weighting & comparison algorithms
    ├── mapModule.js            # Leaflet interactive map, route polylines & simulated GPS tracker
    ├── analyticsModule.js      # Dynamic Chart.js visualizations & period filters
    ├── speechModule.js         # Web Speech API voice announcements & Web Audio chimes
    ├── userTesting.js          # Design Thinking Stage 5 user evaluation runner & metrics
    └── app.js                  # Main controller, event bindings & view orchestration
```

---

## 4. How to Run and Present the Application

No heavy software installations or build tools are required. The application runs in any modern browser:

### Option A: Direct Browser Launch
1. Open File Explorer and navigate to:
   `C:\Users\AAGAAZ NANDA\.gemini\antigravity\scratch\busbuddy`
2. Double-click **`index.html`** to open it in **Google Chrome**, **Microsoft Edge**, or **Brave**.

### Option B: Command Line (PowerShell)
```powershell
cd "C:\Users\AAGAAZ NANDA\.gemini\antigravity\scratch\busbuddy"
Start-Process "index.html"
```

---

## 5. University Presentation & Demonstration Script

Follow this step-by-step walkthrough to give an impressive 5-minute presentation to your evaluators:

1. **Introduction (30s):**
   * State the project identity: *"BusBuddy – Smart Public Transport Assistant"*, built by Team TechKnights for B.Tech CSE (AI/ML) at Chandigarh University.
   * State the problem statement from PPT Slide 01: Public bus overcrowding and unpredictable arrival times causing commuter anxiety (Meera Nair persona).
2. **Dashboard & Crowd Detection (60s):**
   * Show the Smart Dashboard: point out the active boarding stop (Kharar Bus Stand), live countdown timer, and crowd status (**HIGH 86%** on Bus 204 vs **MEDIUM 54%** on Bus 115).
   * Click **"Voice"** on Bus 204 to trigger the Web Speech API announcement out loud.
   * Toggle **"Sim Time"** between **8 AM Peak** and **1 PM Low** to show the live algorithmic adjustment of crowd levels.
3. **Interactive GPS Tracking Map (45s):**
   * Click **"Live Tracking Map"** in the sidebar. Show the animated buses moving along actual routes from Chandigarh ISBT 43 through Kharar to Chandigarh University (Gharuan).
   * Click on any moving bus marker to inspect the popup telemetry and route polyline.
4. **AI Insights & Explainable AI (60s):**
   * Navigate to **"AI Insights & Pred."**.
   * Highlight the mathematical heuristic equation: explain how the time-of-day curve (1.45x peak multiplier) and Kharar spatial bottleneck index (+4 min delay risk) inform the prediction.
   * Showcase the Autonomous Guidance card explaining why waiting 5 minutes for Bus 115 saves 25 minutes of standing fatigue and guarantees arrival before the 9 AM attendance cutoff.
5. **Smart Bus Comparison & Reach On Time (45s):**
   * Open **"Compare Buses"**: review the side-by-side trade-offs and the *TOP RECOMMENDED* badge.
   * Open **"Reach On Time"**: set a 9:00 AM class deadline with a 15-minute buffer; show how the engine reverse-calculates departure at 08:15 AM.
6. **Design Thinking User Testing Mode (60s):**
   * Open **"Design Thinking / Test"**.
   * Explain the 5 stages corresponding to the PPT.
   * Click **"Start Task 1"**: show the evaluation timer running in the top banner. Complete the task, show the confetti effect, and submit an ease-of-use rating (5★).
   * Demonstrate how the testing observations list and SUS metrics update dynamically in LocalStorage.

---

## 6. Transparency on Data & Simulation
* **Simulated Telemetry:** GPS coordinates, vehicle movements, and historical crowd percentages are realistically modeled based on Chandigarh–Kharar–Gharuan corridor geography rather than live government transit APIs.
* **Genuine Functionality:** All UI state management, mathematical heuristic calculations, audio synthesis (Web Speech + Web Audio API), interactive Leaflet map rendering, Chart.js graphs, community reporting, evaluation logging, and LocalStorage persistence are fully implemented and genuinely operational.
