# Prompt Processor for Android Enterprise APK Creator

This document defines how the skill processes user prompts to generate enterprise Android applications.

## Prompt Processing Pipeline
User Prompt -> Tokenization -> Entity Extraction -> Requirement Analysis -> Code Generation -> GitHub Deployment


## Step 1: Prompt Analysis
The skill accepts prompts in natural language, structured requests, or feature lists.

## Step 2: Entity and Feature Extraction
The skill identifies:
- App metadata (name, purpose, company)
- Data entities (crops, expenses, employees, fields, etc.)
- Features (chatbot, widgets, API integration, etc.)
- External APIs (weather, prices, payment, etc.)

### Entity Keywords Mapping
- crop, crops, planting, harvest -> Crop
- expense, expenses, cost, costs -> Expense
- employee, employees, worker -> Employee
- field, fields, land, plot -> Field
- inventory, stock, items -> Inventory
- task, tasks, todo -> Task
- customer, customers -> Customer
- supplier, suppliers -> Supplier
- order, orders -> Order
- report, reports -> Report
- project, projects -> Project

### Feature Keywords
- chatbot, ai, assistant -> AI Chatbot
- widget, widgets -> App Widgets
- api, external, integration -> API Integration
- offline, sync -> Offline Sync
- authentication, login -> Authentication
- search, filter -> Search
- export, import -> Data Export
- notification -> Notifications
- map, maps -> Maps Integration

## Step 3: Requirement Analysis
Organizes extracted information into:
- App configuration
- Data models
- Features
- External integrations

## Step 4: Code Generation
Generates:
1. Database and Entities
2. API Layer
3. Repository Layer
4. Domain Layer
5. Presentation Layer
6. Dependency Injection
7. Widgets
8. Chatbot
9. Configuration files

## Step 5: Contextual Generation
For agricultural apps: generates specific entities like Crop, Field, Expense with agricultural categories.
For general enterprise apps: generates flexible structure with customizable data models.

## UI Generation Rules
- List, Detail, Add, Edit screens for each entity
- Dashboard with stats
- ChatScreen for chatbot
- ReportsScreen for analytics

## Widget Generation
- Quick Actions Widget (2x1 or 4x1)
- Statistics Widget (2x2)
- List Widget (4x2)

## Chatbot Integration
- Natural language understanding
- Context from app data
- Predefined commands: /help, /expenses, /crops, /sync, /summary, /predict
- Example queries: Show me crops planted in March, What are my total expenses?

## Security Implementation
- EncryptedSharedPreferences for sensitive data
- SSL Pinning for API calls
- ProGuard/R8 obfuscation
- Runtime permission requests

## GitHub Integration
- Creates private repository
- Commits all generated files
- Provides repository URL and instructions

## Example: Full Prompt Processing
Input: Create an Android app for my agropecuaria company called FarmManager. I need to manage crops, fields, expenses, and employees. The app should have a chatbot assistant and widgets. Integrate with weather and price APIs.

Extracted:
- Entities: Crop, Field, Expense, Employee
- Features: Chatbot, Widgets, WeatherIntegration, PricesIntegration
- APIs: WeatherApi, AgriculturalPricesApi

Generated Files:
- Entity classes (Crop.kt, Field.kt, Expense.kt, Employee.kt)
- DAO interfaces
- Repository implementations
- Use Cases
- ViewModels
- Composable Screens
- Widget providers
- Chatbot components
- Gradle files
- AndroidManifest.xml
- README.md

## Tips for Effective Prompts
- Be specific about app purpose
- List the entities you need to manage
- Mention integrations (APIs, services)
- Describe features you want
- Specify industry

## Clarification Questions
If prompt is ambiguous, the skill should ask:
- What would you like to name your app?
- Should the chatbot use a local LLM or external AI service?
- Do you need user authentication?
- For the API integration, do you have a specific API in mind?
- Should the app work offline?
- Should the app sync data with a cloud service?