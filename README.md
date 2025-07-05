# 🏟️ Chewball League App

A personal-use web application to **simulate, manage, and track seasons** of the pen-and-paper fantasy baseball RPG, **Chewball**.

This tool brings structure, speed, and depth to the tabletop game—handling league creation, schedule management, game simulation, stat tracking, and more. Designed with a retro-flavored UI and markdown-inspired profiles to honor the spirit of the game while embracing modern conveniences.

---

## 🎯 Features

- 📅 Create and simulate full **Chewball seasons** with custom league structures and team rosters
- 📊 Track detailed **player and team statistics** across seasons
- 🧾 Rich historical record-keeping with browsable season archives
- ⚙️ Supports **manual gameplay** or **automated game simulation**
- 🧙‍♂️ Markdown-powered team profile pages for added immersion
- 🗃️ Persistent team data across multiple seasons

---

## 🗺 App Navigation

- **Season Selector** – Pick from existing seasons or start a new one
- **Schedule** – Play or simulate 3-game series across 10 total weeks
- **Standings** – See team rankings by division with live stat updates
- **Games** – Browse or revisit any simulated game
- **Teams**
  - View static team profiles and history
  - Access roster stats via Player Charts
- **Game Page** – Run Chewball games with interactive play-by-play, stat updates, and mid-game substitutions
- **Settings & League History** – Import/export data, toggle themes, explore archived seasons

---

## 🧱 Data Overview

### Season

- Custom league/divisional structure
- Team list & schedule
- Game results and logs
- View/edit independently

### Team

- Persistent across seasons
- Profile, player charts, game history
- Markdown-based identity & theming

### Game

- 3-inning matchups with simulated play
- Editable lineups and undo features
- Post-game locked state for review

---

## 🆕 New Season Setup

1. Define league/division structure (e.g. 2 Sub-Leagues × 2 Divisions × 4 Teams)
2. Select or create teams
3. Generate balanced 10-series schedule
4. Jump into Season Dashboard

---

## 📂 Pages At A Glance

| Page             | Description                                                    |
| ---------------- | -------------------------------------------------------------- |
| `Schedule`       | Simulate or play current series, view previous games           |
| `Standings`      | Division-based rankings with W/L %, run diff, wild card status |
| `Games`          | Game logs and box scores for every match in the season         |
| `Teams`          | Markdown-based profile + player stats                          |
| `Player Charts`  | Sortable batter/pitcher tables with editable info              |
| `Settings`       | Export/import JSON, reset game data, theme switching           |
| `League History` | Explore or archive past seasons                                |

---

## 🧰 Tech & Tools

- **Frontend**: React (with Vite), Zustand, Tailwind CSS
- **Storage**: IndexedDB via Dexie.js + JSON import/export
- **Design Philosophy**: Markdown-inspired UI, retro themes, offline-friendly

---

## 🔮 Stretch Goals

- Custom game rules and modifiers
- Fantasy Draft mode
- Player progression between seasons
- Stats visualization dashboards
- Replay log viewer
- GitHub-backed season file syncing

---

## 📦 Getting Started

Coming soon: Setup guide & development instructions.

---

## 📝 License

Personal-use project. No commercial license implied. Chewball™ is a homebrew game for friends and storytelling.

---

## 💌 Contribute or Ask

This is a solo project built for fun, stats, and storytelling. Feel free to fork or reach out with questions and ideas!
