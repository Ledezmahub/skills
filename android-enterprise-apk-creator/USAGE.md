# Android Enterprise APK Creator - Usage Guide


## Quick Start

Describe the enterprise Android app you want to create:

Example:
Create an Android app for agricultural management with crop tracking, expense management, and a chatbot assistant.

The skill will generate all necessary code and create a GitHub repository.


## Step-by-Step Usage

### Step 1: Describe Your Requirements
Include in your prompt:
- App purpose (e.g., agricultural management, inventory tracking)
- Entities to manage (e.g., crops, expenses, employees, fields)
- Features needed (e.g., chatbot, widgets, API integration)
- Industry type (e.g., agropecuaria, retail, manufacturing)

### Step 2: Answer Clarification Questions
The skill may ask for details like:
- App name
- AI chatbot provider
- Authentication requirements
- Specific API endpoints

### Step 3: Receive Your App
You will receive:
1. GitHub repository URL
2. Setup instructions
3. Build commands


## Example Use Cases

### Agricultural App
Create an Android app for my farm called GreenFields. I need to manage crops, fields, and expenses. Include a chatbot and widgets for quick actions. Integrate with weather and price APIs.

### Inventory Management
Build an inventory app for my store. Track products, stock levels, and sales. Add barcode scanning and offline support.


## Generated Project Structure
android-enterprise-app/
- app/src/main/java/... (all Kotlin code)
- app/build.gradle
- build.gradle
- settings.gradle
- README.md


## Customization
- Modify data models in data/local/entity/
- Change API endpoints in data/remote/api/
- Customize UI in presentation/[feature]/
- Add new features following the same architecture


## Building the APK
Debug APK:
./gradlew assembleDebug

Install:
adb install app/build/outputs/apk/debug/app-debug.apk

Release APK:
./gradlew assembleRelease


## Dependencies Used
- Kotlin (latest stable)
- AndroidX Core, Lifecycle, Activity
- Jetpack Compose (Material Design 3)
- Room Database
- Retrofit 2 + OkHttp 3
- Hilt (Dependency Injection)
- WorkManager
- AndroidX Security