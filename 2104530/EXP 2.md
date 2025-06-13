# EXPERIMENT NO. 2

## Title: Setting Up Android Studio and Understanding Its Basic Components

## 1. Installing Android Studio

### System Requirements

- **Windows**:
  - 64-bit Windows 8.1, 10, or later
  - Minimum 8 GB RAM (16 GB recommended)
  - 4 GB of available disk space minimum
- **macOS**:
  - macOS High Sierra (10.13) or newer
- **Linux**:
  - GNOME/KDE desktop environment
  - GNU C Library (glibc) 2.31 or later

### Steps to Download and Install

- Visit the [Android Studio download page](https://developer.android.com/studio).
- Click **Download Android Studio** and agree to the terms and conditions.

#### Installation Instructions

**On Windows:**
- Run the downloaded `.exe` file.
- Follow the Setup Wizard to install Android Studio, Android SDK, and emulator.

**On macOS:**
- Open the `.dmg` file.
- Drag and drop Android Studio into the **Applications** folder.
- Launch Android Studio and follow the configuration wizard.

**On Linux:**
- Extract the `.tar.gz` archive.
- Open a terminal, navigate to the extracted directory.
- Run the setup using `./studio.sh`.


## 2. Setting Up Android Studio

- **First Launch**: Open Android Studio and complete the initial setup wizard.
- **Install SDK Components**: The wizard installs the latest SDK version, platform tools, and build tools.
- **Emulator Setup**:
  - Use the **AVD Manager** to create virtual devices.
  - Configure device type, system image (API level), and resolution.


## 3. Basic Components of Android Studio

### 1. Welcome Screen
- **Quick Start Options**:
  - Start a new project
  - Open an existing project
  - Clone from GitHub or other version control
- **Recent Projects**: Access previous projects quickly.

### 2. Project Structure
- **Project View**:
  - Access Java/Kotlin files, resources, Gradle scripts, and manifests.
- **Android View**:
  - Filters project structure to only show relevant Android directories.

### 3. Editor Window
- Primary space to edit code.
- Tab-based interface to switch between files.
- **Split View** support for multitasking.

### 4. Tool Windows
- **Project**: Navigate files and directories.
- **Logcat**: View real-time logs and debugging output.
- **Build**: Monitor build process and errors.
- **Terminal**: Run shell commands directly.
- **Event Log**: Shows background operations like Gradle syncs.

### 5. Toolbar
- **Run/Debug Buttons**: Launch or debug apps on emulator/device.
- **AVD Manager**: Create or manage virtual devices.
- **SDK Manager**: Install or update Android SDK components.

### 6. Code Editor
- **Syntax Highlighting**: Enhances code readability.
- **Code Completion**: Suggests classes, methods, variables.
- **Linting**: Highlights potential issues in real-time.
- **Refactoring Tools**: Rename, extract, or move code safely.

### 7. Layout Editor
- **Design View**: Drag-and-drop UI builder.
- **Code/Text View**: XML code editing mode.
- **Palette**: Collection of UI components (TextView, Button, etc.).
- **Component Tree**: Displays layout hierarchy.


## 4. Creating a Simple Android Project

### Steps to Start a New Project
1. Open Android Studio and select **"Start a new Android Studio project"**.
2. Choose a template (e.g., **Empty Activity**).
3. Fill in project details:
   - Name
   - Package name
   - Save location
   - Language: Java or Kotlin
   - Minimum SDK version

### Exploring the Project Structure
- **`app/java`**: Contains your Java/Kotlin source files.
- **`app/res`**: Contains XML layouts, images, and other resources.
- **`AndroidManifest.xml`**: Declares components and permissions.

### Running the App
- Click the green **Run** button.
- Select a connected device or virtual emulator.
- App will compile, install, and launch.

## 5. Understanding Android App Components
### 1. Activities
- Represent a single screen with a user interface.
- Extend `Activity` or `AppCompatActivity`.

### 2. Layouts
- XML files that define the UI structure.
- Located in `res/layout`.

### 3. Resources
- Include strings (`strings.xml`), colors (`colors.xml`), styles (`styles.xml`), and drawable assets.
- Allow easier localization and design consistency.

### 4. Manifests
- The `AndroidManifest.xml` file contains:
  - App name and icon
  - Activities, services, broadcast receivers
  - Permissions (e.g., Internet, camera)

### 5. Gradle Scripts
- Used for build configuration and dependencies.
- `build.gradle (Project)`: Configuration for all modules.
- `build.gradle (Module: app)`: App-specific dependencies and settings.

## Additional Features that u can add

- **Plugins**: Enhance functionality (e.g., Git, Firebase, Material UI plugins).
- **Version Control Integration**: Supports Git, GitHub, Bitbucket natively.
- **Real-Time Preview**: Layout preview updates as you write XML.
- **Live Templates**: Use shortcuts like `sout`, `Toast`, etc., for rapid coding.
