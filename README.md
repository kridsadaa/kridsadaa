# Kridsada Bunta

Software Engineer at SNC Former PCL — Rayong, Thailand.
B.Eng. in Mechatronics Engineering, Suranaree University of Technology.

I work on manufacturing systems — MES, production planning, warehouse, and
machine vision. Most of what I do sits between factory hardware and backend
software, so I spend my time on data pipelines, real-time sync, and making
shop-floor systems talk to each other.

## Tech I use

- **Backend** — NestJS, TypeScript, Python, FastAPI, Express
- **Frontend** — React, Vite, Tailwind CSS
- **Data** — MongoDB, PostgreSQL, MSSQL
- **Real-time & industrial** — Socket.io, SAP integration, IIoT sensors, KEBA machine data
- **AI / CV** — YOLO (v5/v8/v11), OpenCV, NVIDIA Jetson, LLM APIs, Whisper

## My own projects

These are the ones you can actually read the code for.

### [auto-bot](https://github.com/kridsadaa/auto-bot) — visual automation for SAP and desktop apps

Open source (MIT). Automates repetitive work in SAP GUI, browsers, and Windows
apps that have no API to call.

- Targets elements two ways — image matching and Windows UI Automation selectors
  — so steps don't break when resolution, theme, or zoom changes.
- GUI sequence editor with nested branching, variables, and states, so loops are
  built without hand-editing config.
- Live debugger: on a failed step the bot pauses and offers retry, skip,
  restart-row, re-capture, or injecting a recovery command and continuing.
- Reads `.xlsx`/`.csv` as data source and writes results straight back.
- Runs entirely on the local machine — nothing goes to the cloud, so IT can audit it.

### [tuner-free](https://github.com/kridsadaa/tuner-free) — online instrument tuner

Live at [tuner-free.kridsada-bun.com](https://tuner-free.kridsada-bun.com/). No ads,
no sign-up, all audio processed in the browser.

- Real-time pitch detection over the Web Audio API, with a canvas history graph
  showing note stability rather than one instantaneous reading.
- Tuning presets for Thai instruments — ซออู้, ซอด้วง, ซอสามสาย, จะเข้, พิณ, กระจับปี่ —
  plus guitar, orchestral strings, ukulele, mandolin, banjo.
- Installable PWA that works offline, with prerendered per-instrument pages.

## Work projects

Mostly internal, so only parts of it are public — the label printing service and
the planning frontend are up here. Happy to talk through the design of the rest.

### MES — production digitization

- Sync pipeline with SAP (MSSQL) for purchase orders and BOMs, with raw material
  validation before a job can start.
- Shift-aware production dating and machine interlocking against counter capacity.
- Distributed label printing — generation, queuing, audit, co-product labels,
  reprint tracking — through a Python print service
  ([repo](https://github.com/kridsadaa/SNC-B8_MES_MSA-Print-Label)).
- Inventory by location / position / lot, with aggregation pipelines behind stock
  movement and OEE reporting.

### PPS — production planning and APS

- Scheduling engine mapping material routings to work center capabilities, with a
  multi-material BOM calculator for stock sufficiency and lead-time offsetting.
- NestJS backend on an abstract repository pattern, with RBAC and a global
  audit-log interceptor.
- Machine status broadcast over Socket.io, including a kiosk API for
  machine-side displays ([frontend](https://github.com/kridsadaa/Production-Planning-System-FE)).

### IMM-Analytics — vision QC for injection molding

- YOLOv8/v11 pipeline detecting flash, short shot, and sink mark inline with the
  machine cycle.
- Ingests high-frequency data from KEBA machines and correlates it with the
  vision results to suggest parameter adjustments.
- Frame-differencing and multi-threading to keep it stable on edge hardware, plus
  a camera sleep/wake cycle tied to machine idle time.

### Smart WMS

- React digital-twin warehouse layout for pallet tracking, with live inventory
  events over Socket.io.
- PostgreSQL advisory locks for serial number generation under concurrent writes.
- Batch sync of stock movements back to SAP.

### Robot cognitive layer

- Moved AI processing for Pepper robots onto an external server, since the
  on-board hardware was too limited.
- Audio pipeline in Python/FastAPI with voice activity detection, noise gating,
  and bandpass filtering for a noisy factory floor.
- WebSocket bridge between FastAPI/Python 3 and the robot's NAOqi/Python 2.7
  middleware.

### IIoT & vision

- YOLOv8 parts counting on a paint shop conveyor, fed into IIoT sensor data.
- YOLOv5 defect detection on Jetson Nano, running at the edge.
- QR verification checkpoint that locks the order on a label/shipping mismatch.
- Refrigerant usage tracking backend and a durian orchard sensor station.

## Contact

- LinkedIn — [kridsada-bunta](https://www.linkedin.com/in/kridsada-bunta)
- Email — kridsadabunta@gmail.com
