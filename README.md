# ⚡ APTITUDE PRO — Placement Preparation Platform

> **Practice Smart. Improve Daily. Crack Placements.**

APTITUDE PRO is a modern, responsive, full-stack placement preparation web application built for college engineering students and freshers preparing for campus recruitment drives, competitive examinations, and national qualifier tests (TCS NQT, Infosys, Accenture, Wipro, Cognizant, Amazon).

---

## 🚀 Key Features

### 1. 🎯 Dynamic Student Dashboard
* **Daily Habit Streak Engine**: 7-day momentum calendar with animated streak flames, XP multipliers, and best streak trackers.
* **Placement Readiness Score**: Real-time percentile benchmark calculated against target recruiters.
* **Smart Weak Area Diagnostics**: Flags topics where accuracy is `< 65%` and generates instant 1-click drill recommendations.
* **Domain Quick Launch**: Direct access to Quantitative Aptitude, Logical Reasoning, Verbal Ability, and Company Packs.

### 2. 📚 Topic-Wise Practice Arena
* **Curated Question Bank**: High-frequency questions across Arithmetic, Commercial Math, Permutations, Syllogisms, Series, Grammar, and Reading Comprehension.
* **Instant Step-by-Step Derivations**: Complete verified explanations with mathematical logic.
* **Vedic Math & Shortcut Drawer**: Provides 10-second shortcut techniques and elimination rules.
* **Mentor Hints & Bookmarking**: Toggle hints on demand; bookmark challenging questions for revision.

### 3. ⏱️ Timed Examination & Mock Test Engine
* **Actual Exam Simulation**: Countdown timer with urgent alerts (`< 3 mins`).
* **Interactive Question Palette**: Colour-coded status tracking (Answered, Marked for Review, Unvisited, Current).
* **Negative Marking Support**: Configurable marking schemes (e.g. `+3 / -0.25`).
* **Post-Test Comprehensive Scorecard**:
  * Score obtained vs Total marks
  * Overall accuracy percentage
  * Time spent per question
  * Percentile benchmark
  * Question-by-question review with student answers vs correct answers

### 4. 🏢 Company Placement Packs
* Curated recruitment patterns, test durations, sectional cutoffs, and hiring stages for:
  * **TCS** (Ninja / Digital / Prime — NQT Pattern)
  * **Infosys** (Systems Engineer / DSE / Specialist Programmer)
  * **Accenture** (Associate Software Engineer — Cognitive & Technical Assessment)
  * **Wipro** (Elite National Talent Hunt)
  * **Cognizant** (GenC / GenC Next)
  * **Amazon** (SDE-1 / Problem Solving)

### 5. ⚡ Formulas, Tricks & Speed Math Hub
* Complete cheat sheet library for:
  * Arithmetic & Commercial Math (Profit/Loss, Successive Discounts, CI-SI differences)
  * Time, Speed, Distance & Work (Relative speed, Train crossing, Chain rule)
  * Combinatorics & Probability
  * Clocks & Calendars, Syllogisms, and Grammar rules
* **Interactive Mental Speed Drill**: Rapid recall tests for squares and cubes.
* **1-Click Formula Clipboard Copy**.

### 6. 📊 Analytics & Performance Intelligence
* **Topic Accuracy Breakdown Bar Chart** (powered by Recharts).
* **Mock Test Score Progression Area Chart** tracking trajectory over sequential tests.
* **Weak Topic Diagnostic Radar** with targeted action plans.

### 7. 🏆 Badges & Achievement System
* Gamified XP leveling system (Level 1 Initiate to Level 5 Aptitude Titan).
* Badges: *First Step*, *3-Day Fire*, *Streak Titan*, *Quant Conqueror*, *Mock Challenger*, *Accuracy Bullseye*, *Speed Demon*, *Campus Ready*.

### 8. 🔐 Authentication & Supabase Integration
* Built with `@supabase/supabase-js` and PostgreSQL.
* Includes `supabase/schema.sql` with full tables (`profiles`, `test_attempts`, `bookmarks`, `user_badges`) and Row Level Security (RLS) policies.
* **Instant Demo Mode**: Pre-loaded student profile so the platform works 100% out of the box offline or without immediate Supabase configuration!

---

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| **Frontend Framework** | React 19, Vite 8 |
| **Styling** | Tailwind CSS v4, Custom Design Tokens |
| **Routing** | React Router v7 |
| **Icons** | Lucide React |
| **Data Visualizations** | Recharts |
| **Animations / Confetti** | Canvas Confetti |
| **Backend & DB** | Supabase, PostgreSQL |

---

## 💻 Local Setup & Execution Instructions

### Prerequisites
* **Node.js** (v18 or higher recommended)
* **npm** (v9 or higher)

### Step 1: Open Terminal in Project Directory
```powershell
cd C:\Users\ADMIN\.gemini\antigravity\scratch\aptitude-pro
```

### Step 2: Install Dependencies (if not already installed)
```bash
npm install
```

### Step 3: Run the Development Server
```bash
npm run dev
```

The application will start immediately at:
```
http://localhost:5173/
```

Open this URL in Google Chrome, Microsoft Edge, or any modern web browser.

---

## 🗄️ Supabase PostgreSQL & Google OAuth Setup

### 1. Instant Evaluation (Out of the Box)
The platform includes an automated fallback provider: clicking **"Continue with Google"** on [`/login`](http://localhost:5173/login) immediately authenticates an aspirant demo session with verified metadata and local storage persistence.

### 2. Live Supabase & Google Cloud Setup
To connect real Supabase Google Authentication:
1. Create a project on [Supabase](https://supabase.com).
2. Go to **Authentication -> Providers -> Google**.
3. Enable Google provider and input your **Google Client ID** and **Google Client Secret** from [Google Cloud Console](https://console.cloud.google.com/apis/credentials).
4. In Google Cloud Console, set the Authorized Redirect URI to your Supabase callback URL:
   `https://<your-project-id>.supabase.co/auth/v1/callback`
5. Open the **SQL Editor** in your Supabase dashboard and run [`supabase/schema.sql`](./supabase/schema.sql).
6. Set your credentials in `.env`:
```env
VITE_SUPABASE_URL=https://your-project-id.supabase.co
VITE_SUPABASE_ANON_KEY=your-actual-anon-key
```
7. Restart the Vite server (`npm run dev`).

---

## 🚢 Deploying to Vercel

1. Push your repository to GitHub:
```bash
git init
git add .
git commit -m "feat: complete Aptitude Pro placement preparation platform"
git branch -M main
git remote add origin <your-github-repo-url>
git push -u origin main
```
2. Import the repository in [Vercel](https://vercel.com).
3. Under Environment Variables in Vercel, optionally add:
   * `VITE_SUPABASE_URL`
   * `VITE_SUPABASE_ANON_KEY`
4. Click **Deploy**.
