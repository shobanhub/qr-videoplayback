# QR Video Playback (native Android, no HTML)

Each workflow is its own screen (Activity), built in Java.

| Screen | File | Access |
|---|---|---|
| Entry (mode + camera permission) | EntryActivity | all |
| Workflow menu | HomeActivity | all |
| Scan (CameraX + ZXing, gallery scan) | ScannerActivity | Viewer, Generator |
| Video (local file or link) | PlayerActivity | Viewer, Generator |
| History | HistoryActivity | Generator |
| Make QR + share image | GeneratorActivity | Generator |

Helpers: `Ui.java` (shared look), `Store.java` (history).
Scans lead on to the next workflow: Scan/History -> Play video, Make QR.

## Build
- Android Studio (JDK 17): open this folder, Build > Build APK(s).
- CLI: `gradle assembleDebug` (Gradle 8.7, Android SDK 34).
- GitHub: push, run Actions > Build APK, download the artifact.
Output: `app/build/outputs/apk/debug/app-debug.apk`
