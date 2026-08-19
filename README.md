# Kridsada Bunta

Software Engineer at SNC Former PCL — Rayong, Thailand.
B.Eng. in Mechatronics Engineering, Suranaree University of Technology.

I work on manufacturing systems — MES, production planning, ERP integration, and
IIoT. Most of what I do sits between factory hardware and backend software, so I
spend my time on data pipelines, real-time sync, and making shop-floor systems
talk to each other.

## Tech I use

- **Backend** — NestJS, TypeScript, Python, FastAPI
- **Data** — MongoDB, PostgreSQL, MSSQL
- **Real-time & IIoT** — Socket.io, MQTT
- **AI / CV** — LLM APIs, Whisper, YOLOv8, NVIDIA Jetson

## What I've worked on

Everything below is internal company work, so the code isn't public. Happy to
talk through the design if you're interested.

**Production planning system (MES)**

- Backend for production planning built with NestJS and MongoDB, replacing an
  Excel-based process.
- Scheduling engine mapping material routings to work center capabilities, with
  BOM calculation for stock sufficiency and lead-time offsetting.
- Real-time "plan vs. actual" tracking over WebSockets, plus kiosk displays at
  the machines.
- Role-based access control and an abstract repository layer over the data model.

**SAP integration**

- Sync pipeline pulling purchase orders from SAP (MSSQL) into the MES.
- Raw material validation against BOM before a job is allowed to start.

**Robot cognitive layer**

- Moved the AI processing for Pepper robots off the robot onto an external
  server, since the onboard hardware was too limited.
- Audio pipeline in Python/FastAPI with voice activity detection and noise
  gating, tuned for a noisy factory floor.
- Session storage in NestJS/MongoDB so conversations keep context.

**Warehouse management**

- React dashboard rendering the warehouse layout for pallet tracking.
- Stock tracking down to location / position / lot.
- PostgreSQL advisory locks for serial number generation under concurrent writes.

**IIoT & vision**

- YOLOv8 parts counting in a paint shop, with the output fed into IIoT sensor
  data.
- Defect detection running on Jetson Nano at the edge instead of in the cloud.
- Refrigerant usage tracking over MQTT.
- Machine vision guiding ABB robots for pick & place.

## Repos here

The public repos on this account are mostly side projects and experiments, not
the work above.

## Contact

- LinkedIn — [kridsada-bunta](https://www.linkedin.com/in/kridsada-bunta)
- Email — kridsadabunta@gmail.com
