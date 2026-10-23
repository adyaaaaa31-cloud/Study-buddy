# Smart College Buddy — Android starter project

A simple student utility app built with Kotlin and Jetpack Compose.

## Included features
- Home dashboard
- Attendance percentage calculator
- Quick notes (currently stored in memory only; notes clear when the app process is closed)
- 25-minute study focus timer

## Open and run
1. Install Android Studio on a computer.
2. Extract this ZIP file.
3. In Android Studio, choose **Open** and select the extracted `SmartCollegeBuddy` folder.
4. Allow Gradle sync to finish. Use JDK 17 if Android Studio asks for a Gradle JDK.
5. Connect an Android phone with USB debugging enabled, or start an emulator.
6. Press **Run ▶**.

## Build an APK
In Android Studio, use **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
The debug APK is normally created at:
`app/build/outputs/apk/debug/app-debug.apk`

## Notes
- This is starter source code, not a prebuilt APK.
- Internet access is not required by the app.
- It does not send messages, create notifications, or sync data to the cloud.
- If Gradle reports a plugin or SDK download issue, connect to the internet and install Android SDK Platform 35 from SDK Manager.


## Build APK automatically with GitHub Actions

The project includes `.github/workflows/android.yml`.

1. Create a new repository on GitHub.
2. Upload/push all project files to the repository (including the `.github` folder).
3. Open the repository's **Actions** tab.
4. Select **Android CI and APK**, then click **Run workflow** (or push to `main` / `master`).
5. When the workflow finishes, open the successful run and download the `SmartCollegeBuddy-debug-apk` artifact.

The downloaded artifact is a debug APK for testing, not a Play Store release. GitHub Actions needs to download Android SDK/build dependencies, so the first run can take a few minutes.

Note: GitHub-hosted runners usually have Gradle installed. The workflow generates a Gradle wrapper if the repository does not include one.
