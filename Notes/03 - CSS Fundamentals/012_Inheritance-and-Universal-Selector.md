# CSS Theory #2: Inheritance and the Universal Selector

## Overview
This lecture explores **Inheritance**, a core mechanism where specific CSS properties declared on a parent element are passed down to its children. It also introduces the **Universal Selector**, a tool for applying styles to every element on the page, and distinguishes between the two concepts.

## 1. Inheritance
Inheritance allows child elements to automatically adopt certain styles from their parents without needing explicit declarations.

*   **Common Use Case:** Setting global text styles on the `body` element. Since `body` is the ancestor of all visible content, these styles trickle down.
*   **Which properties inherit?**
    *   **Text-related properties:** `color`, `font-family`, `font-size`, `font-weight`, `line-height`, etc.
    *   **Box-model properties (do NOT inherit):** `margin`, `padding`, `border`, `height`, `width`.

### Inheritance vs. Specificity
*   **Priority:** Inherited styles have extremely **low priority**.
*   **Overriding:** Any rule applied directly to an element (via ID, class, or tag selector) will override an inherited style.
    *   *Example:* If `body` has `color: red` but `p` has `color: blue`, paragraphs will be blue because the direct rule on `p` wins.

### Practical Example: Global Styles
Instead of setting `font-family` on every individual tag (`h1`, `p`, `a`, etc.), set it once on the `body`.
```css
body {
    color: #444;
    font-family: sans-serif;
}
```
*   **Result:** All elements inside the body will use these values unless explicitly overridden.

### Practical Example: Component Styling
Inheritance works on smaller scales too.
*   **Scenario:** You want all text inside a `<nav>` (links, spans, strong tags) to be 18px.
*   **Solution:**
    ```css
    nav {
        font-size: 18px;
    }
    ```
*   **Result:** Child elements like `<strong>` inside the nav will inherit `18px`. However, if a child (like `<p>`) has a specific global rule (e.g., `p { font-size: 22px; }`), that specific rule will override the inherited value.

---

## 2. The Universal Selector (`*`)
The universal selector targets **every single element** in the HTML document individually.

*   **Syntax:** `* { ... }`
*   **Function:** Applies declared styles to all elements directly.
*   **Key Difference from Inheritance:**
    *   **Inheritance:** Passes values down the tree (parent -> child). Only applies to specific text properties.
    *   **Universal Selector:** Selects everything directly. Can apply **any** property (borders, margins, etc.) to **every** element.

### Example: Universal Selector vs. Body
*   **Trying to add a border to everything:**
    *   `body { border-top: 10px solid blue; }` -> Only adds one border to the very top of the page (on the body itself). `border` does not inherit.
    *   `* { border-top: 10px solid blue; }` -> Adds a blue border to *every single element* (paragraphs, links, headings, etc.).

### Priority
The Universal Selector has the **lowest priority** of all selectors (0,0,0), but it still applies styles directly to elements, unlike inheritance which is just a fallback.

---

## Summary
| Feature | Inheritance | Universal Selector (`*`) |
| :--- | :--- | :--- |
| **Mechanism** | Passes values from parent to child. | Selects every element individually. |
| **Properties** | Text-related (color, font, etc.). | Any property. |
| **Use Case** | Setting default text styles. | Global resets (margins/padding). |
| **Priority** | Very Low (overridden by anything). | Lowest Selector Priority (0,0,0). |
