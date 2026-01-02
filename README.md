# 🔐 Trust Factor MVP

**A Dynamo-style Trust Scoring & Guardrails Prototype**

**Trust Factor MVP** is a fully client-side prototype that demonstrates how **trust scoring, banding, and enforcement** can be used to manage user behavior in AI systems.

It simulates assigning each actor a **dynamic trust score**, mapping them into **Green / Yellow / Red bands**, and automatically adjusting enforcement behavior (checks, throttling, logging) based on observed events.

This project is intentionally lightweight and visual—designed for **concept validation, demos, and architectural discussion**, not production deployment.

---

## 🧠 What This Demonstrates

* **Trust scores with memory** (scores persist and evolve over time)
* **Banding logic** (Green / Yellow / Red)
* **Automatic enforcement switching** based on band
* **Real-time observability** via tables, stats, and event logs

All logic runs locally in the browser using plain HTML, CSS, and JavaScript.

---

## 🧩 Core Concepts

### Trust Scoring

Each actor starts with a score between **0–100**. Events adjust the score immediately:

* Clean behavior → score increases
* Violations → score decreases (severity-based)

### Trust Bands

| Band      | Score Range | Meaning                       |
| --------- | ----------- | ----------------------------- |
| 🟢 Green  | 85–100      | Trusted, low friction         |
| 🟡 Yellow | 50–84       | Default scrutiny              |
| 🔴 Red    | 0–49        | High risk, strict enforcement |

### Enforcement Logic

* **Green:** higher throughput, lighter checks
* **Yellow:** default checks and thresholds
* **Red:** strict validation, throttling, heavy logging

---

## 🧪 What You Can Simulate

* Prompt injection or policy violations
* Medium vs high severity events
* Clean usage days
* Real-time band transitions
* Aggregate system health (band distribution, top offenders, violation types)

---

## 🖥️ UI Overview

The interface includes:

* **Simulation Controls & Stats**

  * Actor selection
  * Violation and clean events
  * Trust band and violation breakdowns

* **Actors & Enforcement Table**

  * Live trust score
  * Current trust band
  * Violation count
  * Active enforcement policy
  * Event log

The visual design mirrors **enterprise AI security dashboards** used for guardrails and observability.

---

## 🚀 How to Run

This is a **static HTML prototype** — no build step required.

### Option 1: Open Directly

1. Save the file as `index.html`
2. Open it in any modern browser

### Option 2: Serve Locally

```bash
python3 -m http.server
```

Then open:

```
http://localhost:8000
```

---

## 🛠️ Technical Notes

* No backend
* No frameworks
* No external dependencies
* Fully deterministic logic
* Designed for transparency and inspectability

---

## ⚠️ Disclaimer

This project is a **conceptual prototype** only.
It is **not** a production security system and should not be used as one.

---

## 🔒 License & Intellectual Property Notice

**Copyright © 2026 Ethan Leigh-Fellows. All rights reserved.**

This repository, including but not limited to:

* The underlying idea and conceptual framework
* All source code, logic, scoring models, UI, and documentation

is the **exclusive intellectual property of Ethan Leigh-Fellows**.

### NO RIGHTS GRANTED

**No permission is granted** to any person or entity to:

* Use, copy, reproduce, distribute, or publish this work
* Modify, adapt, translate, or create derivative works
* Implement this idea or system in any form (commercial or non-commercial)
* Train models on this code or concept
* Use this repository for research, benchmarking, or product development

**Any use whatsoever requires explicit prior written permission.**

Unauthorized use, reproduction, or implementation of this idea or code is **strictly prohibited** UNLESS OTHERWISE AGREED TO. 
