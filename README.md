# Flight Monitoring Dashboard

<p align="center">
  <img src="https://github.com/user-attachments/assets/b470b664-d404-4e6d-99a4-3eb3b67978e9" alt="Flight Monitoring Dashboard">
</p>

<p align="center">
  Automated ETL pipeline and real-time dashboard for flight data, built with Python, GitHub Actions, and Supabase.
</p>

<p align="center">

![Status](https://img.shields.io/badge/status-in%20progress-yellow)


</p>

<p align="center">
  <img width="1891" height="677" alt="Interactive route map" src="https://github.com/user-attachments/assets/7d7d103c-9f0d-4278-b678-659c4ac1f580" />
</p>

<p align="center"><i>Interactive route map</i></p>

<p align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-121013?style=for-the-badge&logo=github&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

</p>

<p align="center">
  <b>Click the buttons below to open the project:</b>
</p>

<p align="center">

<a href="https://sn-2026-murilosc.github.io/1-A-A-2Tri-MuriloSouzaC/">
<img src="https://img.shields.io/badge/GitHub%20Pages-Live-blue?style=for-the-badge">
</a>

<a href="https://sirosdashboard.vercel.app/">
<img src="https://img.shields.io/badge/Vercel-Live-black?style=for-the-badge">
</a>

<a href="https://github.com/murilotecoteco/flight-monitoring-dashboard">
<img src="https://img.shields.io/badge/GitHub-Repository-black?style=for-the-badge">
</a>

</p>

---

# Table of Contents

- [About](#about)
- [Screenshots](#screenshots)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Architecture](#architecture)
- [Challenges & Solutions](#challenges--solutions)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Deployment](#deployment)
- [Known Limitations](#known-limitations)
- [Roadmap](#roadmap)
- [License](#license)

---

# About

Flight Monitoring Dashboard automatically collects, processes, stores, and visualizes flight data from Brazil's SIROS/ANAC public API.

The project implements a full ETL pipeline orchestrated by scheduled GitHub Actions workflows, with Python handling extraction and transformation, and Supabase (PostgreSQL) as the persistence layer. The result is a responsive dashboard that stays continuously synchronized with the latest available flight data — no manual updates required.

This project was built to explore how far a serverless, zero-cost stack (GitHub Actions + Supabase free tier) can go in delivering a production-like automated data pipeline.

---

# Screenshots

## Dashboard

![Dashboard](https://github.com/user-attachments/assets/b470b664-d404-4e6d-99a4-3eb3b67978e9)

## Flight Statistics

![Flight Statistics](https://github.com/user-attachments/assets/0e5fc7f4-c5b1-403e-8eba-61ccb7bef068)

## Flight History

![Flight History](https://github.com/user-attachments/assets/d76344e1-79fd-40e5-84bb-cf6b6e6e0638)

## Pipeline

![Pipeline](https://github.com/user-attachments/assets/a6ca3f35-0802-4dcd-9e79-ccda0dbdee92)

---

# Features

- Automated ETL pipeline with scheduled execution
- SIROS/ANAC REST API integration
- Supabase PostgreSQL as the data layer
- Responsive dashboard with airport and airline filtering
- Flight history tracking
- Continuous data synchronization — no manual intervention
- Dual deployment (GitHub Pages + Vercel)

---

# Technology Stack

| Layer | Technology |
| ------ | ---------- |
| Backend | Python 3.12 |
| Automation | GitHub Actions (scheduled workflows) |
| Database | Supabase (PostgreSQL) |
| Frontend | HTML5, CSS3, JavaScript |
| Data Source | SIROS / ANAC API |
| Deployment | GitHub Pages, Vercel |
| Version Control | Git & GitHub |

---

# Architecture

```text
SIROS/ANAC API
       │
       ▼
GitHub Actions
(Scheduled ETL)
       │
       ▼
Python Pipeline
       │
       ▼
Supabase PostgreSQL
       │
       ▼
Web Dashboard
(GitHub Pages / Vercel)
```

The pipeline runs on a schedule via GitHub Actions, fetching flight data from the SIROS/ANAC API, processing it with Python, and persisting it to Supabase PostgreSQL. The dashboard reads from this database and stays in sync automatically, with no server to maintain.

---

# Challenges & Solutions

**Challenge:** Supabase's free tier pauses the database after a period of inactivity, which would break the "always synchronized" premise of the dashboard.

**Solution:** Documented the limitation transparently (see [Known Limitations](#known-limitations)) and outlined two production-ready mitigations: upgrading to a paid tier, or adding a scheduled keep-alive ping as part of the existing GitHub Actions workflow — reusing infrastructure already in place rather than adding a new service.

This reflects a deliberate trade-off: keeping the project fully free-tier while being explicit about what changes in a real production deployment.

---

# Project Structure

```text
flight-monitoring-dashboard/
│
├── .github/
│   └── workflows/
│
├── scripts/
│   └── fetch_flights.py
│
├── sql/
│
├── public/
│
├── index.html
├── style.css
├── script.js
├── requirements.txt
├── schema.sql
└── README.md
```

---

# Getting Started

## Prerequisites

- Python 3.12 or later
- Supabase project
- GitHub account

## Installation

```bash
git clone https://github.com/murilotecoteco/flight-monitoring-dashboard.git
cd flight-monitoring-dashboard
pip install -r requirements.txt
```

Configure the required environment variables and run the data collection script.

---

# Deployment

Live on both:

- GitHub Pages
- Vercel

The ETL pipeline runs automatically via scheduled GitHub Actions workflows, keeping the dashboard synchronized with the latest available flight data.

---

# Known Limitations

- Supabase's free tier automatically pauses the database after a period of inactivity. If the live demo appears unresponsive, the database may need a few seconds to resume, or manual reactivation via the Supabase dashboard.
- In production, this would be mitigated by upgrading to a paid tier or adding a scheduled keep-alive ping to the existing GitHub Actions workflow.

---

# Roadmap

- [x] SIROS/ANAC API integration
- [x] Automated ETL pipeline
- [x] GitHub Actions workflows
- [x] Supabase integration
- [x] Responsive dashboard
- [x] GitHub Pages deployment
- [x] Vercel deployment
- [ ] Interactive charts
- [ ] Airport statistics
- [ ] Advanced search
- [ ] User authentication

---

# License

MIT License — free to use, modify, and distribute.
