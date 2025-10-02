📌 **Cross-Reference:** For engineering guardrails and coding principles, see [`docs/principles/architecture.md`](../principles/architecture.md).
# App Name: CALL·IT: Sports Picks

## Core Concept
CALL·IT is a flexible social gaming platform where players compete by making predictions on sports outcomes. The platform supports multiple sports and tournament formats, emphasizing community, competition, and customizable gameplay.

## Game Modes

### Standings Mode
Predict the final rankings of teams within a structured competition (e.g., divisions, groups, pools, or conferences).

### Standings & Records Mode
Predict each team’s final record. Standings are auto-calculated based on win/loss totals. Ties can be manually reordered.

### Matchup Mode (Weekly Picks)
Predict the outcome of individual games, matches, or events. Configurable by organizers as:
- **Per Game Locking**: Each game locks individually at kickoff.
- **Per Window Locking**: Entire week locks at the first game’s kickoff.

Results in this mode also feed into projected standings and performance outcomes.

## Customizable Group Play

### Public & Private Groups
Compete with friends in private invite-only groups or join public groups to test your skills against the wider community.

### Organizer Controls
Group creators define how the game is played, including:
- **Scoring Method** – Points system or pick accuracy percentage.
- **Midpoint Revisions** – Option to revise long-term predictions once during a season or tournament, with scoring penalties applied.
- **Pick Frequency** – Set submission windows (per day, per week, per round, etc.).
- **Lock Times** – Lock all picks per window or per game.
- **Missed Predictions** – Default to Vegas favorite (Autopick) or score zero.

## Scoring & Leaderboards

### Multi-Layered Scoring
- **Exact outcomes** (correct rank, score, or winner).
- **Near misses** (partial credit).
- **Perfect predictions** (bonus points).

### Leaderboards
Track results in private groups and global leaderboards, filterable by sport, competition, and game mode.

---

# 📌 Call·It — Picks View CTA Blueprint (Final)

## 🎯 Standings Mode
- **PICKS_OPEN**  
  - Header: *Submit Picks*  
  - Subtext: *Make your picks before the deadline.*  
  - Color: Yellow `#FFC107`  

- **PICKS_SUBMITTED_EDITABLE**  
  - Header: *Picks Submitted*  
  - Subtext: *Edit your picks before the deadline.*  
  - Color: Green `#28A745`  

- **PICKS_LOCKED**  
  - Header: *Picks Locked*  
  - Subtext: *Track your weekly results as games conclude.*  
  - Color: Green `#28A745`  

- **REVISION_AVAILABLE (if enabled)**  
  - Header: *Mid-Season Revision Open*  
  - Subtext:  
    - Week 9 → *Revise once during Weeks 9, 10, or 11.*  
    - Week 10 → *Revise once during Weeks 10 or 11.*  
    - Week 11 → *Revise once during Week 11.*  
  - Color: Yellow `#FFC107`  

- **SEASON_OVER**  
  - Header: *Season Complete*  
  - Subtext: *Final Score: [score]. See your rank on the leaderboard.*  
  - Color: Green `#28A745`  

---

## 🎯 Standings & Records Mode
- **PICKS_OPEN**  
  - Header: *Submit Picks*  
  - Subtext: *Make your picks before the deadline.*  
  - Color: Yellow `#FFC107`  

- **PICKS_SUBMITTED_EDITABLE**  
  - Header: *Picks Submitted*  
  - Subtext: *Edit your picks before the deadline.*  
  - Color: Green `#28A745`  

- **PICKS_LOCKED**  
  - Header: *Picks Locked*  
  - Subtext: *Track your weekly results as games conclude.*  
  - Color: Green `#28A745`  

- **REVISION_AVAILABLE (if enabled)**  
  - Header: *Mid-Season Revision Open*  
  - Subtext:  
    - Week 9 → *Revise once during Weeks 9, 10, or 11.*  
    - Week 10 → *Revise once during Weeks 10 or 11.*  
    - Week 11 → *Revise once during Week 11.*  
  - Color: Yellow `#FFC107`  

