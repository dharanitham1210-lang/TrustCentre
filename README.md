# TrustCentre
# SIH26245 – AI-Based Real-Time Monitoring of Training Centres

<p align="center">
  <strong>AI-Based Real-Time Monitoring of Training Centres for Attendance and Infrastructure Compliance</strong>
</p>

<p align="center">
  Smart India Hackathon 2026 | Problem Statement: SIH26245
</p>

---

## 📌 About the Project

SIH26245 is an AI-powered real-time monitoring platform designed to help authorities monitor training centres efficiently through digital attendance tracking, infrastructure compliance monitoring, centralized reporting, and data-driven insights.

The platform provides a unified interface for monitoring training centre activities and identifying compliance issues in real time.

It is designed to improve transparency, reduce manual monitoring efforts, and support faster decision-making by administrators and monitoring authorities.

---

## 🎯 Problem Statement

### SIH26245

**AI-Based Real-Time Monitoring of Training Centres for Attendance and Infrastructure Compliance**

Training centres often require regular monitoring to ensure:

- Student attendance compliance
- Infrastructure availability
- Training centre operational status
- Basic facility compliance
- Timely identification of irregularities
- Centralized monitoring and reporting

Traditional manual monitoring can be time-consuming and difficult to scale across multiple centres.

This project proposes a centralized AI-enabled monitoring platform to simplify this process.

---

## 💡 Proposed Solution

Our solution provides a modern web-based monitoring dashboard that enables authorities to:

- Monitor training centre attendance
- Track infrastructure compliance
- View centre-wise monitoring information
- Identify potential compliance issues
- Visualize data through interactive dashboards
- Work with limited or unstable connectivity using offline storage
- Access the application as a Progressive Web App (PWA)
- Analyze Tamil Nadu training-centre data geographically

---

## 🚀 Key Features

### 📊 Real-Time Monitoring

Centralized dashboard for monitoring training centre activities and compliance information.

### 👥 Attendance Monitoring

Track attendance-related information and identify attendance irregularities.

### 🏢 Infrastructure Compliance

Monitor infrastructure and facility-related compliance parameters across training centres.

### 🗺️ Tamil Nadu Map Visualization

Interactive Tamil Nadu map visualization for geographically representing training-centre data.

### 📈 Data Visualization

Interactive charts and visual indicators help administrators understand centre performance and compliance status.

### 🔎 Centre-Level Monitoring

View individual training-centre information and monitor centre-specific compliance details.

### 💾 Offline Support

The application uses IndexedDB for local data persistence, allowing important application data to remain available during temporary connectivity issues.

### 📱 Progressive Web App

The application supports PWA capabilities through Vite PWA and Workbox.

### 🎨 Modern UI

The interface uses a custom glassmorphism-based design system with responsive layouts.

---

# 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │       User          │
                    │ Admin / Authority   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    React 19 UI      │
                    │  TypeScript + Vite  │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
       ┌────────────┐   ┌──────────────┐  ┌─────────────┐
       │  Zustand   │   │   Services   │  │ D3 Map/Data │
       │   Store    │   │   & Utils    │  │ Visualization│
       └──────┬─────┘   └──────────────┘  └─────────────┘
              │
              ▼
       ┌──────────────┐
       │  IndexedDB   │
       │   via idb    │
       └──────────────┘
