# 🏏 IPL Fantasy 2026

> **Real-time multiplayer fantasy cricket — live auction room, NFL-style waiver wire, and head-to-head matchweeks. No app download required.**

![IPL Fantasy Banner](https://img.shields.io/badge/IPL-2026%20Season%2019-orange?style=for-the-badge&logo=cricket&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-Realtime%20Sync-yellow?style=for-the-badge&logo=firebase)
![Vanilla JS](https://img.shields.io/badge/Built%20With-Vanilla%20JS-blue?style=for-the-badge&logo=javascript)
![Players](https://img.shields.io/badge/Players-250%2B-green?style=for-the-badge)

---

## ✨ Features

### 🔨 Live Draft Auction
- Real-time multiplayer bidding room synced via Firebase Firestore
- **2-round system** — Indian players first, then Overseas
- 60-second countdown timer per player with urgent pulse at 10s
- Commissioner controls: Sold Now, Skip, timer management
- Live bid feed visible to all managers simultaneously
- In-room draft chat so managers can trash-talk in real time
- Full budget tracking per team during the auction

### 🏆 League Management
- Create public or private leagues in under a minute
- Shareable invite link — friends join with one click
- **Commissioner tools:** kick members, post announcements, adjust settings, process waivers manually
- Support for 4–12 teams, ₹50–₹125 Cr budgets, 11–18 players per squad
- **Standard (Total Points)** and **Head-to-Head (Weekly Matchups)** league types

### ⚔️ Head-to-Head Matchweeks
- Every 5 IPL matches = 1 matchweek (17 matchweeks across the season)
- Rotating round-robin schedule auto-generated from your league's teams
- IPL-style points table: Win = 2pts · Tie = 1pt · Loss = 0pts
- NRR tiebreaker (average fantasy points per matchweek)
- Week history with full result archive
- Auto-lock after the 5th match of each week

### 🔄 Waiver Wire & Trades
- NFL-style free agent pickups with 48-hour processing window
- Priority-order waiver claims when multiple teams want the same player
- Commissioner can grant or deny waiver claims manually
- Player-for-player trade proposals with accept/decline flow
- Full transaction log for the entire season

### ⚡ Starting XI & Captaincy
- Set your 11 starters before each match
- Captain (2×) and Vice-Captain (1.5×) multipliers
- **IPL 2026 rules enforced:** Max 4 overseas · Min 1 WK · Min 2 bowlers
- One-tap Auto-fill and AI-powered Optimize XI button
- Drag between Starting and Bench panels

### 📊 Manual Scoring System
- Commissioner enters player points after each IPL match
- Points committed instantly to all league members
- Full per-player breakdown (runs, wickets, economy, fielding)
- Season total + live (uncommitted) points shown side by side
- Points table auto-updates on commit

### 💬 League Chat
- Live chat synced in real-time for all league members via Firebase
- Separate draft room chat during the auction
- Unread message badge on the Chat tab

### 🚫 Injury Flags
- Commissioner marks players as **Doubtful** or **Out**
- Injury badges appear everywhere the player is shown
- Owners with that player get an in-app alert on league open

---

## 🗂️ Full Feature List

| Feature | Details |
|---|---|
| Players database | 250+ IPL 2026 players across all 10 franchises |
| Roles | Batter · Bowler · All-rounder · Wicketkeeper |
| Auction rounds | Round 1: Indian players · Round 2: Overseas |
| Auction timer | 60s per player, urgent pulse at ≤10s |
| Budget | ₹50 / ₹75 / ₹100 / ₹125 Cr (Real IPL) per team |
| Squad size | 11 / 15 / 18 players per team |
| Overseas cap | Max 4 in Playing XI |
| Captain bonus | 2× points |
| Vice-Captain bonus | 1.5× points |
| Waiver processing | Manual (commissioner) or auto every Tuesday |
| Trade system | Propose → Accept/Decline → auto-execute |
| Matchweeks | Every 5 IPL matches, ~17 per season |
| Sync | Firebase Firestore real-time for all data |

---

## 🏏 Scoring Rules

### Batting
| Action | Points |
|---|---|
| Run scored | +1 |
| Boundary (4) | +1 |
| Six (6) | +2 |
| Half-century (50+) | +8 |
| Century (100+) | +16 |
| Duck (0 off 1+ balls) | −2 |
| Strike rate ≥ 170 (min 10 balls) | +6 |
| Strike rate 150–169 | +4 |
| Strike rate 130–149 | +2 |
| Strike rate < 70 (min 10 balls) | −6 |

### Bowling
| Action | Points |
|---|---|
| Wicket | +25 |
| 3-wicket haul bonus | +4 |
| 4-wicket haul bonus | +8 |
| 5-wicket haul bonus | +16 |
| Maiden over | +12 |
| Economy < 6 (min 2 overs) | +6 |
| Economy 6–7.99 | +4 |
| Economy ≥ 10 (min 2 overs) | −6 |

### Fielding & Bonus
| Action | Points |
|---|---|
| Catch | +8 |
| Stumping | +12 |
| Run-out (direct) | +12 |
| Run-out (assist) | +6 |
| Playing XI | +4 |
| Player of the Match | +16 |
| Captain | ×2 |
| Vice-Captain | ×1.5 |

---

## 🚀 Getting Started

### Play instantly (no setup needed)
1. Open `index.html` in any modern browser — or host it anywhere static
2. Click **Sign In** (top right) — enter your name and team nickname
3. Click **+ Create League** from the Leagues page
4. Set your league name, team count, budget, and type
5. Share the invite link with your friends
6. Once everyone joins, go to your league → **Start Draft Auction**
7. In the waiting room, click **Begin Auction Now** when all managers are present

### For members joining
1. Open the invite link your commissioner shared
2. Sign in and enter your team name
3. Click **Enter Draft Room** when the auction starts

---

## 🏗️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML · CSS · JavaScript (no frameworks) |
| Realtime sync | Firebase Firestore (live listeners) |
| Fonts | Bebas Neue · DM Sans · JetBrains Mono |
| Hosting | Any static host (GitHub Pages, Netlify, Vercel, etc.) |
| Auth | Lightweight local storage (name + team nickname) |

No build step. No npm. No framework. Just one `index.html` file.

---

## 📁 Project Structure

```
index.html          ← The entire app (HTML + CSS + JS in one file)
README.md           ← This file
```

The app is intentionally a single self-contained file for easy sharing and hosting.

---

## 🔧 Firebase Setup

The app ships with a default Firebase project for demo use. To use your own:

1. Go to [Firebase Console](https://console.firebase.google.com/) and create a project
2. Enable **Firestore Database** (start in test mode)
3. Replace the `firebaseConfig` object near the top of `index.html`:

```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

4. Set Firestore rules to allow reads/writes during your league season:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}
```

> ⚠️ Tighten these rules before making your league public.

---

## 👑 Commissioner Guide

As commissioner you have exclusive access to:

| Tool | How to use |
|---|---|
| **Start Auction** | League page → *Start Draft Auction* → waiting room → *Begin Auction Now* |
| **Sold / Skip** | During auction — *✓ SOLD* or *Skip →* buttons appear only for you |
| **Process Waivers** | Waiver Wire tab → *⚡ Process Waivers Now* |
| **Grant/Deny Claims** | Each claim shows Grant ✓ and Deny ✗ buttons |
| **Injury Flags** | Call `setInjuryFlag('Player Name', 'out', 'reason')` in browser console |
| **Post Announcement** | Overview tab → *📣 Post Announcement* |
| **Enter Scores** | Scoring page → enter player points → *✅ Commit Points to Season* |
| **Kick Member** | Overview → Members list → *Remove* button |
| **League Settings** | ⚙️ League Settings button in league header |
| **Lock Matchweek** | H2H tab → *🔒 Lock Week* (auto-locks after 5th match) |

---

## 📱 Browser Support

| Browser | Support |
|---|---|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Mobile (iOS / Android) | ✅ Responsive |

---

## 🏟️ All 10 IPL Franchises

| Team | Full Name |
|---|---|
| **CSK** | Chennai Super Kings |
| **MI** | Mumbai Indians |
| **RCB** | Royal Challengers Bengaluru |
| **KKR** | Kolkata Knight Riders |
| **SRH** | Sunrisers Hyderabad |
| **DC** | Delhi Capitals |
| **RR** | Rajasthan Royals |
| **LSG** | Lucknow Super Giants |
| **GT** | Gujarat Titans |
| **PBKS** | Punjab Kings |

---

## 📋 Roadmap

- [ ] Firestore security rules template
- [ ] Email notifications for waiver results and trade offers
- [ ] Historical season stats per player
- [ ] Playoff bracket for top 4 teams
- [ ] Dark/light theme toggle
- [ ] Player news feed integration
- [ ] Export team as image / share card

---

## 🤝 Contributing

Pull requests welcome. For major changes please open an issue first.

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

<div align="center">

**Built for cricket fans. Powered by Firebase. No download needed.**

🏏 *IPL Fantasy 2026 — Season 19*

</div>
