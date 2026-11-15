# Memory Match React V4

React + Vite game with responsive navigation, four color themes, 1–4 players, 8/10/20 pairs, timer, scoring, replay, and Chinese pronunciation via browser Web Speech API.

## Run locally

Install Node.js 20+ and run:

```bash
npm install
npm run dev
```

Open the URL printed by Vite.

## Publish to GitHub Pages

The project is configured for repository **memory-match** (`base: '/memory-match/'` in vite.config.js). If the repository name changes, update the base.

1. Run `npm install` and `npm run build`.
2. Publish the **contents of `dist/`** to the root of your GitHub Pages publishing branch, OR use a GitHub Actions workflow (provided in `.github/workflows/deploy.yml`) with Settings → Pages → Source → **GitHub Actions**.
3. The expected address is `https://akarawitawp.github.io/memory-match/` after successful deployment.

**Important:** uploading source files only to a Pages branch will not build React. GitHub Actions will do the build.

## Vocabulary completeness

HSK 1 has **150 words**; HSK 2, 3, and 4 currently have **40 sample words each**, copied from the previous V3 files. This is **not** a complete HSK 2–4 vocabulary dataset. The app displays the exact counts in its level selector and a warning. Replace `src/data/hsk2.json`, `hsk3.json`, and `hsk4.json` with vetted complete datasets in the same `[hanzi, pinyin, english]` format to extend them.

## Audio

Works best in desktop Chrome / Microsoft Edge with a Chinese Mandarin voice installed. Audio uses SpeechSynthesis, so browser/OS voices determine quality. LINE in-app browser and Safari are not guaranteed.

## Features

- Responsive navbar and home/game/how-to views
- Fruit / Car / Mixed / HSK mode-specific background accents
- 1–4 local players, extra turn for successful pair
- Chinese cards with Hanzi, Pinyin and English
- Voice test and replay
- Same-set replay and fresh random set

No server or account needed.
