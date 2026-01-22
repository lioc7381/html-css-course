# Using Chrome DevTools

## Overview
**Developer Tools (DevTools)** are a set of built-in utilities in modern browsers that simplify the development process. They allow developers to inspect HTML structure, view and manipulate CSS styles in real-time, and debug code efficiently. This lesson focuses on the **Google Chrome** DevTools.

## How to Open DevTools
There are three methods to access the tools:
1.  **Right-click Method:** Right-click anywhere on the page and select "Inspect" or "Inspect Element".
2.  **Menu Method:** Go to the Chrome menu → View → Developer → Developer Tools.
3.  **Keyboard Shortcut:**
    *   **Mac:** `Option + Command + I`
    *   **Windows:** `Option + Control + I`

## Key Panels

### 1. Elements Tab
This tab displays the live HTML structure of the page.
*   **Inspecting Elements:** Clicking on an element in the code view highlights the corresponding area on the actual webpage (e.g., highlighting a header shows its blue bounding box).
*   **Navigation:** You can expand and collapse elements (like `nav` or `div`) to see their children.
*   **Context:** Right-clicking an element on the actual webpage and choosing "Inspect" automatically jumps to that specific line of code in the Elements tab.

### 2. Styles Tab
Located (usually) to the right or bottom of the Elements tab, this pane controls CSS.
*   **Viewing Styles:** When an HTML element is selected, this pane lists all CSS rules currently applying to it, including those from your external stylesheets.
*   **User Agent Styles:** You may see default styles (like `font-weight: bold` for `h1`) labeled under "user agent stylesheet." These are the browser's default settings.
*   **Live Editing:**
    *   You can toggle individual properties on/off using the checkboxes.
    *   You can add temporary properties (e.g., adding `font-size: 30px` to a link) to test changes.
    *   *Note:* These changes are **temporary**. Reloading the page reverts everything to the original code.

### 3. State Simulation (Pseudo-classes)
DevTools allows you to "fake" element states (like hover) without actually interacting with the page.
*   **How to access:** Click the `:hov` button in the Styles pane.
*   **Function:** Check boxes for states like `:hover`, `:active`, or `:visited`.
*   **Result:** The browser renders the element as if it were in that state (e.g., showing the hover color and underline permanent), allowing for easier design tweaking.

## Summary
*   **Inspect:** Use the magnifying glass or right-click "Inspect" to find code fast.
*   **Experiment:** Edit CSS values live in the browser to test designs before writing permanent code.
*   **Debug:** Use the state toggle to fix issues with interaction styles like hovers and clicks.