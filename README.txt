KETCHUP AND DOLL - APK BUILDER
==============================

A tiny Android app (a full-screen WebView) that GitHub builds into an APK for you.
No Android Studio needed.

TWO MODES
- Online (default): loads https://17han5.itch.io/ketchup-and-doll-sim
- Offline: put the game's HTML5 build files in app/src/main/assets/ so that
  index.html is directly inside that folder. The app detects it and runs the
  game from inside the APK.

BUILD IT
1. Make a free account at github.com and create a new repository.
2. Upload everything in this folder to it, including the .github folder.
   (Browser upload is limited to 100 files at a time. For big game builds,
   use GitHub Desktop or git instead.)
3. Open the repository's "Actions" tab. "Build APK" starts automatically.
   When it turns green (a few minutes), open the run and download
   "ketchup-and-doll-apk" from the Artifacts section.
4. Unzip it and install app-debug.apk on your phone
   (allow "install unknown apps" when asked).

If the run fails, open it, copy the error from the red step and send it to Claude.

TWEAKS
- Orientation: app/src/main/AndroidManifest.xml -> android:screenOrientation
- App name: app/src/main/res/values/strings.xml
- Online URL: app/src/main/java/com/example/ketchupdoll/MainActivity.java -> ONLINE_URL
