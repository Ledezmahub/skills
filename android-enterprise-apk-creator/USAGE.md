# Android Enterprise APK Creator - Usage Guide

## Quick Start

Describe the enterprise Android app you want to create.

Example: Create an Android app for agricultural management with crop tracking, expense management, and a chatbot assistant.

The skill will generate all code and create a GitHub repository.

## Usage

### Step 1: Describe Requirements
Include:
- App purpose
- Entities to manage
- Features needed
- Industry type

### Step 2: Answer Questions
The skill may ask:
- App name?
- Chatbot provider?
- Authentication?
- API endpoints?

### Step 3: Receive App
You get:
- GitHub repository URL
- Setup instructions
- Build commands

## Examples

### Agricultural App
Prompt: Create an Android app for my farm. I need to manage crops, fields, expenses, and employees. Include chatbot, widgets, weather and price API integration.

### Inventory Management
Prompt: Build an inventory app. Track products, stock levels, suppliers, and sales. Add barcode scanning and offline support.

## Project Structure
app/
- src/main/java/... (Kotlin code)
- src/main/res/ (resources)
- build.gradle

- build.gradle (project)
- settings.gradle
- README.md

## Customization
- Modify data models in data/local/entity/
- Change API endpoints in data/remote/api/
- Customize UI in presentation/[feature]/

## Building
Debug: ./gradlew assembleDebug
Install: adb install app/build/outputs/apk/debug/app-debug.apk
Release: ./gradlew assembleRelease

## Dependencies
- Kotlin
- AndroidX Core/Lifecycle/Activity
- Jetpack Compose
- Room
- Retrofit + OkHttp
- Hilt
- WorkManager
- AndroidX Security

## Support
Check README.md for detailed instructions.