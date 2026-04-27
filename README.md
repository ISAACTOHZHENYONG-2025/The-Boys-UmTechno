# The-Boys-UmTechno
 
# Concept A — SejukAI

**Predictive AC Retrofit for Tropical Homes**

---

## One-liner

A clip-on device that turns any existing AC into a thermally-aware AI controller, cutting AC bills 25–40% without replacing a single appliance.

---

## The Angle

Most "smart AC" products are **reactive** — turn off when nobody's home.

**SejukAI is predictive:**

- Learns your room's thermal mass
- Uses tomorrow's weather forecast + your schedule + the AC's efficiency curve
- Pre-cools optimally so you walk into a 24°C room without the AC blasting at full power for 90 minutes
- Detects overcooling (room at 19°C when 24°C is comfortable) and corrects
- Schedules around tiered TNB residential tariffs

---

## Hardware

| Component | Purpose |
|---|---|
| ESP32 | Microcontroller / brain |
| IR blaster | Controls any existing AC remote-style |
| DHT22 | Temperature + humidity sensing |
| PIR or mmWave sensor | Occupancy detection |

**BOM:** ~RM40

---

## Software

- **Edge ML model** — lightweight LSTM or learned controller running on-device
- **Companion app** — schedule, savings dashboard, RM + kg CO2 tracking

---

## Rubric Scoring (Predicted)

| # | Criterion | Weight | Predicted | Reasoning |
|---|---|---|---|---|
| 1 | Applicability | 10% | **Excellent** | Directly attacks the largest waste source in tropical residential |
| 2 | Innovation | 10% | Good | Predictive thermal modeling is novel for consumer retrofit |
| 3 | Sustainability | 10% | **Excellent** | RM40 BOM, retrofit, scales to PPR/B40 |
| 4 | Feasibility | 10% | **Excellent** | Every component is off-the-shelf |
| 5 | Technical Aspects | 20% | **Excellent** | If we show the ML pipeline, thermal model, control logic clearly |
| 6 | Stakeholder / Ethics | 10% | Good | Privacy-preserving (edge), inclusive (low cost) |
| 7 | Urgency | 10% | **Excellent** | TNB tariff hikes 2024–25 are politically hot |
| 8 | Clarity (video) | 10% | TBD | Depends on execution |
| 9 | Formatting & Creativity | 10% | TBD | Depends on execution |

---

## Where This Loses

"Smart AC controller" is a saturated product category. **Sensibo, Tado, Ambi Climate already exist.**

We need to be crystal clear on what's different:

- **Predictive thermal modeling** (not reactive)
- **Malaysian tariff awareness** (TNB tiered residential)
- **Price point** (RM40 BOM vs RM500+ competitors)

### Q&A Landmine

> *"How is this different from Sensibo?"*

Need a sharp answer. Probably:

> *"Sensibo is designed for temperate climates with binary heat/cool modes and flat tariffs. Malaysia is 32°C year-round, AC runs 8+ hrs/day, and our tariff is tiered. The optimization problem is fundamentally different — and nobody's serving the M40/B40 segment at this price point with Bahasa Malaysia UI and TNB tariff awareness."*

