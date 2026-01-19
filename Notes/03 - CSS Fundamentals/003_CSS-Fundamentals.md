# CSS Fundamentals

## Overview
**CSS (Cascading Style Sheets)** is known as the "second language of the web." While HTML is used to describe the **content** and structure of a page, CSS is used to describe the **visual style**, presentation, and layout of that content.

The goal of learning CSS is to combine practical application (building projects) with theoretical concepts to understand the mechanics of the language, ensuring developers know exactly how their code functions.

---

## 1. HTML vs. CSS
To understand CSS, it is essential to distinguish it from HTML:

*   **HTML:** Consists of **elements**. It describes *what* the content is (e.g., a heading, a paragraph).
*   **CSS:** Consists of **properties**. It describes *how* the content looks (e.g., font size, color, spacing, layout).

> **Concept:** HTML and CSS work closely together. HTML provides the raw structure, and CSS applies the visual formatting.

---

## 2. CSS Syntax and Terminology
Developers do not need to memorize every CSS property. Instead, learning the core syntax and using common properties repeatedly builds intuition.

### The CSS Rule
A typical piece of CSS code is called a **Rule**. A rule is composed of a **Selector** and a **Declaration Block**.

#### Breakdown of a Rule:
1.  **Selector:** Indicates which HTML element to style (e.g., `h1`).
2.  **Declaration Block:** Starts with `{` and ends with `}`. It contains the specific styles.
3.  **Declaration:** A single style instruction found inside the block. It consists of:
    *   **Property:** The aspect being changed (e.g., `color`).
    *   **Value:** The specific setting for that property (e.g., `blue`).

**Visual Example:**
```css
/* Selector */
h1 {
    /* Declaration (Property: Value) */
    color: blue;
    font-size: 20px;
}
```

---

## 3. Methods of Writing CSS
There are three distinct ways to apply CSS to HTML. Understanding the differences and best practices for each is crucial.

### A. Inline CSS
Inline CSS involves writing style code directly inside an HTML element using the `style` attribute.

*   **Syntax:** `<h1 style="color: blue;">Text</h1>`
*   **Verdict:** **Avoid.** It entangles HTML and CSS, making the code hard to maintain. It should generally not be used in professional development.

### B. Internal CSS
Internal CSS is written within the HTML file, specifically inside the `<head>` section using the `<style>` element.

*   **Syntax:**
    ```html
    <head>
        <style>
            h1 { color: blue; }
        </style>
    </head>
    ```
*   **Pros:** Decouples styles from specific HTML elements better than Inline CSS.
*   **Cons:** If the CSS code becomes large (e.g., 500 lines), it bloats the HTML file and makes navigation difficult.
*   **Verdict:** Acceptable for small, quick projects or testing, but not ideal for larger applications.

### C. External CSS (Best Practice)
External CSS involves moving all style rules into a separate file (commonly named `style.css`). This file is then linked to the HTML document.

*   **Syntax:**
    1.  Create a file (e.g., `style.css`).
    2.  Write CSS rules directly in that file (no `<style>` tags needed).
    3.  Link it in the HTML `<head>`.
*   **The Link Element:**
    To connect the file, use the `<link>` element.
    *   `href`: Specifies the path to the CSS file.
    *   `rel`: Specifies the relationship (`stylesheet`).
    *   *Note:* The `<link>` element is strictly for connecting resources, not for creating hyperlinks (which use `<a>`).

    ```html
    <head>
        <link href="style.css" rel="stylesheet" />
    </head>
    ```
*   **Pros:** Achieves true **Separation of Concerns**. HTML handles content, and the external file handles style.
*   **Verdict:** **Best Practice.** This is the standard method for web development and will be used throughout the course.

---

## Summary
*   **CSS** handles presentation; **HTML** handles structure.
*   A **CSS Rule** consists of a **Selector** and a **Declaration Block** (Property + Value).
*   **External CSS** is the preferred method for applying styles, connected via the `<link>` tag in the HTML head.