# Setting Up the Code Editor: Visual Studio Code

### Key Concepts/Overview

This guide covers the installation and initial setup of **Visual Studio Code (VS Code)**, the recommended code editor for this course. A code editor is a specialized software tool designed to make writing programming code, like HTML and CSS, easier and more efficient.

**Main Goal:** To install VS Code and configure it with specific extensions and settings to create a consistent and productive development environment that matches the instructor's setup.

---

### Detailed Breakdown

#### 1. What is Visual Studio Code (VS Code)?

-   **Definition:** A free code editor from Microsoft, widely regarded as one of the best for web development.
-   **Popularity:** Used by a vast majority of developers.
-   **Availability:** Free for macOS, Windows, and Linux.

#### 2. Installation Process

1.  **Download:** Navigate to `code.visualstudio.com` or search for "VS Code" on Google.
2.  **Install:** Download the installer for your operating system (macOS, Windows, or Linux).
3.  **Run:** Install the program just like any other application on your computer.

#### 3. Configuration and Setup

After installing and opening VS Code, the following setup is recommended to align your editor with the course.

##### **A. Extensions**

Extensions are small pieces of functionality that can be downloaded to add features and customize the editor.

1.  **Prettier - Code Formatter**
    -   **Purpose:** Automatically formats your code to ensure it is clean, consistent, and readable.
    -   **Benefit:** Helps your code look exactly like the instructor's, making it easier to spot and fix errors.
    -   **Action:** Search for `Prettier` in the extensions marketplace, install it, and enable it. You may need to reload VS Code.

2.  **One Monokai - Color Theme**
    -   **Purpose:** A custom color theme that changes the colors of the editor and the code syntax to improve readability.
    -   **Benefit:** Using the same theme as the instructor makes it easier to follow along with the videos.
    -   **Action:** Search for `One Monokai` in the extensions marketplace, install it, and set it as your active color theme.

##### **B. Core Settings**

Access settings by clicking the **gear icon** (⚙️) in the bottom-left corner and selecting "Settings." Use the search bar to find and modify the following:

| Setting Name | Recommended Value | Purpose |
| :--- | :--- | :--- |
| **Default Formatter** | `Prettier - Code formatter` | Tells VS Code to use the Prettier extension for all code formatting. The specific ID is `esbenp.prettier-vscode`. |
| **Format On Save** | `Checked` (Enabled) | Automatically formats your code every time you save the file. |
| **Auto Save** | `onFocusChange` | Automatically saves your file whenever you switch to another tab or window, preventing data loss. |
| **Tab Size** | `2` | Sets the indentation of your code to two spaces, ensuring your code structure matches the instructor's. |

##### **C. File Icon Theme**

-   **Purpose:** Changes the appearance of icons next to filenames in the file explorer.
-   **Recommendation:** Set the **File Icon Theme** to `Seti` for visual consistency with the course.
-   **Action:** Access this option via the gear icon (⚙️) > "File Icon Theme".

---

### Summarization/Key Takeaways

To successfully set up your code editor for this course, follow these essential steps:

1.  **Install VS Code:** Download and install the editor from `code.visualstudio.com`.
2.  **Install Extensions:**
    -   `Prettier`: For automatic code formatting.
    -   `One Monokai`: For a consistent and readable color theme.
3.  **Configure Settings:**
    -   Set **Default Formatter** to `Prettier`.
    -   Enable **Format On Save**.
    -   Set **Auto Save** to `onFocusChange`.
    -   Set **Tab Size** to `2`.
4.  **Set Icon Theme:** Choose the `Seti` file icon theme.

With this setup complete, your editor is now configured and ready for you to start coding.