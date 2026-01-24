# CSS Pseudo-elements

## Key Concepts
*   **Definition:** Pseudo-elements act like elements that do not exist in the HTML source code but can be selected and styled via CSS.
*   **Syntax:** Denoted by a double colon `::` (e.g., `::first-letter`).
    *   *Differentiation:* Pseudo-classes use a single colon (e.g., `:hover`), while pseudo-elements use two.
*   **Main Goal:** To style specific parts of an element (like the first letter) or insert cosmetic content (like icons or badges) without cluttering the HTML structure.

---

## 1. Text Formatting Pseudo-elements

### `::first-letter`
Selects and styles the very first character of a block-level element.
*   **Example:** Making the first letter of a heading non-italic and adding spacing.

```css
h1::first-letter {
    font-style: normal;
    margin-right: 5px;
    font-size: 80px; /* Can dramatically change size */
}
```

### `::first-line`
Selects and styles the first line of a block-level element.
*   **Behavior:** The styling applies to whatever text renders on the first line. If the browser window resizes and the text wraps differently, the styling adjusts automatically to the new first line.

```css
p::first-line {
    color: red;
}
```

---

## 2. Advanced Selectors: The Adjacent Sibling (`+`)
While not a pseudo-element, this selector is often used in conjunction with them for precise targeting.
*   **Definition:** Selects an element that is the **immediate next sibling** of another element.
*   **Syntax:** `ElementA + ElementB` (Selects B only if it immediately follows A).

```css
/* Selects only paragraphs that come immediately after an h3 */
h3 + p::first-line {
    color: red;
}
```

---

## 3. The `::after` and `::before` Pseudo-elements
These are the most powerful and commonly used pseudo-elements. They insert a "virtual" element into the DOM that can be styled just like a real HTML tag.

### Mechanics
*   **`::before`**: Creates a pseudo-element as the **first child** of the selected element.
*   **`::after`**: Creates a pseudo-element as the **last child** of the selected element.

### The `content` Property
*   **Mandatory:** You *must* define the `content` property for these pseudo-elements to appear.
*   **Values:** It can be text (e.g., "Top"), special characters, or often just an empty string `""` for purely visual shapes.

### Practical Example: "Top Article" Badge
The instructor demonstrates creating a yellow "Top" label attached to an `<h2>` heading.

#### Step 1: Create and Content
```css
h2::after {
    content: "TOP"; /* Text to display */
    background-color: #ffe70e;
    color: #444;
    font-size: 16px;
    font-weight: bold;
}
```

#### Step 2: Display and Box Model
By default, pseudo-elements are **inline**. To apply padding and dimensions effectively, change the display mode.
```css
h2::after {
    /* ... previous styles ... */
    display: inline-block; /* Allows padding/margins to work */
    padding: 5px 10px;
}
```

#### Step 3: Absolute Positioning
To place the badge precisely (e.g., overlapping the corner of the header), use absolute positioning.

1.  **Set Context:** Make the parent (`h2`) the positioning context.
    ```css
    h2 {
        position: relative;
    }
    ```
2.  **Position the Pseudo-element:**
    ```css
    h2::after {
        position: absolute;
        top: -10px;  /* Moves UP (negative value) */
        right: -25px; /* Moves RIGHT (negative value pushes it outside) */
    }
    ```

### Negative Margins/Positioning
*   **Positive values:** Move elements *inwards* from the reference edge (e.g., `right: 25px` moves it 25px to the left).
*   **Negative values:** Move elements *outwards* or in the opposite direction (e.g., `right: -25px` moves it 25px to the right, potentially outside the parent).

---

## Summary Table

| Pseudo-element | Description | Common Use Case |
| :--- | :--- | :--- |
| `::first-letter` | First character of the element | Drop caps (magazine style) |
| `::first-line` | First line of text | Emphasizing the opening sentence |
| `::before` | Inserts content *before* the element's content | Icons, decorative quotes |
| `::after` | Inserts content *after* the element's content | Badges, clear-fix hacks, decorative shapes |

> **Crucial Tip:** Always remember to set `content: ""` for `::before` and `::after`, otherwise, they will not render on the page.