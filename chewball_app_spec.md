# 🏟️ Chewball League App – Project Specification

A personal-use web application to **simulate, manage, and track seasons** of the pen-and-paper game **Chewball**. The app should allow fast simulation of games, detailed stat tracking, and a rich historical view of league seasons, teams, and player performance.

---

## 🎯 Core Objectives

- Organize and simulate **Chewball seasons** with custom schedules and evolving team rosters
- Track detailed **player and team statistics** across seasons
- Offer a retro-inspired, markdown-like UI for nostalgic aesthetic and clarity
- Support **multiple seasons**, with historical browsing and rich in-game interactivity
- Enable both **manual gameplay** and **automated game simulation**

---

## 🧱 Data Model Overview

### 🔄 Season

Each Season is an independent container with:

- Custom **divisional structure** (e.g., 2 sub-leagues × 2 divisions)
- A list of **teams** chosen from the broader league pool
- A **10-series schedule**, each with 3 games
- Standings calculated from results
- A complete record of **games played**, including box scores and logs

> 📉 Seasons can be browsed and edited independently

### 🧒 League Teams (Persistent across seasons)

Each team may appear in any number of seasons and includes:

- **Profile Page**: team history, logo, team identity (markdown-based, read-only)
- **Player Charts**: roster of batters and pitchers, including stats and gameplay data
- **Game History**: links to games from current or past seasons where the team appeared

> 📌 Teams not participating in the current season are only accessible by switching to a season they participated in.

---

## 🗘️ Pages and Navigation

### 📁 Sidebar Layout

```
[ Season Name ▼ ]   ← Season dropdown (with week indicator)
[ Schedule ]
[ Standings ]
[ Games ]           → List of all series/games this season
[ Teams ]
   ├─ Profile
   ├─ Player Charts
   └─ Games
[ ⚙ Settings ]
[ 📂 League History / Misc ]
```

- Season dropdown includes:
  - Select from existing seasons
  - “➕ New Season” setup flow
- Week counter for tracking current series

---

## 🆕 New Season Setup Page

Wizard-style form to initialize a new season:

- Define league structure:
  - 2 Sub-Leagues → 2 Divisions per league → 4 Teams per division (customizable in future)
- Name the league/divisions
- Select existing teams or create new teams
  - Checkbox list of available teams
  - Button to "Add New Team"
- Submit to:
  - Save configuration
  - Generate randomized but balanced schedule
  - Redirect to Season Dashboard (default to Schedule page)

---

## 📅 Schedule Page

Displays the full 10-series schedule:

### Layout:

```
▸ Week 1 (expandable)
   - Game 1: Team A (0-0) vs Team B (0-0)
     → [Sim Game] / [Play Game]
     → Result: Team A (1) vs Team B (0)
     → Game link: Opens full Game Page
▸ Week 2
   ...
```

- Can only play or simulate the **current week**
- Past games are view-only
- Click on a game to enter full play-by-play view

---

## 📊 Standings Page

Grouped by **Sub-Leagues and Divisions**:

- Show:
  - Team W/L record
  - Win percentage
  - Run differential
  - Division leader indicator
- At **Week 5 (halfway)**:
  - Display **Wild Card Rankings** per league

---

## ⚾ Game Page

Simulates or displays a Chewball game.

### Core UI Sections:

- **Title**: e.g. *Series 1 Game 1: Team A @ Team B*
- **Lineups** for both teams (batters + pitchers)
- **Current Batter**: Name, Position, Stats
- **Game Log**: Chronological record of actions
- **Pitcher vs Batter graphic**
- **Roll Button**: triggers the next simulated action
- **Innings Table / Scorecard**: 3-inning structure with scores per inning

### Game Features:

- 🔄 Undo plays (only go backward, like a limited rollback)
- ✏️ Overwrite functionality (toggle bases, update text for corrections)
- ⚙ **Edit Lineup** (before start only)
  - Switch to view bench players, reassign roles
- 🚒 **Bullpen Options** (mid-game pitcher swaps)
- ⏪ Back button: returns to Schedule
- ✅ When the game ends: switch view to **read-only** mode

---

## 👢 Team Profile Page

- Markdown-based page
- Static for now (editable later)
- Allows images and styled text
- Read-only; may include:
  - Mascot
  - Stadium
  - History
  - Theme song?

---

## 📊 Player Charts Page

- Two sortable tables:
  - **Batters**
  - **Pitchers**
- Includes:
  - Player names, roles
  - Running stats (updated after each game)
  - Basic gameplay metrics (hits, RBIs, ERA, etc.)
- Button to:
  - Unlock customization
  - Toggle readonly mode
- Editable player data:
  - Name, position, handedness
  - Pre-season stats / adjustments
  - In-game accumulated stats

---

## 🧰 Other System Features

### ⚙ Settings / Misc

- Import/export JSON data for backups
- Toggle UI themes (retro, modern)
- Dev tools: reseed league, reset game state
- Optionally store data in:
  - IndexedDB (via Dexie.js)
  - Exportable JSON

### 📂 League History

- View list of all created seasons
- Click into any past season to explore data
- Archive or delete seasons

---

## 🔮 Future Features (Stretch Goals)

- Custom game rules per season
- Fantasy League Draft Mode
- Player progression between seasons
- Visual graphs/stats dashboards
- Game replays
- Sync to GitHub repo for versioned season files

