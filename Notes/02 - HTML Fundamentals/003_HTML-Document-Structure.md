# Common HTML Document Structure

## Key Concepts & Overview
*   **Summary:** This lesson outlines the mandatory structure required for every HTML document, often referred to as "boilerplate" code.
*   **Main Goal:** To manually write the fundamental HTML skeleton—without the aid of auto-completion—to ensure deep memorization of the core elements (`html`, `head`, `body`).
*   **Project Context:** The structure is applied to a new project called **"The Code Magazine,"** a simple blog post titled "The Basic Language of the Web."

## Detailed Breakdown

### 1. Project Setup
Before writing code, the workspace is prepared:
*   **File Creation:** The main file is named `index.html`. This is the standard name for the main page of any website.
*   **VS Code Configuration:** The instructor recommends temporarily disabling **"Auto Close Tags"** in settings. This forces the student to write both opening and closing tags manually, aiding in muscle memory.

### 2. The Four Pillars of HTML Structure
Every HTML document relies on a specific hierarchy of elements.

#### A. The DOCTYPE Declaration
*   **Syntax:** `<!DOCTYPE html>`
*   **Purpose:** The very first line of code. It informs the browser that the document uses **HTML** (specifically the HTML5 specification) and directs it to render the page accordingly.

#### B. The HTML Element
*   **Syntax:** `<html> ... </html>`
*   **Purpose:** The root element. It acts as the parent element for everything else in the document.

#### C. The Head Element
*   **Syntax:** `<head> ... </head>`
*   **Placement:** Must be nested *inside* the `<html>` element.
*   **Purpose:** Contains information **not visible** in the main browser window (metadata).
*   **Key Child Element:**
    *   `<title>`: Defines the text shown in the browser tab (e.g., "The Basic Language of the Web").

#### D. The Body Element
*   **Syntax:** `<body> ... </body>`
*   **Placement:** Must be nested *inside* the `<html>` element (after the `<head>`).
*   **Purpose:** Contains all elements **visible** on the page (what the user actually sees).
*   **Key Child Element (Example):**
    *   `<h1>`: A top-level heading used to display the blog post title.

### 3. Code Indentation and Readability
*   **Indentation:** When an element is placed inside another (nesting), it should be indented (usually by a tab).
    *   *Example:* `<title>` is indented because it is inside `<head>`.
*   **Purpose:** The browser ignores indentation, but it is critical for **human readability** and understanding the parent-child relationships in the code.
*   **Formatting Tools:** Saving the file in VS Code (with Prettier installed) automatically corrects indentation.

### 4. Visualizing the Hierarchy
The structure represents a tree of elements:
*   `<html>` (Parent)
    *   `<head>` (Child of html)
        *   `<title>` (Child of head)
    *   `<body>` (Child of html)
        *   `<h1>` (Child of body)

## Summary & Key Takeaways
To be valid, every HTML document must follow this exact structure:

1.  **DOCTYPE:** `<!DOCTYPE html>` declares the file type.
2.  **HTML Root:** The `<html>` element wraps the whole document.
3.  **Head:** The `<head>` section holds the `<title>` and invisible settings.
4.  **Body:** The `<body>` section holds the visible content.

**Reference Code Structure:**
```html
<!DOCTYPE html>
<html>
    <head>
        <title>The Basic Language of the Web HTML</title>
    </head>
    <body>
        <h1>The Basic Language of the Web: HTML</h1>
    </body>
</html>
```