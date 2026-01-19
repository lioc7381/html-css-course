# Introduction to CSS

## Key Concepts
*   **Definition:** CSS stands for **Cascading Style Sheets**.
*   **Core Function:** It is used to describe the **visual style** and **presentation** of content defined by HTML.
*   **Relationship:** HTML and CSS are core web technologies that work closely together. While HTML describes the *content* (using elements), CSS describes the *formatting* (using properties).

## Detailed Breakdown

### 1. HTML vs. CSS
To understand the role of CSS, it is helpful to contrast it with HTML:

*   **HTML:** Consists of **elements** used to describe content.
    *   *Example:* Identifying text as a heading or a paragraph.
*   **CSS:** Consists of **properties** used to format that content.
    *   *Capabilities:* Formatting fonts, text styling, general spacing, and page layout.

> **Visual Context:** If you view a webpage with only HTML, you see raw content. When CSS is added, that exact same HTML code is transformed with visual styles and a defined layout.

### 2. Learning Approach
*   **Volume of Properties:** There are countless different CSS properties available to developers.
*   **Study Strategy:** You do **not** need to memorize all properties by heart.
*   **Method:** Focus on using the most important properties repeatedly; usage will become intuitive over time.

### 3. CSS Terminology and Syntax
Understanding the specific terminology of CSS code is essential. A typical piece of CSS code consists of the following components:

#### The CSS Rule
The entire structure (Selector + Declaration Block) is called a **CSS Rule**. A CSS file is essentially a collection of many CSS rules written one after another.

#### Component Breakdown

1.  **Selector**
    *   **Function:** Selects the specific HTML element(s) you want to style.
    *   *Example:* Selecting all `H1` elements on a page.

2.  **Declaration Block**
    *   **Structure:** Defined by curly braces `{ }` appearing after the selector.
    *   **Content:** Contains all the different declarations (styles) applied to the selector.

3.  **Declaration (Style)**
    *   **Definition:** A single styling instruction inside the block.
    *   **Composition:** Made up of a **Property** and a **Value**.
        *   **Property:** The specific aspect being changed (e.g., `font-size`).
        *   **Value:** The specific setting applied to the property (e.g., `20px`).

### Visualizing Syntax

| Term | Example Context | Definition |
| :--- | :--- | :--- |
| **Selector** | `h1` | The element being targeted. |
| **Property** | `font-size` | What style is being changed. |
| **Value** | `20px` | The setting for the style. |
| **Declaration** | `font-size: 20px` | The Property + The Value. |
| **Declaration Block**| `{ ... }` | Container for all declarations. |
| **CSS Rule** | `h1 { ... }` | The Selector + The Declaration Block. |

## Summary
*   CSS is the language of visual presentation on the web.
*   It functions through **properties** applied to HTML **elements**.
*   Code is structured into **Rules**, which consist of a **Selector** (who to style) and a **Declaration Block** (how to style).
*   A **Declaration** pairs a specific **Property** with a **Value**.