# Your Very First Webpage!

### Key Concepts/Overview

This lesson provides a step-by-step guide to creating your first simple webpage. The primary goal is to write a few lines of HTML code, save the file, and then view the resulting webpage in a web browser. This process demonstrates the fundamental workflow of web development: writing code and seeing its visual output.

### Detailed Breakdown

#### 1. Setting Up the Project Environment

- **Project Folder:** In VS Code, all work is done within a "project folder." This is simply a regular folder on your computer that holds all the files for a specific project.
- **Steps to Set Up:**
    1.  Create a new folder on your computer (e.g., on the Desktop). For this lesson, it's named `zero one and test`.
    2.  Open VS Code and click **"Open Folder"**.
    3.  Navigate to and select the folder you just created. This folder is now your active project folder in VS Code.

#### 2. Creating the HTML File

- A webpage is fundamentally an **HTML file**.
- **File Naming Convention:**
    - The main page of any website should be named `index.html`.
    - This is the standard name for the entry point of a website.
- **Steps to Create the File in VS Code:**
    1.  Hover over the project folder name in the left sidebar (the Explorer tab).
    2.  Click the **"New File"** icon.
    3.  Name the file `index.html`.

#### 3. Writing Basic HTML Code

- **VS Code Shortcut (Emmet):** To quickly generate a basic HTML structure:
    1.  In the empty `index.html` file, type a single exclamation mark (`!`).
    2.  Press the `Tab` key or click the suggestion that appears.
    3.  This will insert a standard HTML boilerplate, including `<head>` and `<body>` sections.

- **Editing the HTML Structure:**
    - **`<title>`:** This element is inside the `<head>` section. The text here appears in the browser tab.
        - **Example:** `<title>my first webpage</title>`
    - **`<body>`:** This section contains all the visible content of the webpage.
        - **Heading (`<h1>`):** Stands for "Heading 1" and is used for main titles.
            - **Example:** `<h1>Hello World</h1>`
            - *Note: "Hello World" is a long-standing tradition for a first program.*
        - **Paragraph (`<p>`):** Used for regular text content.
            - **Example:** `<p>My name is Jonas, and this is my very first webpage.</p>`

#### 4. Saving and Formatting

- **Saving the File:**
    - Press `Command + S` (Mac) or `Control + S` (Windows).
    - VS Code's **Auto Save** feature will also save the file automatically when you click away from the editor tab.
- **Automatic Code Formatting:**
    - The **Prettier** extension (installed in a previous lesson) automatically formats your code every time you save it.
    - This ensures your code is clean, organized, and consistent with the style shown in the course videos.

#### 5. Viewing the Webpage in a Browser

- **Steps to Open:**
    1.  Navigate to your project folder on your computer (e.g., on the Desktop).
    2.  Locate the `index.html` file.
    3.  **Double-click** the file to open it in your default browser.
    4.  Alternatively, right-click the file and select "Open with" to choose a specific browser like **Google Chrome**.

- **Recommended Browser:**
    - It is highly recommended to use **Google Chrome** for this course to ensure your results match what is shown in the videos.

- **Observing the Result:**
    - The text inside the `<h1>` tags appears as a large, bold heading.
    - The text inside the `<p>` tags appears as a standard paragraph.
    - The text from the `<title>` tag is displayed on the browser tab.

#### 6. Recommended Development Workflow

- A common and efficient setup is to arrange your screen with:
    - **VS Code** on the left side.
    - The **web browser** on the right side.
- This allows you to see your code and the resulting changes in the browser simultaneously.
- You can collapse the VS Code sidebar (by clicking the Explorer icon) to maximize space for your code.

### Summarization/Key Takeaways

The core process for creating and viewing a webpage involves these key steps:
1.  **Create a Project Folder** on your computer.
2.  **Open the Folder** in VS Code.
3.  **Create an `index.html` File** inside the project folder.
4.  **Add HTML Code** to the file to define the page's structure and content (e.g., `<h1>`, `<p>`).
5.  **Save the File**, allowing Prettier to format the code.
6.  **Open the `index.html` File in a Browser** (like Google Chrome) to see the visual translation of your code.