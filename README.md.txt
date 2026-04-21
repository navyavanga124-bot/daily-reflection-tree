# Daily Reflection Tree — Deterministic Reflection Agent

## Overview

This project implements a **deterministic end-of-day reflection system** that guides an employee through a structured self-reflection process.

Unlike AI chat-based tools, this system:

* Uses **no LLM or AI at runtime**
* Produces **consistent and auditable outputs**
* Encodes psychological principles into a **decision tree**

The goal is to help users reflect across three key axes:

1. **Locus of Control** (Victim ↔ Victor)
2. **Orientation** (Entitlement ↔ Contribution)
3. **Radius of Concern** (Self ↔ Others)

---

## Project Structure

/tree/

* reflection-tree.json
* tree-diagram.md

/agent/ (optional)

* main.py

/transcripts/ (optional)

* persona1.md
* persona2.md

write-up.md
README.md

---

## How It Works

The system is implemented as a **decision tree**:

* Each node represents a step in the reflection
* Users select from **fixed options**
* Each option leads to a **predefined next node**
* No randomness, no AI involvement

---

## Node Types

* **start** → Begins session
* **question** → User selects an option
* **decision** → Internal routing
* **reflection** → Insight based on answers
* **bridge** → Moves between axes
* **summary** → Final reflection
* **end** → Closes session

---

## State Tracking

The system tracks:

* User answers (by node ID)
* Axis signals:

  * axis1 → internal / external
  * axis2 → contribution / entitlement
  * axis3 → self / others

These are tallied to determine dominant behavioral patterns.

---

## Key Design Principles

* **Deterministic** → Same input = same output
* **Structured thinking** → Guided reflection, not free text
* **Non-judgmental tone** → Encourages awareness
* **Conversational flow** → Feels natural, not like a survey

---

## Example Output

Today you leaned internal in handling situations, contribution-oriented in your actions, and your focus extended toward others.

This reflects a pattern of ownership and outward thinking — a strong base for consistent growth.

---

## Running the Agent (Optional)

```bash
cd agent
python main.py
```

---

## Future Improvements

* Multi-day tracking (deterministic)
* Adaptive depth in questioning
* Visual analytics dashboard
* Expanded behavioral coverage

---

## Author

Navya Vanga
