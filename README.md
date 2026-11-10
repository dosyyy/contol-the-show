# PCR Live Broadcast & Esports Control Room

A production control room (PCR) and real-time live streaming HUD overlay web application for battle royale and esports tournaments. Features live scoring, player health knockouts, recall tracking, custom formula multipliers, roster management with logos, and a 100% transparent OBS browser source overlay.

---

## 🚀 Features

- **Live Esports Game Controller**: Fullscreen zero-scroll team matrix (supports 1 to 20 teams) with instant player status toggling (`Alive`, `Knocked`, `Finished`) and integrated recall tracking.
- **OBS Live Stream Overlay**: 100% transparent browser source overlay displaying team name, logo, recall symbol, player life bars, finish points (`FIN`), and total points (`PTS`).
- **Score Calculation**: Flexible standard formula or custom weighting for finish and placement points.
- **Role-Based Access Control**:
  - **Admin**: Full tournament management, temporary operator pass generation, schedule planning, and global match archives.
  - **Staff / Operator**: Isolated temporary access with custom match quotas and automated pass expiry.
- **Match History & Exports**: Archived match scoreboards with single-click scorecard text file downloads.
- **Responsive Theme**: Signature esports design in Black and Bright Orange (`#ff6b00`) on a sleek grey gradient background with custom in-app confirmation modals and vector space graphics.

---

## 🛠️ Tech Stack

- **Frontend**: React 19, TypeScript, Vite, Tailwind CSS
- **Icons**: Lucide React
- **Backend / Realtime Database**: Firebase Realtime Database & Firebase Authentication

---

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

### 2. Install dependencies

```bash
npm install
```

### 3. Firebase Configuration

Create a `.env` file in the project root based on `.env.example`:

```bash
cp .env.example .env
```

Ensure your Firebase credentials in `src/firebase.ts` or environment variables point to your Firebase Realtime Database project.

### 4. Run Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### 5. Build for Production

```bash
npm run build
```

---

## 🎥 OBS Studio Integration

1. In the app, create or open an active match.
2. In the Controller, click **Functions** > **Copy OBS Overlay Link** (or click the Share icon from the Hub).
3. Open **OBS Studio**.
4. In your scene, add a new source: **Browser**.
5. Paste the copied link into the **URL** field.
6. Recommended dimensions:
   - Width: `600`
   - Height: `800`
7. Check **Shutdown source when not visible** (optional) and click **OK**.
8. The scoreboard HUD will render with a transparent background directly on top of your game feed.
