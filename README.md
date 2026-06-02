# 🏌️ AIGolfCoach

An AI-powered golf swing analyzer


## How it works

| Step | What happens |
|------|-------------|
| 1 | OpenCV loads your video and reads frame count |
| 2 | 5 frames sampled evenly from 10%–90% of the video |
| 3 | Frames sent to Gemini 1.5 Flash as PIL images |
| 4 | Gemini analyzes setup, backswing, downswing, impact, finish |
| 5 | Full coaching report displayed and saved as Markdown |
