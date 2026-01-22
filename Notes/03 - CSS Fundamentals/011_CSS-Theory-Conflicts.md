# CSS Theory #1: Conflicts Between Selectors

## Overview
This lecture addresses a fundamental question in CSS: **What happens when multiple CSS rules apply to the exact same element?** These scenarios are called "conflicting selectors." Understanding the hierarchy of how CSS resolves these conflicts is crucial for troubleshooting and writing predictable code.

## Conflict Resolution Logic
When an element is targeted by multiple selectors (e.g., an ID, a class, and an element tag), **all** rules apply. However, if they contain conflicting declarations (e.g., one rule sets `font-size: 18px` and another sets `font-size: 20px`), CSS uses a specific priority system to decide which value "wins."

### The Priority Hierarchy
The following list is ordered from **highest** priority to **lowest**:

1.  **`!important` Keyword**
    *   **Description:** Overrides almost all other declarations.
    *   **Usage:** Generally considered a "hack" or last resort. Avoid using it unless absolutely necessary.
    *   **Example:** `color: green !important;`

2.  **Inline Styles**
    *   **Description:** Styles written directly in the HTML `style` attribute.
    *   **Example:** `<p style="color: red;">`
    *   **Priority:** Higher than IDs, classes, and elements.

3.  **ID Selectors (`#id`)**
    *   **Description:** The most powerful standard selector.
    *   **Priority:** An ID selector will override class and element selectors.
    *   **Tie-Breaker:** If multiple ID selectors target the same element, the **last one** written in the code applies.

4.  **Class (`.class`) and Pseudo-class (`:hover`) Selectors**
    *   **Description:** Classes and pseudo-classes share the same priority level.
    *   **Priority:** Higher than element selectors but lower than IDs.
    *   **Tie-Breaker:** If multiple classes apply conflicting styles, the **last one defined in the CSS file** applies (not the order in the HTML `class` attribute).

5.  **Element Selectors (`tag`)**
    *   **Description:** Selecting by tag name (e.g., `p`, `div`, `h1`).
    *   **Priority:** Lower than classes.
    *   **Tie-Breaker:** If multiple element rules conflict, the **last one** in the file applies.

6.  **Universal Selector (`*`)**
    *   **Description:** Selects everything.
    *   **Priority:** Lowest of all.

## Visualizing Specificity (VS Code Tip)
When you hover over a selector in VS Code, it displays a specificity score (e.g., `(1, 0, 0)`).
*   **First number:** Count of ID selectors.
*   **Second number:** Count of Class/Pseudo-class selectors.
*   **Third number:** Count of Element selectors.
*   *Note:* The "numbers" function like a version number; `(1, 0, 0)` is always greater than `(0, 5, 5)`.

## Practical Examples from Lecture

### Example 1: ID vs. Class vs. Element
*   **Scenario:** A footer paragraph has an ID `#copyright`, a class `.copyright`, and is an element `p`.
    *   Rule 1: `#copyright { color: red; }`
    *   Rule 2: `.copyright { color: blue; }`
    *   Rule 3: `footer p { color: green; }`
*   **Result:** Text is **Red**.
*   **Reason:** The ID selector (`#copyright`) has the highest priority.

### Example 2: Class vs. Class (Tie-Breaker)
*   **Scenario:** Same element, but the ID rule is removed.
    *   Rule 1: `.copyright { color: blue; }`
    *   Rule 2: `.text { color: yellow; }` (Assuming `.text` comes after `.copyright` in the CSS file).
*   **Result:** Text is **Yellow**.
*   **Reason:** Both are classes (same priority), so the **last rule defined in the CSS file** wins.

### Example 3: Pseudo-class vs. Element
*   **Scenario:** Styling links.
    *   Rule 1: `a { color: red; }`
    *   Rule 2: `a:link { color: blue; }`
*   **Result:** Text is **Blue**.
*   **Reason:** `:link` is a pseudo-class, which has higher priority than the simple element selector `a`.

## Key Takeaways
1.  **Simplify Selectors:** Avoid over-nesting or using unnecessary IDs/Classes. Simple selectors are easier to maintain.
2.  **Order Matters:** For selectors of equal weight (e.g., two classes), the one written last in the CSS file wins.
3.  **Avoid `!important`:** It disrupts the natural cascade and makes debugging difficult.
4.  **DevTools:** Use the inspector to see which styles are being applied and which are being crossed out (overridden).