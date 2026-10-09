# Midterm Exam: Android Portal App + 3D Pixel Demo
 
**MOBDEV1-L Mobile Application Development Lab**
**Made by Gimbert Ludovice**
 
| | |
|---|---|
| **Name** | Gimbert Ludovice |
| **Section** | 2nd Year, WITMWD3M1 |
| **Professor** | Sir. John Kyle Martin |
| **IDE** | Android Studio Rabbit |
| **Language** | Kotlin (package `com.example.midterm_exam`) |
 
A two-screen Android app built in **Android Studio Rabbit**, plus an HTML5 3D pixel demo (`index.html`) that shows the layout **Design** view, the **Blueprint** view, and the **running phone** side by side. A recorded human voice explains every line of code.
 
## Live Demo
 
Open `index.html` in Chrome or Edge, or use the GitHub Pages link:
`https://<your-github-username>.github.io/<repo-name>/`
 
## Application Tasks (50 points)
 
| # | Task | Module | Where |
|---|------|--------|-------|
| 1 | Layout Construction | 4 | `activity_main.xml` (vertical `LinearLayout`, `EditText`, `Button`) |
| 2 | Explicit Intents & Data Extraction | 6 | `MainActivity` sends `USER_KEY` with `putExtra`; `DashboardActivity` reads it with `getStringExtra` |
| 3 | Activity Lifecycle Tracing | 5 | `onStart()` and `onDestroy()` log to Logcat with tag `Lifecycle` |
| 4 | State Preservation on Rotation | 5 | `onSaveInstanceState()` saves `COUNTER_KEY`, restored in `onCreate()` |
| 5 | Implicit Intents | 6 | "Visit School Site" uses `Intent.ACTION_VIEW` to open `https://trimexcolleges.edu.ph` |
 
## Project Structure
 
```
app/src/main/
├── java/com/example/midterm_exam/
│   ├── MainActivity.kt
│   └── DashboardActivity.kt
├── res/layout/
│   ├── activity_main.xml
│   └── activity_dashboard.xml
└── AndroidManifest.xml        (DashboardActivity registered)
index.html                     (3D pixel demo with recorded voice narration)
README.md
```
 
## How to Run the Android App
 
1. Open the project in **Android Studio Rabbit**.
2. Sync Gradle and select an emulator or device.
3. Press **Run**.
4. Test: enter a name, tap **Enter Dashboard**, tap **Add Click**, rotate the device (the count stays), then tap **Visit School Site** (the browser opens).
5. Filter Logcat by `Lifecycle` to see the `onStart` and `onDestroy` logs.
Tested on: HUAWEI TXZ-W09 emulator, API 31.
 
## 3D Pixel Demo (`index.html`)
 
- **Run**: installs the app on the demo phone; Design and Blueprint views update live.
- **Rotate phone**: shows that the click counter survives rotation.
- **Visit School Site**: opens an in-phone browser screen (implicit intent), with a button to open the real site.
- **Enable Sound**, then **Play full explanation**: a recorded voice explains every line of `MainActivity.kt` and `DashboardActivity.kt`. Click any line to hear just that one.
> The demo is a browser simulation of the app for explanation purposes. The real app runs in Android Studio.
 
## Tech
 
Kotlin · Android SDK · AndroidX AppCompat · XML layouts · Android Studio Rabbit · HTML5 / CSS3 3D transforms
 
---
© Gimbert Ludovice, 2nd Year, WITMWD3M1
