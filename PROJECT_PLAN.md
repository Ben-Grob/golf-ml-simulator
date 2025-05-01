# 🏌️ Golf Score Impact Analyzer – Project Plan

## 🎯 Project Goal

Predict a golfer’s score based on key stats (e.g., drive distance, GIR %, scrambling) and simulate how changes in these stats would affect overall scoring — to guide personalized practice and improvement.

---

## 🧱 Data Overview

### 📥 Inputs (Features)
| Stat | Description |
|------|-------------|
| `drive_dist`       | Average carry distance (yards) |
| `fairways_hit_pct` | % of fairways hit |
| `gir_pct`          | % of greens in regulation |
| `scramble_pct`     | % of successful up-and-downs |
| `putts_per_round`  | Average number of putts per round |
| `hcp`              | Players handicap index |

### 🎯 Target (Label)
- `score` – Total strokes per round (can later be hole-by-hole)

---

## 🧠 Questions to Answer

- What skills (stat categories) have the biggest impact on score?
- How much would my score/handicap change if I:
  - Added 10 yards of drive distance?
  - Hit 10% more greens?
  - hit 20% more fairways
  - e.t.c
- Which area of my game should I prioritize to lower my score fastest?

---

## 🗺️ Milestones

### ✅ Phase 1: Setup & Data
- [ ] Define inputs and outputs
- [ ] Simulate or gather sample data
- [ ] Create folder structure and notebooks

### 📊 Phase 2: Data Exploration
- [ ] Clean and format data
- [ ] Explore stat distributions
- [ ] Identify which stats most impact score

### 🧠 Phase 3: Modeling
- [ ] Train regression model (Random Forest or XGBoost)
- [ ] Evaluate model accuracy (R², MAE)
- [ ] Examine feature importance

### 🔁 Phase 4: Simulation Tool
- [ ] Build logic to simulate stat changes
- [ ] Predict impact on score from stat improvements

### 🖥️ Phase 5: App (Optional)
- [ ] Build a Streamlit UI for score simulation
- [ ] Deploy locally or online (Streamlit Cloud)

# Part 2: Shot-by-Shot Sim Expansion

## Goal: High level stats --> Club specific
Instead of relying on stats such as GIR, use players accuracy and distance with each of their clubs to simulate shot-by-shot results

## Data Overview:

### Data collection:
- Track distance and yards off of center (L/R) with each club over 20+ shots (the more the merrier)
- e.g. (Club: 7-iron, Carry: 157, Miss: -15) -- Carry is in yards, negative miss indicates left of target, positive would indicate a miss to the right

### Target:
- Simulated shot -- uses data to create a random shot that would be comparable to the result from an actual swing
- Simulated Hole -- simulate shots from tee to green(maybe not putts) repeadetly and take an average score/shots to green for a specific hole
    - Putts won't be simulated, but could be given an average difficulty based on distance to the center of the green and course difficulty
- simulated Round -- Simulate every hole many times and take an average and display the predicted score and IQR

## Revisit Questions
Use this style of simulation to more accurately predict scores and answer questions
- What skills (stat categories) have the biggest impact on score?
- How much would my score/handicap change if I:
  - Added 10 yards of drive distance?
  - Hit 10% more greens?
  - hit 20% more fairways
  - e.t.c
- Which area of my game should I prioritize to lower my score fastest?

---

## 🔗 Useful Links
- [Insert link to data source or inspiration]
- [Insert link to project repo or demo app]

