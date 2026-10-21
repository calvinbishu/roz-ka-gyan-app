# रोज़ का ज्ञान (Roz Ka Gyan)

Daily GK/GS quiz + daily mindset card, for students — Easy / Medium / Hard levels.

## What's here

- `www/index.html` — the whole app (HTML + CSS + JS, no build step, no external JS libraries).
- `.github/workflows/build-apk.yml` — on every push to `main` (or a manual run from the
  **Actions** tab), GitHub's own server wraps `www/` with [Capacitor](https://capacitorjs.com)
  into a native Android project and builds a debug APK — no Android Studio or SDK needed on
  any local machine.

## Getting the APK

1. Go to the **Actions** tab of this repo.
2. Open the latest **Build Android APK** run (green check = success).
3. Under **Artifacts**, download `roz-ka-gyan-debug-apk` — it's a zip containing `app-debug.apk`.
4. Copy the `.apk` to an Android phone and open it to install. Android will warn that it's from
   an unknown source the first time — allow it for this file to sideload.

This is a **debug build**: fine for installing and testing on your own phone, not yet signed
for the Play Store.

## Next steps

- Swap the placeholder app icon for a real one (`android/app/src/main/res/mipmap-*` once the
  workflow has run at least once, or ask Claude to add one to the pipeline).
- Replace the sample questions in the `BANK` object and the `THOUGHTS` list inside
  `www/index.html` with a real, growing question bank.
- Move scores/streaks off on-device storage and onto a backend if the app needs to sync
  across phones.
- For the Play Store: a signed **release** build (not debug) and a Google Play Developer
  account (one-time fee) are needed — ask Claude when you're ready for that step.
