# 🧠 System Architecture — EduFootball Manager

## 1. Architectural Philosophy

- Simulation-first design
- Data-driven systems
- Modular Unreal subsystems
- Clear separation between:
  - Core simulation
  - UI
  - Education layer
  - Meta-progression

All systems communicate through:
- Subsystems
- Event dispatchers
- Read-only data assets where possible

---

## 2. Core Runtime Loop

### Weekly Club Cycle
1. Training simulation
2. Morale & psychology update
3. Financial update
4. Media events
5. Tactical preparation

### Match Day Cycle
1. Tactical setup
2. Opponent AI analysis
3. Match simulation ticks
4. Event generation
5. Stats aggregation
6. Psychology & fatigue update

### Season Cycle
1. Financial summary
2. Transfers & contracts
3. Player aging & growth
4. Board evaluation
5. Academy progression

---

## 3. Main Subsystems

### A. MatchSimulationSubsystem
Responsible for:
- Match timeline
- Probabilistic event resolution
- Tactical modifiers

Consumes:
- Tactical System
- Player Profiles
- Psychology System

Outputs:
- Raw match events
- Player fatigue changes
- Post-match stats inputs

---

### B. TacticalSystem
Responsible for:
- Formations
- Roles
- Phases of play
- Player instructions

Feeds modifiers into:
- MatchSimulationSubsystem
- AI Counter System

---

### C. Stats & Analytics System
Responsible for:
- Event → Metric conversion
- xG, xA, PPDA, heatmaps
- Match reports

Consumes:
- Match events

Feeds:
- UI dashboards
- Board evaluation
- Media narratives

---

### D. Player Development System
Responsible for:
- Attributes
- Training plans
- Form curves
- Injury risk

Consumes:
- Training schedules
- Match workloads

Feeds:
- Match performance
- Market value
- Squad hierarchy

---

### E. Psychology & Group Dynamics System
Responsible for:
- Morale
- Ego
- Leadership
- Relationships

Consumes:
- Match results
- Media choices
- Squad decisions

Feeds:
- Performance volatility
- Transfer requests
- Locker room events

---

### F. Finance & Economy System
Responsible for:
- Club budget
- Contracts
- Market inflation
- Debt

Consumes:
- Results
- Media exposure
- Transfers

Feeds:
- Available budget
- Board pressure
- Long-term survival risk

---

### G. Academy & Education System
Responsible for:
- Certifications
- Tactical curriculum
- Learning challenges

Consumes:
- Player decisions
- Puzzle results

Feeds:
- Feature unlocks
- Analytical panel depth

---

### H. Adaptive AI System
Responsible for:
- Tracking player tactical habits
- Generating counter-strategies

Consumes:
- Player history
- Repeated behaviors

Feeds:
- Opponent tactical setups

---

### I. Meta-Progression System
Responsible for:
- Football IQ level
- Manager profile
- Access gating to tools

Consumes:
- Player success in systems

Feeds:
- UI depth
- Tactical freedom
- Educational unlocks

---

## 4. Data Flow Overview

Player Decision
→ Tactical System
→ Match Simulation
→ Event Stream
→ Stats Processor
→ Psychology & Finance
→ Board & Media
→ Meta Progression
→ Unlocks More Tools
→ Back to Player Decision

This loop is the heart of the game.
