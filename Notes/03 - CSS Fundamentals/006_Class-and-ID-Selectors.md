# Class and ID Selectors

## Overview
This section introduces the practice of naming HTML elements to target them specifically in CSS. This avoids writing overly complex or brittle selectors (like `article header p`) that rely heavily on the HTML structure. The primary tools for this are **IDs** and **Classes**.

## 1. ID Selectors
An **ID** is a unique identifier assigned to a single HTML element.

*   **HTML Attribute:** `id="name"`
*   **CSS Selector:** `#name` (The Hash symbol)
*   **Key Rule:** An ID name must be unique within a page. You cannot assign the same ID (e.g., `id="copyright"`) to multiple elements.

### Example
**HTML:**
```html
<p id="author">By Jonas Schmedtmann</p>
```
**CSS:**
```css
#author {
    font-style: italic;
    font-size: 18px;
}
```

---

## 2. Class Selectors
A **Class** is an identifier that can be reused across multiple HTML elements. This is essential when you want to apply the same style to several different items (e.g., author names in a list of posts).

*   **HTML Attribute:** `class="name"`
*   **CSS Selector:** `.name` (The Dot symbol)
*   **Naming Convention:** Use hyphens to separate words (e.g., `related-author` rather than `related_author` or `relatedAuthor`).

### Example
**HTML:**
```html
<p class="related-author">Posted by Jim</p>
<p class="related-author">Posted by Sarah</p>
```
**CSS:**
```css
.related-author {
    font-size: 18px;
    font-weight: bold;
}
```

---

## 3. ID vs. Class: Best Practices
While both IDs and Classes can be used to select elements, **Classes are the industry standard.**

| Feature | ID (`#`) | Class (`.`) |
| :--- | :--- | :--- |
| **Uniqueness** | Must be unique per page. | Can be used multiple times. |
| **Selector Syntax** | `#id-name` | `.class-name` |
| **Primary Use** | Specific, one-off elements (historically). | Grouping elements, general styling. |
| **Recommendation** | **Avoid.** | **Use by default.** |

### Why Prefer Classes?
*   **Future-Proofing:** Even if an element seems unique now (like a "Related Posts" list), you might want to add a second one later (e.g., in the sidebar or footer). If you used an ID, you would have to refactor your HTML and CSS to switch to a Class. Using a Class from the start avoids this work.
*   **Scalability:** Classes prevent errors and bugs in larger projects where elements often need to be reused.

---

## 4. Additional CSS Properties Introduced
*   **`font-weight`:** Controls the thickness of the text.
    *   *Example:* `font-weight: bold;`
*   **`list-style`:** Controls the appearance of list markers (bullets/numbers).
    *   *Example:* `list-style: none;` removes bullet points from a list.

---

## 5. Commenting in CSS
*   **Syntax:** `/* comment goes here */`
*   **Usage:** Used to leave notes or temporarily disable code without deleting it.
*   **VS Code Shortcut:** `Ctrl + /` (Windows) or `Cmd + /` (Mac).

---

## 6. Conflict Resolution (Preview)
The lesson briefly noted that a single HTML element might be targeted by multiple selectors (e.g., a generic `p` selector, a class selector `.related-author`, and an ID selector).
*   **Observation:** All rules apply, but if there are conflicting properties (e.g., one says font size is 20px, another says 18px), the browser uses specific logic to decide which one wins.
*   **Note:** This logic involves **Specificity** and the **Cascade**, which will be covered in a future detailed lecture.