# Substring Finder — app source code

This source bundle has three versions of the same DFA substring finder.

## Web app

The live web app is [Substring Finder](https://udaydhoke468.github.io/Substring-Finder/). It runs the DFA in the browser and works without a Python server. The `web` folder keeps the Python API server version for local use.

Open `web` in File Explorer and double-click `start.bat`. It starts the Python backend and opens the browser at http://127.0.0.1:8000. Keep the server terminal open. The browser frontend and backend are connected through `POST /api/simulate`.

## Windows desktop app

Requires Python 3 with Tkinter. Double-click `windows/run_windows.bat` or run `python substring_finder.py` from that folder. For an optional standalone EXE, follow `windows/README.md`.

## Android app

Install Android Studio with Android SDK Platform 36 and JDK 17. Open the `android` folder in Android Studio, wait for Gradle sync, select a phone or emulator, and press **Run**. To make an APK, select **Build > Build APK(s)**. The native Java app runs the DFA locally and works offline.

All three versions include Run, Load example, Reset/Clear, overlapping match counting, transition display, and step controls.

The Android build uses Android Gradle Plugin 9.4.0 and Gradle 9.6.0, per the [official compatibility table](https://developer.android.com/build/releases/about-agp). Android sources are provided; an APK was not built because Android Studio, Java, and Android SDK are not installed in this environment.

