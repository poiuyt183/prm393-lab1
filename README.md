# PRM393 – Lab 1

## Table of Contents

- [PRM393 – Flutter Lab 1](#prm393--flutter-lab-1)
  - [Exercise 1: Environment Setup](#exercise-1-environment-setup)
    - [Flutter Doctor](#flutter-doctor)
    - [Android Studio Flutter/Dart Plugins](#android-studio-flutterdart-plugins)
  - [Exercise 2: Flutter Project Overview](#exercise-2-flutter-project-overview)
    - [Project Structure](#project-structure)
    - [Running Counter App](#running-counter-app)
    - [Hot Reload Demonstration](#hot-reload-demonstration)
  - [Exercise 3: Flutter Source Code](#exercise-3-flutter-source-code)
  - [Exercise 4: Conceptual Questions](#exercise-4-conceptual-questions)
    - [1. What is the purpose of the flutter doctor command?](#1-what-is-the-purpose-of-the-flutter-doctor-command)
    - [2. What file acts as the entry point of a Flutter application?](#2-what-file-acts-as-the-entry-point-of-a-flutter-application)
    - [3. Explain the difference between Hot Reload and Hot Restart.](#3-explain-the-difference-between-hot-reload-and-hot-restart)
    - [4. How does runapp build the widget tree?](#4-how-does-runapp-build-the-widget-tree)
    - [5. Describe how Flutter’s architecture enables cross-platform development.](#5-describe-how-flutters-architecture-enables-cross-platform-development)


## Exercise 1: Environment Setup

### Flutter Doctor

The `flutter doctor` command was executed to verify that the Flutter SDK and all required dependencies are correctly installed and configured.

<img src="/Exercise1.png" alt="Flutter Doctor Output" width="800"/>

### Android Studio Flutter/Dart Plugins

The Flutter and Dart plugins were successfully installed and enabled in Android Studio to support Flutter development.

<img src="/Exercise1(2).png" alt="Flutter & Dart Plugins" width="800"/>

---

## Exercise 2: Flutter Project Overview

### Project Structure

The default Flutter project structure was explored to understand the role of each folder and file.

<img src="/ProjectStructure.png" alt="Project Structure" width="700"/>

### Running Counter App

The default Flutter Counter App was successfully built and executed on an emulator/device.

<img src="/RunningCounterApp.png" alt="Running Counter App" width="400"/>

### Hot Reload Demonstration

Hot Reload was tested by making UI changes and observing instant updates without restarting the application.

<img src="/HotReload.png" alt="Hot Reload Example" width="400"/>
---

## Exercise 3: Flutter Source Code

The main Flutter application code can be found at:

[main.dart](hello_flutter_lab1/lib/main.dart)

---

## Exercise 4: Conceptual Questions

### 1. What is the purpose of the `flutter doctor` command?

`flutter doctor` is a diagnostic tool used to check the Flutter development environment.  
It verifies whether the Flutter SDK, Android SDK, connected devices, and required tools are correctly installed and reports any issues that need to be fixed.

---

### 2. What file acts as the entry point of a Flutter application?

The entry point of a Flutter application is:
```
lib/main.dart
```

### 3. Explain the difference between Hot Reload and Hot Restart.

| Feature | Hot Reload | Hot Restart |
|------|-----------|-------------|
| Speed | Very fast | Slower |
| App state | Preserved | Reset |
| Use case | UI changes, small logic updates | State or initialization changes |

- **Hot Reload** injects updated code into the running app without restarting it.
- **Hot Restart** rebuilds the app from scratch and resets the application state.

### 4. How does `runApp()` build the widget tree?

`runApp()` takes a widget as its argument and attaches it to the screen.  
This widget becomes the **root of the widget tree**. Flutter then recursively builds all child widgets, creating a hierarchical structure that defines the entire UI.

Example:
```dart
void main() {
  runApp(MyApp());
}
```
### 5. Describe how Flutter’s architecture enables cross-platform development.

Flutter uses a single codebase written in Dart and renders UI using its own high-performance rendering engine (Skia).
Instead of relying on native UI components, Flutter draws everything itself, ensuring consistent behavior and appearance across platforms such as Android, iOS, Web, and Desktop.