- **SEASON_OVER**  
  - Header: *Season Complete*  
  - Subtext: *Final Score: [score]. See your rank on the leaderboard.*  
  - Color: Green `#28A745`  

---

## 🎯 Weekly Picks — Per Game Locking
- **PICKS_OPEN**  
  - Header: *Submit Picks*  
  - Subtext: *Make your picks before each game’s kickoff.*  
  - Color: Yellow `#FFC107`  

- **PICKS_SUBMITTED**  
  - Header: *Picks Submitted*  
  - Subtext: *Edit your picks until each game’s kickoff.*  
  - Color:  
    - Green `#28A745` if user submitted  
    - Red `#D62828` if autopick applied  

- **DEADLINE_MISSED_PARTIAL**  
  - Header: *Submit Picks*  
  - Subtext (Vegas): *Vegas favorites will be autopicked.*  
  - Subtext (Zero): *Missed games scored as zero.*  
  - Color: Red `#D62828`  

---

## 🎯 Weekly Picks — Per Window Locking
- **PICKS_OPEN**  
  - Header: *Submit Picks*  
  - Subtext: *Make your picks before the window locks.*  
  - Color: Yellow `#FFC107`  

- **PICKS_SUBMITTED**  
  - Header: *Picks Submitted*  
  - Subtext: *Edit your picks before the window locks.*  
  - Color: Green `#28A745`  

- **DEADLINE_MISSED_NO_PICKS**  
  - Header: *Missed Deadline*  
  - Subtext (Vegas): *Vegas favorites will be autopicked.*  
  - Subtext (Zero): *Missed window scored as zero.*  
  - Color: Red `#D62828`  

- **WINDOW_CLOSED** *(only appears if picks were submitted)*  
  - Header: *Picks Locked*  
  - Subtext: *Picks for this window are locked. Future windows remain open.*  
  - Color: Green `#28A745`  

- **SEASON_OVER**  
  - Header: *Season Complete*  
  - Subtext: *Final Score: [score]. See your rank on the leaderboard.*  
  - Color: Green `#28A745`

---

## Style Guidelines

### 1. Color Palette
- **Primary**: Blue (#4169E1)
- **Backgrounds**: Light (#E6EAF7), Dark (#0D1117)
- **Accent**: Orange (#FFA500)
- **Text**: Dark Gray (#333333), Off-White (#F0F6FC)
- **Correct (Green)**: #28A745  
- **Incorrect (Red)**: #D62828  
- **Near Miss (Yellow)**: #FFC107  
- **Off by 2 (Orange)**: #FFA500  
- **Pending (Blue)**: #4169E1  
- **Zero Points (Gray)**: #6B7280  

### 2. Typography
- **Inter** (sans-serif), tabular numerals for alignment.
- **H1**: 24–28px bold  
- **H2**: 18–20px medium  
- **Body**: 14–16px regular  
- **Tables**: 12–14px medium, uppercase headers  

### 3. Layout & Spacing
- Grid-based layout, consistent multiples of 8px spacing (8, 16, 24, etc.).
- Border radius = 8px.

### 4. Buttons
- **Submit Picks / Save Changes** = Blue (#4169E1), inactive until valid.  
- **Action Complete** = Green (#28A745).  
- **Action Missed** = Red (#D62828).  
- **Secondary** = Outline.  
- **Tertiary** = Muted (Cancel).  

### 5. Feedback & Status Rules
- Standings & Standings + Records: Standings colors update weekly after the last game of that week.  
- Standings & Records: Records colors finalize only at end of season (totaling 17).  
- Weekly Picks: Game results update in real time; record colors apply after the last game of the creation week concludes.  
- Zero Points Missed Pick: Teams grayed out (#6B7280). Both teams reflect 0–1 in projections.  

### 6. Animation
- Subtle (150–200ms), ease-in-out.  
- Examples: lock icon on submit, leaderboard slide on rank change.  

### 7. Data Visualization
- Neutral grays, map highlight colors to semantic system.
