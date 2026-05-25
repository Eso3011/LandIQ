# LandIQ

> Soil health intelligence for Nigerian agricultural land  
> Women Techsters Fellowship 2026 · Group 32 · Paragon Squad · SDG 15: Life on Land

---

## What Is LandIQ?

LandIQ is a mobile application that gives farmers and agricultural SMEs in Nigeria an instant, standardized soil health rating for any GPS location — before they commit financial resources to land acquisition or lease.

Users input GPS coordinates and receive a **Gold, Silver, or Bronze** badge, a score out of 100, a degradation risk level (Low, Medium, or High), and a plain-English explanation — delivered in seconds, without needing an expert consultation.

Built by a 17-member multidisciplinary team across seven tracks as a capstone project under the Women Techsters Fellowship 2026.

---

## The Problem

Agricultural land is bought, leased, and allocated across Nigeria every day — mostly based on surface appearance, word-of-mouth, or incomplete historical knowledge. Professional soil testing is expensive, inaccessible, and written in technical language most farmers cannot interpret.

Soil degradation develops gradually and is often invisible until productivity collapses. LandIQ makes soil health visible and comparable at the exact point of land decision-making.

---

## Live Demo

| Resource | Link |
|---|---|
| Backend API (Live) | https://backendlandiq.onrender.com |
| Backend Health Check | https://backendlandiq.onrender.com/health |
| UI Design (Figma) | [Full UI Designs](https://www.figma.com/design/WqpkFKfAbpfxM34FmtW5so/ProductDesign-Team?node-id=0-1) |

---

## Core Features

**Soil Health Scoring** — Five indicators evaluated using FAO and IITA scientific frameworks, producing a score out of 100 mapped to Gold (70–100), Silver (45–69), or Bronze (0–44).

**Degradation Risk Assessment** — Beyond the badge, LandIQ tells users whether the land is at risk of getting worse over time: Low, Medium, or High risk based on slope, drainage, pH, and soil depth factors.

**Plain-English Explanation** — Every result includes an automatically generated explanation that any user can understand and act on, with no soil science knowledge required.

**Land Comparison** — Users can compare 2–3 farm locations side-by-side and identify the best option for their needs.

**Saved Assessments** — Assessment reports are saved to the user's dashboard, searchable and filterable by state or badge type.

---

## AI Implementation

LandIQ uses a **two-layer AI system**:

**Layer 1 — Rule-Based Expert System (Data Science)**  
A classical AI scoring engine that captures FAO agronomist and IITA soil scientist knowledge, applies weighted rules across five soil indicators, and produces interpretable scores with zero latency and zero external cost. Built on the Nigerian Soil Survey (2017), covering 658 national soil mapping units.

**Layer 2 — HuggingFace Mistral-7B-Instruct (Backend)**  
Generates extended natural language explanations asynchronously in the background, structured across five sections: verdict, practical interpretation, risk factors, improvement recommendations, and optimal agricultural use suggestions.

---

## Scoring Algorithm

| Indicator | Max Points | Weight | Scientific Basis |
|---|---|---|---|
| Suitability | 40 pts | 40% | FAO primary land evaluation criterion |
| pH Level | 20 pts | 20% | IITA: primary yield-limiting factor in Nigeria |
| Drainage | 20 pts | 20% | IITA: primary yield-limiting factor in Nigeria |
| Slope | 10 pts | 10% | Long-term sustainability — gradual erosion impact |
| Soil Depth | 10 pts | 10% | Root development — partially manageable |

Badge thresholds align with FAO Land Suitability Classes. The algorithm was calibrated to IITA guidelines for tropical Nigerian crops after initial thresholds (set for temperate crops) produced only 11 Gold zones (1.7%). Recalibration brought Gold zones to 87 (13.2%) — correctly within FAO benchmarks.

---

## Technology Stack

### Mobile (Frontend)
| Technology | Role |
|---|---|
| Flutter (Dart) | Cross-platform mobile app (Android + iOS) |
| Riverpod | State management |
| GoRouter | Navigation and routing |
| Dio | HTTP networking client |

### Backend
| Technology | Role |
|---|---|
| Node.js / Express | REST API server |
| MySQL 8.0 / Sequelize | Database and ORM |
| Turf.js | Point-in-polygon geospatial lookups |
| JWT / bcryptjs | Authentication and security |
| HuggingFace (Mistral-7B) | AI explanation generation |

### Infrastructure
| Platform | Role |
|---|---|
| Railway | MySQL database hosting |
| Render | Backend API deployment |

### Data Science
| Tool | Role |
|---|---|
| Python + shapefile library | Shapefile to GeoJSON conversion |
| Nigerian Soil Survey (2017) | Primary dataset — 658 soil mapping units |

---

## Test Results

| Location | Latitude | Longitude | Badge | Score | Risk |
|---|---|---|---|---|---|
| Abuja (FCT) | 9.0820 | 7.5324 | Silver | 48 | HIGH |
| Kano | 11.9964 | 8.5211 | Silver | 68 | MEDIUM |

---

## Track Repositories

| Track | Repository |
|---|---|
| 📊 Data Science | [landiq-data-science](https://github.com/fawziyyahk/landiq-data-science) |
| 📱 Mobile (Flutter) | [landiq](https://github.com/Rolalove/landiq) |
| 🔧 Backend API | Live at https://backendlandiq.onrender.com |

---

## SDG Alignment

LandIQ directly supports **SDG 15 — Life on Land** by making soil quality visible and economically relevant during land acquisition and leasing decisions. By discouraging investment in degraded land and promoting sustainable land management, LandIQ contributes to the protection, restoration, and sustainable use of terrestrial ecosystems across Nigeria.

---

## Future Improvements

- Multi-language support in Yoruba, Igbo, and Hausa
- Satellite imagery integration using NDVI and remote sensing APIs
- PDF report export for professional and cooperative users
- Government and NGO dashboard for land productivity planning
- Premium subscription model with advanced analytics
- Google Play Store and App Store deployment

---

## Project Context

| Detail | Value |
|---|---|
| Programme | Women Techsters Fellowship 2026 |
| Track | Data Science and Engineering |
| Group | 32 — Paragon Squad |
| Team Size | 17 members across 7 tracks |
| SDG Alignment | SDG 15: Life on Land |
| Submission Date | 27th February 2026 |
