# LAI Meter – Android app

Leaf Area Index from the phone camera, using the 57.5° gap-fraction method.
The app shows the camera, reads the tilt sensor, captures automatically when the
phone is held at 57.5° ± 1.5° from vertical, and saves readings as CSV to Downloads/LAI.

## Build option A – GitHub (nothing to install)
1. Create a free account on github.com and a new repository (e.g. `lai-meter-app`).
2. "Add file" → "Upload files" → drag in everything inside this folder
   (including the hidden `.github` folder – on a computer use "Show hidden files";
   or create `.github/workflows/build-apk.yml` by hand with "Add file → Create new file").
3. Commit. Open the **Actions** tab – "Build APK" runs automatically (about 5 minutes).
4. When it shows a green tick, open the run → **Artifacts** → download `LAI-Meter-APK`.
5. Unzip, copy `app-debug.apk` to your phone, tap it, and allow "Install unknown apps".

## Build option B – Android Studio on a computer
1. Install Android Studio (developer.android.com/studio).
2. File → Open → select this `LAIMeter` folder. Wait for Gradle sync to finish.
3. Plug in your phone with USB debugging on and press ▶ Run,
   or use Build → Build App Bundle(s)/APK(s) → Build APK(s).

## Changing the app
All of the measuring logic and the screen layout are in
`app/src/main/assets/index.html`. Edit it, rebuild, reinstall.
