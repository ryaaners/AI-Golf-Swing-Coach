# 🏌️ AIGolfCoach

An AI-powered golf swing analyzer inspired by [AITennisCoach](https://github.com/Ayan-Mahmood/AITennisCoach).

Drop in a video of your swing and get detailed coaching feedback powered by **Google Gemini 1.5 Flash** — completely free, no credit card needed.

---

## Project Structure

```
AIGolfCoach/
├── model/
│   └── golf_coach.ipynb   ← Main notebook (start here)
├── videos/                ← Put your swing videos here
├── test_video/            ← Sample/test videos
├── frames/                ← Auto-generated (don't touch)
│   └── frames_<video_name>/
│       ├── frame_001.jpg
│       └── ...
├── requirements.txt
└── README.md
```

---

## Quickstart

### 1. Install dependencies
```bash
pip install -r requirements.txt
```

### 2. Get your free Gemini API key
- Go to https://aistudio.google.com
- Sign in with Google → **Get API Key → Create API key**
- Copy the key (starts with `AIza...`)
- Free tier: 15 requests/min, 1,500 requests/day — no card required

### 3. Add your video
Drop your swing video (MP4 works best) into the `videos/` or `test_video/` folder.

### 4. Open the notebook
```bash
jupyter notebook model/golf_coach.ipynb
```

### 5. Run all cells
- Paste your API key in Cell 2
- Set your video filename in Cell 4
- Run all cells top to bottom

---

## How it works

| Step | What happens |
|------|-------------|
| 1 | OpenCV loads your video and reads frame count |
| 2 | 5 frames sampled evenly from 10%–90% of the video |
| 3 | Frames sent to Gemini 1.5 Flash as PIL images |
| 4 | Gemini analyzes setup, backswing, downswing, impact, finish |
| 5 | Full coaching report displayed and saved as Markdown |

---

## Tips for best results

- 🎥 Film from the **side** (down-the-line or face-on)
- ☀️ Good lighting helps the AI see your positions
- 📱 Slow-motion video works great
- 🕐 Clips of **3–10 seconds** work best
- 💾 **MP4 format** is most reliable

---

## Cost

Completely free. Gemini 1.5 Flash has a free tier of 1,500 requests/day with no credit card required.
