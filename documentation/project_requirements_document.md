# Project Requirements Document (PRD) – GenieList

## 1. Project Overview

GenieList is an iOS mobile app designed to help users keep track of their everyday life by managing daily tasks, reminders, to-dos, notes, and lists. The app is built to allow users to easily track important events and items, receive helpful notifications, and use simple yet powerful tools for staying organized. Its overall design emphasizes a magical, approachable experience with fun animations and unique visual elements like gradients and glassmorphic UI, making task management engaging and delightful.

The app is being built to replace an existing beta version, offering a more robust and refined experience that appeals to busy parents, working professionals, college students, or anyone in need of a smarter way to organize their schedules. Key objectives include seamless synchronization across devices through cloud backups, effective collaboration features, and optional AI integrations for personalized productivity tips and smart notifications. Success will be measured by how intuitively users can manage their tasks and the effectiveness of the app's magical, user-friendly design in enhancing productivity.

## 2. In-Scope vs. Out-of-Scope

**In-Scope:**

*   iOS mobile application development using SwiftUI.
*   Custom to-do lists, note-taking, and event management with calendar integration (Apple Calendar and optional Google Calendar sync).
*   Push notifications for reminders and due dates.
*   Cloud backup that automatically syncs data upon any changes and performs daily backups.
*   Optional AI suggestions (via GPT-4o or Claude 3.5 Sonnet) for productivity tips, task prioritization, and list generation.
*   Real-time collaboration features that allow users to share tasks, lists, and events through email invitations or unique share links with role-based permissions.
*   A template marketplace for users to share and use pre-made to-do templates.
*   A magical and engaging UI with smooth transitions, animations, bold icons, and fun visual effects.
*   Use of Supabase for authentication, data storage, and backend operations.
*   Integration of advanced development tools (Xcode and Cursor) for a seamless coding and development process.

**Out-of-Scope:**

*   Android or cross-platform app development; this version focuses solely on the iOS ecosystem.
*   Complex third-party integrations beyond Apple Calendar and basic Google Calendar support.
*   Extensive offline functionality beyond the basic offline data access provided by local caching (primary focus is online backup/sync with the cloud).
*   Any non-app related website or desktop versions at launch.
*   Expanding to community social features beyond the template marketplace and basic collaboration.

## 3. User Flow

A typical user starts by creating an account using their email and secure password, managed by Supabase, ensuring that their profile, tasks, reminders, notes, and settings (like notification preferences) are safely stored. After a simple onboarding process that introduces key features and the magical design elements, the user lands on an intuitive dashboard where all major functionalities are readily accessible on the home screen. From here, users can navigate through a side or bottom menu to access custom to-do lists, calendar events, note-taking sections, and the Genie tab for optional AI suggestions.

Once inside the dashboard, a user will easily add or edit tasks, set reminders with push notifications, and view upcoming events integrated from Apple Calendar (and optionally Google Calendar). Collaboration is straightforward: a user can share tasks or lists in real time by sending an invite via email or a share link, with the app providing role-based permissions like Viewer, Editor, or Admin. The flow is designed to be smooth and magical—for example, with delightful animations when a task is completed or when a new note is added—helping users feel motivated and engaged throughout their day.

## 4. Core Features

*   **Custom To-Do Lists:**\
    Users can create, edit, and manage multiple custom to-do lists tailored for different aspects of their lives.
*   **Push Notifications:**\
    Timely reminders for tasks and due dates, with customizable alert settings to keep users on track.
*   **Calendar Integration:**\
    Seamlessly sync events with Apple Calendar, along with optional Google Calendar support for added flexibility.
*   **Simple Note-Taking:**\
    Quick and easy note-taking features for jotting down ideas, grocery lists, or other notes.
*   **Cloud Backup & Automatic Sync:**\
    Continuous syncing of all user data (tasks, notes, reminders, events) in real-time, with scheduled daily backups to ensure data integrity and availability across devices.
*   **Optional AI Suggestions:**\
    Leverage GPT-4o or Claude 3.5 Sonnet for smart productivity tips, generating list suggestions, and offering reminders based on user habits. These suggestions can be activated via a dedicated “Genie” tab or set to trigger automatically.
