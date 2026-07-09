# Flight Monitoring Dashboard

<p align="center">
  <img src="https://github.com/user-attachments/assets/b470b664-d404-4e6d-99a4-3eb3b67978e9" alt="Flight Monitoring Dashboard">
</p>

<p align="center">
  Automated flight monitoring dashboard powered by the SIROS/ANAC API, Supabase and GitHub Actions.
</p>

<p align="center">

![Status](https://img.shields.io/badge/status-completed-brightgreen)
![License](https://img.shields.io/badge/license-none-lightgrey)

</p>

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

<a href="https://github.com/SN-2026-MuriloSC/1-A-A-2Tri-MuriloSouzaC">
<img src="https://img.shields.io/badge/GitHub-Repository-black?style=for-the-badge">
</a>

</p>

---

# Table of Contents

- About
- Why this project
- Screenshots
- Features
- Technology Stack
- Architecture
- Project Structure
- Getting Started
- Deployment
- Roadmap
- License

---

# About

Flight Monitoring Dashboard is a web application that automatically collects, processes, stores and visualizes flight information from the SIROS/ANAC API.

The project implements a complete ETL pipeline using GitHub Actions and Supabase, making flight data continuously available through a responsive web dashboard.

---

# Why this project

This project was built to practice and demonstrate:

- ETL pipeline development
- Python automation
- Scheduled GitHub Actions workflows
- REST API integration
- Cloud database management
- PostgreSQL
- Data visualization
- Automated deployment

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

- Automated ETL pipeline
- Scheduled GitHub Actions workflows
- SIROS/ANAC API integration
- Supabase PostgreSQL database
- Responsive dashboard
- Airport filtering
- Airline filtering
- Flight history
- Automatic data synchronization
- GitHub Pages deployment
- Vercel deployment

---

# Technology Stack

| Layer | Technology |
| ------ | ---------- |
| Backend | Python 3.12 |
| Automation | GitHub Actions |
| Database | Supabase (PostgreSQL) |
| Frontend | HTML5, CSS3, JavaScript |
| API | SIROS / ANAC |
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

The application periodically retrieves flight data from the SIROS/ANAC API through scheduled GitHub Actions workflows. The data is processed using Python, stored in a Supabase PostgreSQL database and displayed through a responsive dashboard deployed on GitHub Pages and Vercel.

---

# Project Structure

```text
flight-monitor-dashboard/
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
git clone https://github.com/SN-2026-MuriloSC/1-A-A-2Tri-MuriloSouzaC.git
```

```bash
cd 1-A-A-2Tri-MuriloSouzaC
```

```bash
pip install -r requirements.txt
```

Configure the required environment variables and execute the data collection script.

---

# Deployment

The application is available on:

- GitHub Pages
- Vercel

The ETL pipeline runs automatically through scheduled GitHub Actions workflows, ensuring that the dashboard remains synchronized with the latest available flight information.

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

This project was developed for educational purposes.

No license has been applied.
