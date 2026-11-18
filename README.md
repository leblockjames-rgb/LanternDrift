# Lantern Drift (Android)

A full-screen WebView wrapper that runs the game from `app/src/main/assets/index.html`.

## Build with GitHub (no install needed)
1. Create a new repository on GitHub and upload everything in this folder (keep the `.github` folder).
2. Open the **Actions** tab. The "Build APK" workflow runs on every push (or press **Run workflow**).
3. When it finishes (about 3 to 5 minutes), open the run and download **LanternDrift-apk**. Unzip it to get `app-debug.apk`.

## Build with Android Studio
1. File > Open, pick this folder, and let Gradle sync.
2. Build > Build App Bundle(s) / APK(s) > Build APK(s).
3. The APK is in `app/build/outputs/apk/debug/`.

## Install on a phone
Copy the APK to the phone, open it, and allow "Install unknown apps" when asked.

## Publishing on Google Play
Play needs a signed release bundle (`.aab`), not the debug APK. In Android Studio use
Build > Generate Signed App Bundle / APK, and keep the keystore safe: you need it for every update.

## Updating the game
Replace `app/src/main/assets/index.html` with the new version and bump `versionCode` in `app/build.gradle`.
