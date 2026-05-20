# CommuteSafe AI Agent

AI-powered transit safety assistant that alerts commuters before they miss their stop — even during GPS failures, tunnel outages, and degraded transit feeds.

---

## Problem Statement

Many commuters fall asleep or lose track of their journey during metro, train, or bus travel. Existing alarm systems fail when:

- GPS becomes inaccurate underground
- Transit feeds go offline
- Networks disconnect
- Routes get delayed or diverted

CommuteSafe solves this problem using a hybrid AI + deterministic architecture.

---

## Features

- Real-time commuter alert system
- AI reasoning for uncertain transit conditions
- GPS degradation handling
- GTFS transit feed integration
- Sleep-risk alert escalation
- Deterministic fallback logic
- Offline-first alarm philosophy
- Failure-tolerant architecture

---

## System Architecture

User Device
↓
Location Engine
↓
Transit Data Service
↓
AI Decision Layer
↓
Notification Engine

---

## Tech Stack

| Technology | Usage |
|---|---|
| FastAPI | Backend API |
| Claude API | AI decision reasoning |
| GTFS-RT | Transit feed data |
| React Native | Mobile application |
| Expo Notifications | Alert delivery |
| Python | Core backend |

---

## AI Agent Responsibilities

The AI agent is only used where deterministic systems become unreliable.

### AI Handles
- GPS signal degradation
- Tunnel scenarios
- ETA uncertainty
- Route diversion detection
- Sleep-mode escalation
- GTFS inconsistencies

### Deterministic Logic Handles
- Stop counting
- GPS polling
- Transit API parsing
- Notification delivery
- Distance calculations

---

## Example AI Input

```json
{
  "gps": {
    "lat": 12.9716,
    "lng": 77.5946,
    "accuracy_m": 18
  },
  "stops_to_destination": 2,
  "gtfs_confidence": 0.4,
  "user_mode": "sleep_declared"
}
