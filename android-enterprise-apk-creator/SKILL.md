---
name: "android-enterprise-apk-creator"
description: "Load this skill when the user wants to create a complete native Android APK for enterprise/productivity apps from scratch using AI-generated Kotlin code. Handles architecture, UI, databases, APIs, widgets, security, and GitHub integration for private use."
---

# Android Enterprise APK Creator

**Use this skill** when the user requests to generate a **complete native Android application (APK)** for **enterprise or productivity purposes** from scratch.

## Core Purpose
Generate **production-ready Android apps** for private enterprise use (no Play Store publishing) based on **natural language prompts**. The output is a **complete GitHub repository** with all code ready to compile into an APK.

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
Create an Android app for my agropecuaria company. I need to manage crops, fields, expenses, and employees. Include a chatbot assistant, widgets for quick actions, and integration with weather and price APIs. The app will be used privately by my company only.

## Generated Output
- Complete project structure in GitHub repository
- All source code (Kotlin, Jetpack Compose, Room, Retrofit, Hilt)
- README with build instructions
- Ready to compile and generate APK

## Requirements
- Android Studio (latest)
- Java JDK 17+
- Android SDK API 34
- GitHub account

## Quick Start
1. Describe your app needs
2. Skill generates all code
3. GitHub repository is created automatically
4. Clone and build: ./gradlew assembleDebug
5. Install on device: adb install app/build/outputs/apk/debug/app-debug.apk

## Architecture
- MVVM + Clean Architecture
- Data Layer: Entities, DAOs, Repositories, API Services
- Domain Layer: Use Cases, Domain Models
- Presentation Layer: ViewModels, Composable Screens, Navigation
- Widgets: AppWidgetProvider for home screen
- Chatbot: Integrated assistant with app context

## Security
- EncryptedSharedPreferences for sensitive data
- SSL Pinning for API calls
- ProGuard/R8 obfuscation for release builds
- Runtime permission requests

## Templates Included
All templates for generating Android app code:
- entity_template.txt
- dao_template.txt
- repository_template.txt
- usecase_template.txt
- viewmodel_template.txt
- api_service_template.txt
- composable_screen_template.txt
- database_template.txt
- hilt_module_template.txt
- README_template.md

## Files Structure
android-enterprise-apk-creator/
- SKILL.md (main skill file)
- USAGE.md (usage guide)
- prompt_processor.md (prompt processing logic)
- config/skill_config.yaml (configuration)
- templates/*.txt and *.md (code templates)