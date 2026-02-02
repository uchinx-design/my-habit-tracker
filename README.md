# Loggd — Track Your Life

A self-hosted habit tracker with **Google Drive auto-sync**, heatmap, tasks, focus timer, journal, goals, vision board, notes, and gamification.

## ⭐ NEW: Google Drive Sync

✅ **Auto-save to Google Drive** — Never lose your data  
✅ **Sync across ALL devices** — Phone, laptop, tablet  
✅ **Free forever** — No subscription fees  
✅ **100% private** — Only you can access your data  

**👉 See [GOOGLE_DRIVE_SETUP.md](GOOGLE_DRIVE_SETUP.md) for setup instructions** (takes 5 minutes)

---

## Deploy to GitHub Pages

1. Create a new GitHub repository (or use an existing one).
2. Add `index.html` to the repo root.
3. Go to **Settings → Pages → Source: `main` branch, root `/`**.
4. GitHub will publish it at `https://your-username.github.io/your-repo-name/`.

That's it — no build step, no dependencies, no server.

## Features

| Module | What it does |
|---|---|
| **☁️ Google Drive Sync** | Auto-save to cloud, sync across all devices, never lose data |
| **Dashboard** | Single-page overview: streak, habits, tasks, goals, and the activity heatmap |
| **Heatmap** | GitHub-style yearly grid. Each cell's color intensity = how many habits you completed that day |
| **Habits** | Daily/weekday/weekend schedules, streak tracking, skip-safe |
| **Tasks** | Priority, tags, "Main Focus" pin, link to goals |
| **Focus Timer** | Pomodoro sessions (15/25/45/60/90 min), session tracking |
| **Journal** | Morning planning + evening reflection + mood tracker |
| **Goals** | Long-term goals with milestones, categories, progress bar |
| **Vision** | 6 life-design exercises (Eulogy, Bucket List, Mission, etc.) |
| **Notes** | Hierarchical pages with auto-save |
| **Gamification** | XP, levels, 16 badges, simulated leaderboard |

## Data Storage

**With Google Drive Sync (Recommended):**
- All data automatically saves to YOUR Google Drive
- Syncs across all your devices in real-time
- Cloud backup — never lose data even if device breaks

**Without Sync:**
- Data saved to `localStorage` in your browser
- Manual backup: Open console and run `JSON.stringify(localStorage)`

**👉 Enable sync:** See [GOOGLE_DRIVE_SETUP.md](GOOGLE_DRIVE_SETUP.md)

## License

MIT — do whatever you want.
