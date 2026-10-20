# Video Maker

Type a topic and get a short vertical video (9:16) with captions. AI writes the script, and your browser builds the video. No server, no sign-up, no paid video API.

**Live demo:** https://seven25-ui.github.io/video-maker/

## What it does

- Writes a scene-by-scene script from your topic using the Gemini API
- Supports Bisaya, Tagalog, and English
- Three styles: Promo, Facts, and Story
- Choose 4, 5, 6, or 8 scenes
- Optional: upload your own photos to use as scene backgrounds
- Previews the video in the browser, with a spoken narration option
- Downloads the finished video as a `.webm` file

## How to use

1. Open the live demo.
2. Open **One-time setup** and paste your free Gemini API key (get one at [aistudio.google.com](https://aistudio.google.com)).
3. Type a topic, for example: `3 tips to make your sari-sari store sell more`.
4. Pick a language, style, and number of scenes.
5. Press **Make video**.
6. Use **Play with voice** to hear the narration, or **Download video** to save the file.

## Privacy and your API key

Your API key is stored only in your own browser (`localStorage`). It is never written into the code or sent anywhere except directly to Google's Gemini API. Do not paste your key into `index.html` or commit it to GitHub.

## Limitations

- The downloaded video has captions but **no voice**. Browsers cannot record text-to-speech audio. Voice plays in the preview only.
- Voices come from your browser. There is no true Bisaya voice, so Bisaya narration is read with a Filipino voice.
- Video recording works best in Chrome, Edge, or Brave. Some browsers do not support recording.
- The default model is `gemini-3.5-flash`. If you get a "model not found" error, change the model name in the setup box to `gemini-flash-latest`.

## Tech

Single-file app: plain HTML, CSS, and JavaScript. Uses the Canvas API for drawing scenes, `MediaRecorder` for recording, the Web Speech API for the voice preview, and the Gemini API for script writing.

## Run locally

Open `index.html` in a browser. Or host it free with GitHub Pages: **Settings → Pages → Deploy from a branch → `main` / root**.

## Ideas for next versions

- Background music in the recording
- More styles, colors, and a custom logo or watermark
- Choose video length and 16:9 format
- Store the API key in a serverless proxy so visitors do not need their own key
