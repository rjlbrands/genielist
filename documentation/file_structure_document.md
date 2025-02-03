# Introduction

In every development project, especially one as feature-rich and user-focused as GenieList, having a well-organized file structure is crucial. It not only keeps the project in order but also aids in smooth collaboration across the team. GenieList, an iOS app designed to help users keep track of their tasks, reminders, events, notes, and more, benefits from a file structure that maintains clarity and consistency, ensuring everyone—from developers to project managers—understands where everything is located and how it is organized.

# Overview of the Tech Stack

GenieList is built using SwiftUI for its modern and engaging iOS user interface. The backend is powered by Supabase, which handles user authentication, data storage, and real-time syncing to support features such as cloud backup and collaboration. Calendar integrations primarily target Apple Calendar, with additional support for Google Calendar. Optional AI functionalities leveraging GPT-4o or Claude 3.5 Sonnet are integrated for smart productivity suggestions. The development environment is centered around Xcode, with enhanced coding efficiency provided by Cursor. This tech stack directly shapes our file organization, ensuring separation between the user interface, backend configurations, and auxiliary tooling files.

# Root Directory Structure

The root directory of the GenieList project is organized to clearly separate all major components. At the highest level, folders are designated for source code, assets, configurations, tests, and documentation. The source code folder contains the main SwiftUI project files including views, models, view models, services, and utilities, ensuring that each aspect of the application is neatly compartmentalized. Asset management, including icons, images, and design resources like gradients and animation files, is centralized in a dedicated folder to ensure consistency across the app. In addition, configuration and environment-specific files are placed at the root level, accompanied by documentation that guides both current development and future enhancements.

# Configuration and Environment Files

At the heart of the GenieList project’s setup lie its configuration and environment files. These files include settings for connecting to Supabase for user authentication and cloud storage, as well as environment variable files to securely store API keys and sensitive configurations. Build configurations and dependency management files are also housed at this level, ensuring that the project remains portable and easy to set up in different development environments. This approach minimizes the risk of misconfiguration and facilitates a smooth onboarding process for new developers.

# Documentation Structure

To promote transparency and facilitate collaboration, all project documentation is organized in a dedicated documentation folder. This includes the Project Requirements Document (PRD), app flow documentation, tech stack guidelines, and frontend and backend structure documents. This centralization makes it easy for team members to share knowledge, refer to design principles, and understand the modularity of the project. By maintaining all documentation in one place, the project benefits from a consistent source of truth that is both easily accessible and updateable as the project evolves.

# Conclusion and Overall Summary

In summary, the file structure of the GenieList project is designed to support robust development and effective collaboration. The clear segmentation of source code, assets, configurations, and documentation ensures that every team member can quickly locate what they need and contribute efficiently. This structure not only adheres to best practices but also accommodates the dynamic nature of GenieList—a magical, engaging iOS app with intricate features ranging from cloud backup to AI-driven productivity tips.

Overall, GenieList’s unique blend of modern design, powerful backend services, and smart AI integrations is mirrored in its meticulously organized project structure. This careful arrangement makes the development process smoother, fosters better teamwork, and sets the stage for scalable growth as the app continues to evolve.
