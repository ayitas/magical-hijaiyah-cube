# ✨ Magical Hijaiyah Cube

An interactive 3D educational game to learn **all 28 Hijaiyah (Arabic alphabet)** letters — designed for toddlers.

![Preview](https://img.shields.io/badge/Letters-28%20Hijaiyah-purple) ![Status](https://img.shields.io/badge/Status-Production-green) ![Type](https://img.shields.io/badge/Type-Standalone%20HTML-blue)

## 🎮 Features

- **3D Interactive Cube** — Rounded cube with Hijaiyah letters on each face (Three.js)
- **All 28 Letters** — Organized in 5 groups of 6 (last group: 4 letters + decorative faces)
- **Voice Pronunciation** — Tap the cube to hear each letter spoken in Arabic (Google TTS + Web Speech API fallback)
- **Sound Effects** — Pop, whoosh, sparkle chimes, celebration fanfare, and background lullaby melody (Web Audio API)
- **Smooth Animations** — Squash & stretch, rotation, particle bursts, and floating idle (GSAP)
- **Toddler-Friendly UI** — Large buttons, pastel colors, progress dots, and celebration overlay
- **Auto Group Progression** — Complete a group → brief celebration → automatically loads the next group
- **4 Interactive Game Modes** — Explore, Challenge, Draw, and Sort
- **100% Standalone** — Single `index.html` file (plus one image), no build step
- **Responsive** — Works beautifully on mobile, tablet, and desktop

## 🎯 Game Modes

### 🎲 Explore Mode
Browse through all 28 letters by tapping and rotating the 3D cube. Each letter is spoken aloud with Arabic pronunciation.

### ✏️ Challenge Mode
Listen to each letter's pronunciation and pick the correct Arabic letter from 4 choices. Progress through all 28 letters sequentially.

### 🖌️ Draw Mode
Practice writing Hijaiyah letters! A faded reference letter guides your strokes on the canvas. The app uses pixel-based template matching to validate your drawing — get ≥35% match to advance to the next letter.

### 🧺 Sort Mode
A drag-and-drop mini-game where all 28 Hijaiyah letters appear as apples falling into the grass in batches. Drag each apple into the correct group tree (1 of 5) based on the matching shadow hints and the interactive Hijaiyah Dictionary (Legend). Features batched apple spawning, snap-to-shadow validation on correct drops, bounce-back on wrong drops, and satisfying sound effects.

> Feedback messages are in Indonesian: **"Kamu benar, ayo lanjut!"** (correct) / **"Kamu salah, ayo coba lagi!"** (wrong) / **"Buah ini bukan di pohon yang tepat!"** (wrong sort)

## 🚀 Quick Start

### Option 1: Open Directly
```bash
open index.html
```
> Just double-click `index.html` in your file manager — it works in any modern browser!

### Option 2: Local Server (recommended for audio)
```bash
npx serve .
```

## 📦 Deploy

### Vercel
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy (from project directory)
vercel
```

### Netlify
```bash
# Install Netlify CLI
npm i -g netlify-cli

# Deploy (from project directory)
netlify deploy --prod --dir .
```

### GitHub Pages
1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to **main branch** / root
4. Your site will be live at `https://<username>.github.io/<repo-name>`

## 🗂️ Project Structure

```
magical-hijaiyah-cube/
├── index.html    ← The entire game (single file, ~2800 lines)
└── README.md     ← You are here
```

## 🔤 Letter Groups

| Group | Letters | Range |
|:-----:|---------|-------|
| 1 | ا ب ت ث ج ح | Alif – Ha |
| 2 | خ د ذ ر ز س | Kha – Sin |
| 3 | ش ص ض ط ظ ع | Syin – 'Ain |
| 4 | غ ف ق ك ل م | Ghain – Mim |
| 5 | ن و ه ي | Nun – Ya |

## 🛠️ Tech Stack

| Tech | Usage |
|------|-------|
| [Three.js](https://threejs.org/) v0.160.0 | 3D rendering, raycasting, materials |
| [GSAP](https://greensock.com/gsap/) v3.12.5 | Animations (squash, rotation, particles) |
| Web Audio API | Synthesized SFX & background music |
| HTML5 Canvas | Dynamic texture generation & Draw mode |
| Google TTS / Web Speech API | Arabic letter pronunciation |

## 📄 License

MIT
