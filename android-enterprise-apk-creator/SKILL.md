---
name: "android-enterprise-apk-creator"
description: "Load this skill when the user wants to create a complete native Android APK for enterprise/productivity apps from scratch using AI-generated Kotlin code."
---

# Android Enterprise APK Creator

Use this skill when the user requests to generate a complete native Android application (APK) for enterprise or productivity purposes from scratch.

## Core Purpose
Generate production-ready Android apps for private enterprise use based on natural language prompts.

## Features
- Full Kotlin codebase generation
- MVVM + Clean Architecture
- Room Database for local storage
- Retrofit for external API integration
- Jetpack Compose for UI
- Widgets for home screen
- AI chatbot integration
- Security best practices
- GitHub repository automation

## Example Prompt
Create an Android app for my agropecuaria company. I need to manage crops, fields, expenses, and employees. Include a chatbot assistant, widgets for quick actions, and integration with weather and price APIs.

## Generated Output
- Complete project structure in GitHub repository
- All source code ready to compile
- README with build instructions
- Ready to generate APK

## Requirements
- Android Studio (latest)
- Java JDK 17+
- Android SDK API 34
- GitHub account

## Quick Start
1. Describe your app needs
2. Skill generates all code
3. GitHub repository is created
4. Clone and build: ./gradlew assembleDebug
5. Install: adb install app/build/outputs/apk/debug/app-debug.apk