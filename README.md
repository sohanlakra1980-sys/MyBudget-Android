# My Budget V4 — Android App

This is a real Android application wrapper around the working My Budget web app.
It opens the existing GitHub Pages app in an Android WebView, so the Google Sheets / Apps Script backend remains unchanged.

## App
- Name: My Budget
- Package: com.sohanlakra.mybudget
- Version: 4.0
- Portrait mode
- JavaScript + DOM storage enabled
- Internet permission enabled
- Android back button navigates within the app

## Build without installing Android Studio

1. Create a new GitHub repository, e.g. `MyBudget-Android`.
2. Upload the contents of this folder to the repository root.
3. Go to **Actions**.
4. Select **Build My Budget APK**.
5. Click **Run workflow** (or push to `main` to trigger it).
6. When the workflow completes, open the run and download the **MyBudgetV4-APK** artifact.
7. Extract the artifact and install `app-debug.apk` on the Android phone.

The APK is a debug/sideload build. It is suitable for your phone and does not require Play Store publication.

## Existing web app
The app launches:
https://sohanlakra1980-sys.github.io/Monthly-Budget/

The existing Google Apps Script backend in the web app is not changed.

## Why V4 uses an Android wrapper
The web PWA is technically valid on the current device, but Chrome is not exposing `beforeinstallprompt`. A native Android wrapper avoids that browser-install limitation while preserving the existing web app and Sheets backend.


## V4.1 update

The Android app hides the web PWA installation and PWA Status panels.
The Google Sheets backend and existing Budget features are unchanged.
