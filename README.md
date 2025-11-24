# 📰 What's New — Automated Daily Tech News Curator
A no-code/low-code automated platform that collects, curates, and presents the day's top tech stories from multiple publications — all in one clean, beautiful interface.

![Status](https://img.shields.io/badge/automation-daily-blue)
![Built With](https://img.shields.io/badge/built%20with-Make.com%20%2B%20Glide-green)
![Status](https://img.shields.io/badge/status-live-brightgreen)

---

## 🌍 Live Demo
👉  **Visit the App:** [What's New (Live App)](https://whats-new-6tdg.glide.page/dl/d0a5f4)


---

## 🚀 Why I Built This
On several mornings, I found myself spending **20–30 minutes** browsing TechCrunch, The Verge, Wired, and other tech sites.  
It was:
- 🔁 Repetitive  
- ⏳ Time-consuming  
- 👀 Easy to miss hidden gems from smaller publications  

So I built **What's New** — a fully automated system that fetches, processes, and displays the day's top technology stories in one place.

---

## 🧠 Project Overview

This project uses:
- **Make.com** → Automation & data collection  
- **Google Sheets** → Lightweight database  
- **Glide** → User-facing web app  
- **News API** → Source of technology headlines  

The end result is a **smooth, daily-updating news dashboard** you can check at a glance.

---

## 🏗️ Architecture
        ┌──────────────────┐
        │  News API (Tech) │
        └───────┬──────────┘
                │ HTTP Request @ 8AM
                ▼
     ┌───────────────────────┐
     │       Make.com        │
     │  - Scheduler          │
     │  - Iterator           │
     │  - Data Formatter     │
     └─────────┬─────────────┘
               │ Writes rows
               ▼
    ┌──────────────────────────┐
    │      Google Sheets       │
    │  (Structured database)   │
    │  title / desc / img /    │
    │  source / url / featured │
    └──────────┬──────────────┘
               │ Sync
               ▼
    ┌──────────────────────────┐
    │         Glide App        │
    │  Clean daily news UI     │
    │  Filters & categories    │
    └──────────────────────────┘

---

## 🔧 How It Works

### **1. Automation & Data Collection (Make.com)**
A scheduled Make.com scenario runs **every morning at 8:00 AM**:

- Triggers a **HTTP GET** to the News API  
- Fetches the top **technology headlines**  
- Uses an **Iterator** module to loop through articles  
- Writes each article into Google Sheets with fields:
  - `title`
  - `description`
  - `source`
  - `url`
  - `image`
  - `publishedAt`
  - `featured` (manual toggle)

#### Example Make.com Data Structure
```json
{
  "title": "Example Tech Headline",
  "description": "A summary of the article...",
  "source": "TechCrunch",
  "url": "https://example.com/story",
  "image": "https://example.com/img.jpg",
  "publishedAt": "2025-01-01T12:00:00Z",
  "featured": "FALSE"
}
```
## Front-End & Presentation (Glide)

**The Glide app:**

- Displays the newest tech articles

- Provides smooth navigation in a card-based layout

- Uses a clean blue theme with subtle shadows

- Includes filtering and categorization options

- Syncs automatically with updated data each morning

### 🧑‍💻 Author

**Caleb Maina**
**Automation  • No-Code • Data Engineering**
