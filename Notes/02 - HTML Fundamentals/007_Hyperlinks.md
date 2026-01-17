# Hyperlinks (Anchors)

## Key Concepts & Overview
*   **Summary:** This lesson covers how to create hyperlinks, the fundamental building blocks that connect webpages into a "World Wide Web." It explores linking to external websites, internal pages, and creating placeholder links.
*   **Main Goal:** To implement links in the "Code Magazine" project that navigate to external resources (MDN Web Docs) and internal pages (a new blog page).

## Detailed Breakdown

### 1. The Anchor Element (`<a>`)
*   **Element:** `<a>` (stands for **Anchor**).
*   **Syntax:** `<a>Link Text</a>`
*   **Function:** Creates a clickable link.
*   **Crucial Attribute:** The element *must* have an `href` attribute to function as a link. Without it, it is just plain text.

### 2. Types of Links

#### A. External Links (Pointing Outwards)
Links that navigate to a different website.
*   **Example:** Linking to MDN Web Docs.
*   **Syntax:**
    ```html
    <a href="https://developer.mozilla.org/en-US/">MDN Web Docs</a>
    ```
*   **Opening in a New Tab:**
    *   To keep the current page open and launch the link in a new tab, use the `target` attribute.
    *   **Value:** `_blank`
    *   **Syntax:** `target="_blank"`
    *   **Example:** `<a href="..." target="_blank">Link</a>`

#### B. Internal Links (Pointing Inwards)
Links that navigate to another page within the same website project.
*   **Example:** Linking from `index.html` to `blog.html`.
*   **Setup:**
    1.  Create a new file (e.g., `blog.html`).
    2.  Add basic HTML structure (DOCTYPE, html, head, body).
*   **Syntax:**
    ```html
    <a href="blog.html">Blog</a>
    ```
*   **Reciprocal Linking:** It is common practice to add a "Back" link on the destination page (e.g., `<a href="index.html">Back to Home</a>`).

#### C. Placeholder Links (Dead Links)
Links that look clickable but do not navigate to a new page.
*   **Use Case:** When the destination page hasn't been created yet, or for "Back to Top" functionality.
*   **Syntax:** Use the `#` (hash) symbol as the value for `href`.
*   **Behavior:** Clicking it jumps to the top of the current page.
*   **Example:**
    ```html
    <a href="#">Flexbox</a>
    ```

### 3. Practical Implementation
The lesson implements a navigation menu using these concepts:

```html
<!-- Internal Link -->
<a href="blog.html">Blog</a>

<!-- Placeholder Links -->
<a href="#">Challenges</a>
<a href="#">Flexbox</a>
<a href="#">CSS Grid</a>
```

And an external link within a paragraph:
```html
<p>
    You can learn more at 
    <a href="https://developer.mozilla.org/en-US/" target="_blank">
        MDN Web Docs
    </a>
</p>
```

## Summary & Key Takeaways
*   Use the `<a>` element for links.
*   **`href` attribute:** Mandatory. Defines the destination URL (external) or filename (internal).
*   **`target="_blank"`:** Opens the link in a new browser tab.
*   **`href="#"`:** Creates a placeholder link that stays on the current page.
*   **Navigation:** Internal links rely on relative file paths (e.g., just the filename if in the same folder).