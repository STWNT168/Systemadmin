# Ops Log — Android APK

System admin work order tracker, packaged as a Cordova Android app.

## Get the APK (no local Android setup needed)

1. Create a new GitHub repo.
2. Upload all files from this zip, keeping the folder structure (`.github/workflows/build-apk.yml` must stay at that exact path).
3. Push to `main`.
4. Go to the repo's **Actions** tab → the "Build APK" workflow runs automatically.
5. When it finishes (green check, ~3-4 min), open the workflow run → **Artifacts** → download `ops-log-apk`. Unzip it to get `app-debug.apk`.
6. Copy `app-debug.apk` to your phone and install it (you'll need to allow "install unknown apps" for whatever app you use to open it).

## Notes

- This builds a **debug** APK — fine for personal/sideloaded use. It is not signed for Play Store distribution.
- Data is stored locally on your phone (`localStorage` inside the app's WebView). It does not sync anywhere or leave the device.
- To rebuild after editing `www/index.html`, just push again — the workflow reruns automatically.
- App id: `com.lalit.opslog`. Change it in `config.xml` if you want a different package name.