*   **Real-Time Collaboration:**\
    Enable users to share and work on lists or tasks together through email invitations or share links, with role-based permissions (Viewer, Editor, Admin) and real-time syncing of updates.
*   **Template Marketplace:**\
    A dedicated section where users can find, share, and use templates for to-do lists and other organizational frameworks, including premium templates available through in-app purchases.

## 5. Tech Stack & Tools

*   **Frontend Framework:**\
    SwiftUI for building the iOS user interface with engaging animations and polished visuals.
*   **Backend & Storage:**\
    Supabase will manage authentication, database storage, and real-time data syncing. It will securely store user profiles, tasks, notes, reminders, and settings.
*   **Calendar Integration:**\
    Integration with Apple Calendar (primary) and optional Google Calendar support for syncing events.
*   **AI Integration:**\
    Optional modules using GPT-4o or Claude 3.5 Sonnet to provide intelligent productivity suggestions. The AI integration will enhance user experience by offering tailored advice and smart notifications.
*   **Development Environment:**\
    Xcode as the primary IDE for iOS development.
*   **Coding Assistance:**\
    Cursor for advanced AI-powered coding suggestions and real-time development tips.

## 6. Non-Functional Requirements

*   **Performance:**\
    The app should ensure smooth animations and transitions with minimal lag, responding quickly (within 1-2 seconds) to user interactions.
*   **Security:**\
    User data must be stored securely using Supabase’s authentication mechanisms, following encryption protocols for data in transit and at rest. Satisfy regulations such as GDPR, CCPA, and Apple’s App Store guidelines.
*   **Usability:**\
    The user interface should be intuitive and accessible, featuring easy-to-read text, prominent buttons, and a user-directed navigation system. Maintain the magical aesthetic with fun yet subtle animations.
*   **Reliability:**\
    Ensure that cloud backup and synchronization work seamlessly, with backup intervals on change and scheduled daily backups to prevent data loss.
*   **Scalability:**\
    The backend should efficiently handle increasing user numbers and real-time collaboration updates without performance degradation.

## 7. Constraints & Assumptions

*   **Platform Constraint:**\
    Focus solely on the iOS platform, using SwiftUI. This means that Android or cross-platform support is out of scope for this version.
*   **Cloud & AI Dependency:**\
    The app relies on Supabase for data management and cloud backup, and on AI models like GPT-4o or Claude 3.5 Sonnet for smart suggestions. Their availability, performance, and rate limits are assumed to be stable.
*   **User Data Regulation:**\
    The app must comply with GDPR, CCPA, and Apple's privacy guidelines. It is assumed that the team will work with legal/compliance experts to maintain adherence to these standards.
*   **Third-Party Integrations:**\
    Focus will be on Apple Calendar integration with a secondary consideration for Google Calendar. Any additional calendar service is not considered.
*   **UI/UX Ambition:**\
    The magical, fun, and enchanting UI design is expected to be balanced with usability. It is assumed that designers will conduct iterative user testing to refine animations and interactions.

## 8. Known Issues & Potential Pitfalls

*   **Real-Time Sync Challenges:**\
    Real-time collaboration and cloud backup require efficient data synchronization. Potential pitfalls include API rate limits or network latency issues. Mitigation includes thorough testing of synchronization under various network conditions and fallback mechanisms for offline mode.
*   **AI Integration Performance:**\
    Relying on external AI models may introduce latency or dependability issues. Consider offering users the option to disable AI suggestions if delays occur and ensure comprehensive error handling for AI responses.
*   **Privacy & Compliance Risks:**\
    Managing sensitive user data adds a layer of risk regarding privacy and compliance. Mitigation strategies involve regular audits, clear privacy policies, and adherence to data protection regulations by design.
*   **User Onboarding Experience:**\
    With multiple features and a unique magical design, there may be a learning curve for new users. To mitigate this, focus on a guided onboarding process that clearly explains the primary functionalities without overwhelming the user.
*   **Design Complexity & Animations:**\
    Integrating fun animations and a glassmorphic, gradient-based UI could impact performance on older devices. It’s important to perform performance testing and optimize animations to ensure a smooth user experience across all supported devices.

This PRD provides a clear, detailed reference for developing GenieList, ensuring that every aspect of the project is well-understood. It sets the stage for subsequent technical documents covering detailed tech stacks, frontend guidelines, backend structures, and implementation plans.
