# LAI Meter – Android app

Leaf Area Index from the phone camera. Maintained by LARG.

- Normal mode: single-angle gap fraction at 57.5°, auto-capture when the phone is on target.
- Fisheye mode: clip-on 180° lens, phone flat and camera up, five LI-COR-style zenith rings.
- GPS position, accuracy and altitude saved with each reading (photo GPS used for uploads).
- Map view of readings coloured by LAI (satellite / street map; needs internet).
- Readings kept on the phone until cleared; CSV saved to Downloads/LAI.
- Menu: "How the number is computed" and Settings.

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
`app/src/main/assets/index.html` (map library: leaflet.js / leaflet.css in the same folder). Edit it, rebuild, reinstall.
