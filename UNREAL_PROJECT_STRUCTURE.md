# 📦 Unreal Project Structure — EduFootball Manager

This structure enforces strict modularity and long-term scalability.

---

## Root

/Source/EduFootballManager/

---

## 1. Core

/Source/EduFootballManager/Core/

- GameInstance
- GameModeBase
- Time system
- Global event dispatcher
- Global save/load coordinator

Purpose:
- Owns lifecycle and high-level state

---

## 2. Simulation

/Source/EduFootballManager/Simulation/

- MatchSimulationSubsystem
- MatchTimeline
- EventResolver
- ProbabilityEngine

Purpose:
- All football match simulation

---

## 3. Tactics

/Source/EduFootballManager/Tactics/

- Formation system
- Phase system
- Instruction system

Purpose:
- Tactical logic only

---

## 4. Stats & Analytics

/Source/EduFootballManager/Stats/

- MatchStatsProcessor
- xGCalculator
- HeatmapGenerator

Purpose:
- Transform events → metrics

---

## 5. Players

/Source/EduFootballManager/Players/

- PlayerProfile
- AttributeBlocks
- PersonalityProfiles

Purpose:
- All player data definitions

---

## 6. Development & Physiology

/Source/EduFootballManager/Development/

- TrainingSystem
- FatigueSystem
- InjurySystem
- FormCurveSystem

---

## 7. Psychology & Relationships

/Source/EduFootballManager/Psychology/

- MoraleSystem
- RelationshipGraph
- LeadershipEffects

---

## 8. Finance & Transfers

/Source/EduFootballManager/Finance/

- ClubFinanceSystem
- ContractSystem
- TransferMarketSystem
- MarketInflationModel

---

## 9. AI & Adaptation

/Source/EduFootballManager/AI/

- TacticalPatternTracker
- CounterStrategyGenerator
- OpponentMemory

---

## 10. Academy & Education

/Source/EduFootballManager/Academy/

- AcademyProgressionSystem
- LicensingSystem
- PuzzleSystem
- ScenarioSystem

---

## 11. Narrative & Media

/Source/EduFootballManager/Narrative/

- MediaEventSystem
- PressConferenceSystem
- ReputationSystem

---

## 12. Meta-Progression

/Source/EduFootballManager/Meta/

- ManagerProfileSystem
- FootballIQSystem
- ToolUnlockSystem

---

## 13. UI

/Source/EduFootballManager/UI/

- MainMenu
- SquadScreen
- TacticsScreen
- MatchDashboard
- AcademyScreen
- FinanceScreen

UMG Widgets live here.

---

## 14. Data Assets

/Content/DataAssets/

- Formations
- Tactical roles
- Training modules
- Scenarios
- Puzzles

All configurable data via UDataAsset.

---

## 15. Save System

/Source/EduFootballManager/Save/

- SaveGameProfiles
- CareerSlots
- Versioning logic

---

## 16. Build & Config

/Config/
/Build/

- Packaging rules
- Platform configs
