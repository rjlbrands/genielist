# .cursorrules

## Project Overview

*   **Type:** cursorrules_file
*   **Description:** I want to build an iOS mobile app for keeping track of your life to manage daily tasks, reminders, to-dos, note keeping, and lists. The app keeps track of important events, items in the users lists, sends helpful notifications for said items, and offers simple tools for staying organized. GenieList is designed with a magical, approachable UI featuring gradients, bold icons, glassmorphism, and fun animations.
*   **Primary Goal:** Develop GenieList, an iOS app that provides an intuitive, magical task management experience with real-time cloud backup, seamless collaboration, calendar integration, and optional AI-driven productivity suggestions.

## Project Structure

### Framework-Specific Routing

*   **Directory Rules:**

    *   SwiftUI (iOS): Utilize a modular structure based on SwiftUI's NavigationStack and View composition. Organize feature-specific views into dedicated subfolders (e.g. Onboarding, Dashboard, Tasks, Genie) to align with SwiftUI's declarative routing.
    *   Example 1: "SwiftUI iOS" → `Views/Onboarding/ContentView.swift` as the entry point for the onboarding flow.
    *   Example 2: "SwiftUI Navigation" → `Views/Dashboard/DashboardView.swift` representing the main dashboard after login.
    *   Example 3: "Xcode Project Structure" → Standard Xcode directories like `Assets.xcassets` for design assets.

### Core Directories

*   **Versioned Structure:**

    *   Views: Contains SwiftUI view files implementing the magical UI, animations, and user interactions.
    *   Models: Houses data structures for users, tasks, reminders, notes, and events.
    *   ViewModels: Implements business logic and state management following the MVVM pattern to bind Models and Views.
    *   Services: Manages integrations with Supabase for authentication and cloud backup, Apple Calendar for event syncing, and optional AI modules for intelligent productivity suggestions.

### Key Files

*   **Stack-Versioned Patterns:**

    *   ContentView.swift: The main entry point leveraging SwiftUI’s NavigationStack for smooth transitions between screens.
    *   AppDelegate.swift: Handles critical app lifecycle events and service initializations.
    *   GenieView.swift: Dedicated view for the AI-powered Genie tab that activates smart suggestions and magical animations.

## Tech Stack Rules

*   **Version Enforcement:**

    *   SwiftUI@Latest: Enforce usage of SwiftUI’s modern declarative syntax and navigation paradigms.
    *   Xcode@Latest: Use the latest stable version of Xcode to support current iOS features and optimize development workflows.
    *   Supabase@Current: Require Supabase for authentication, user data management, and cloud backup integrations as per project requirements.

## PRD Compliance

*   **Non-Negotiable:**

    *   "GenieList is an iOS mobile app designed to help users keep track of their everyday life by managing daily tasks, reminders, to-dos, notes, and lists." : The app must integrate real-time cloud backup, seamless task collaboration, intuitive calendar syncing, and optional AI suggestions, all while delivering a magical, user-friendly experience.

## App Flow Integration

*   **Stack-Aligned Flow:**

    *   SwiftUI Onboarding Flow → `Views/Onboarding/ContentView.swift` initiates user account creation, onboarding tutorials, and transitions into the dashboard.
    *   Dashboard Flow → `Views/Dashboard/DashboardView.swift` centralizes task management, note taking, and event viewing.
    *   Genie Tab Flow → `Views/Genie/GenieView.swift` activates server-driven AI suggestions and magical UI effects for enhanced productivity.
