# Styling Hyperlinks

## Overview
This section focuses on styling hyperlinks (`<a>` tags) using dedicated **pseudo-classes**. Rather than styling the anchor tag directly, CSS provides four specific states that allow for more interactive and robust link designs.

## The Four Link States (LVHA)
To ensure links function correctly, these pseudo-classes should always be defined in the following order: **L**ink, **V**isited, **H**over, **A**ctive (**LVHA**).

### 1. `:link`
*   **Purpose:** Targets anchor elements that have an `href` attribute (unvisited links).
*   **Why use it?** Unlike selecting just `a`, `a:link` ensures you don't accidentally style anchor tags that are used for other purposes (like internal bookmarks) which might lack an `href`.
*   **Common Styling:**
    *   Set a primary color.
    *   Remove default underlines using `text-decoration: none;`.

### 2. `:visited`
*   **Purpose:** Targets links that the user has already clicked.
*   **Common Practice:** While browsers often default these to purple, modern web design typically styles `:visited` links identically to `:link` to maintain a cleaner look.
*   **Example:**
    ```css
    a:visited {
        color: #1098ad; /* Same as the normal link color */
    }
    ```

### 3. `:hover`
*   **Purpose:** Applies styles when the mouse cursor is placed over the link.
*   **Usage:** Crucial for user feedback, indicating the element is clickable.
*   **Styling Examples:**
    *   Change color (e.g., to `orangered`).
    *   Add underlines or borders.
    *   Change font weight (e.g., `bold`).
*   **Text Decoration Tricks:**
    *   `text-decoration` is a shorthand for line, style, and color.
    *   *Example:* `text-decoration: underline wavy orangered;` creates a wavy underlined effect.

### 4. `:active`
*   **Purpose:** Targets the link during the exact moment it is being clicked (mouse button down).
*   **Styling Examples:**
    *   Change background color (e.g., `black`).
    *   Change font style (e.g., `italic`).

## Summary of Properties
*   **`text-decoration`:** Used to add or remove underlines. `none` removes it; `underline` adds it. It supports shorthand for style (solid, dotted, wavy) and color.
*   **`font-weight`:** Used to make text bold on hover.
*   **`background-color`:** Can be used to highlight the link while it is being clicked (`:active`).

## Practical Code Example
```css
/* 1. Link State */
a:link {
    color: #1098ad;
    text-decoration: none;
}

/* 2. Visited State */
a:visited {
    color: #1098ad;
}

/* 3. Hover State */
a:hover {
    color: orangered;
    font-weight: bold;
    text-decoration: underline dotted orangered;
}

/* 4. Active State */
a:active {
    background-color: black;
    font-style: italic;
}
```