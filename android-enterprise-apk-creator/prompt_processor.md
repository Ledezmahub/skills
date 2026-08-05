# Prompt Processor for Android Enterprise APK Creator

## Prompt Processing Pipeline
User Prompt -> Tokenization -> Entity Extraction -> Requirement Analysis -> Code Generation -> GitHub Deployment


## Step 1: Prompt Analysis
Accepts natural language descriptions, structured requests, or feature lists.

## Step 2: Entity and Feature Extraction
Identifies:
- App metadata (name, purpose, company)
- Data entities (crops, expenses, employees, fields, inventory, tasks, etc.)
- Features (chatbot, widgets, API integration, offline sync, etc.)
- External APIs (weather, prices, payment, maps, etc.)

## Entity Keywords
- crop, crops, planting, harvest -> Crop
- expense, expenses, cost, costs -> Expense
- employee, employees, worker -> Employee
- field, fields, land, plot -> Field
- inventory, stock, items -> Inventory
- task, tasks, todo -> Task
- customer, customers -> Customer
- supplier, suppliers -> Supplier
- order, orders -> Order
- project, projects -> Project

## Feature Keywords
- chatbot, ai, assistant -> AI Chatbot
- widget, widgets -> App Widgets
- api, external, integration -> API Integration
- offline, sync -> Offline Sync
- authentication, login -> Authentication
- search, filter -> Search
- export, import -> Data Export

## Step 3: Requirement Analysis
Organizes into:
- App configuration
- Data models
- Features
- External integrations

## Step 4: Code Generation
Order:
1. Database and Entities
2. API Layer
3. Repository Layer
4. Domain Layer
5. Presentation Layer
6. Dependency Injection
7. Widgets
8. Chatbot
9. Configuration

## Step 5: Contextual Generation
For agricultural apps: Crop, Field, Expense, Employee, Inventory, Task with agricultural-specific features.
For general apps: Flexible structure with customizable data models.

## Chatbot Integration
- Natural language understanding
- Context from app data
- Commands: /help, /expenses, /crops, /sync, /summary, /predict
- Example queries: Show me crops planted in March, What are my total expenses?

## Security Implementation
- EncryptedSharedPreferences
- SSL Pinning
- ProGuard/R8
- Runtime permissions

## GitHub Integration
- Creates private repository
- Commits all files
- Provides URL and instructions

## Example Full Processing
Input: Create an Android app for my agropecuaria company called FarmManager. I need to manage crops, fields, expenses, and employees. The app should have a chatbot assistant and widgets. Integrate with weather and price APIs.

Extracted:
- Entities: Crop, Field, Expense, Employee
- Features: Chatbot, Widgets, WeatherIntegration, PricesIntegration
- APIs: WeatherApi, AgriculturalPricesApi

Generated: Entity classes, DAOs, Repositories, Use Cases, ViewModels, Screens, Widgets, Chatbot, Gradle files, README

## Tips for Effective Prompts
- Be specific about app purpose
- List entities you need to manage
- Mention integrations
- Describe features
- Specify industry

## Clarification Questions
- What would you like to name your app?
- Should the chatbot use a local LLM or external AI service?
- Do you need user authentication?
- For the API integration, do you have a specific API in mind?
- Should the app work offline?