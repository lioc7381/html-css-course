# Developer Skill #1: Googling and Reading Documentation

## Key Concepts
*   **The Myth of Memorization:** You do not need to memorize every single CSS property. It is normal and expected for developers of all levels to look things up.
*   **Problem Solving:** The ability to find solutions through search engines and documentation is a critical skill for a developer.
*   **The Goal:** Learn efficient techniques to find CSS solutions and understand how to read technical documentation to implement features correctly.

---

## 1. Effective Googling Strategies

When you encounter a styling issue or forget how to implement a specific visual effect, follow this search pattern:

### Search Query Structure
1.  **Language:** Always start with `CSS`.
2.  **Goal/Problem:** Briefly describe what you want to achieve or the property you are unsure about.
3.  **Context:** Mention the specific element involved (e.g., "button", "anchor element").

*   **Example Query:** `CSS property to add a mouse cursor to button`

### Analyzing Search Results
*   **Stack Overflow:** Look for `stackoverflow.com` results. This is a Q&A community where solutions are often peer-reviewed.
    *   *Tip:* Check the "Accepted Answer" (green checkmark) or the answer with the most upvotes.
    *   *Tip:* Read multiple questions/answers if the first one doesn't exactly match your scenario.
*   **Avoid:** `W3Schools` is often less reliable for deep technical understanding compared to other resources.
*   **Recommended:** `CSS-Tricks` and `MDN Web Docs` are excellent, high-quality resources.

### Scenario A: Adding a Cursor Pointer
*   **Problem:** You want a button to show a hand icon when hovered, but forgot the property.
*   **Search:** `CSS property to add a mouse cursor to button`
*   **Solution found:** `cursor: pointer;`

### Scenario B: Centering Anchor Links
*   **Problem:** `text-align: center` on anchor (`<a>`) tags isn't working.
*   **Analysis:** Anchors are inline elements; they only take up the width of their content, so there is no extra space inside them to "center" anything.
*   **Search:** `CSS how to center anchor elements`
*   **Solution found:** Apply `text-align: center` to the **parent container** (e.g., the `<nav>` element), not the anchors themselves.

---

## 2. Reading Documentation (MDN)

The **MDN Web Docs (Mozilla Developer Network)** is the gold standard for web documentation. It provides precise definitions, syntax, and browser compatibility info.

### How to Search MDN
*   **Query:** `MDN CSS [property-name]`
*   **Example:** `MDN CSS text-align`

### Anatomy of an MDN Page
1.  **Description:** A technical summary of what the property does (e.g., "sets the horizontal alignment of content inside a block element").
2.  **Interactive Demos:** Live code examples where you can click different values (like `left`, `right`, `center`) to see immediate results.
3.  **Syntax/Values:** Lists all possible valid values for the property.
    *   *Example for Border:* Shows that `border` is a shorthand for `border-width`, `border-style`, and `border-color`.
4.  **Browser Compatibility:** A table showing which browsers support the feature (crucial for modern/bleeding-edge CSS features).

---

## 3. Summary & Takeaways
*   **It is okay not to know everything.** Knowing *that* something is possible is often more important than knowing exactly *how* to write the code immediately.
*   **Process:**
    1.  Identify the problem.
    2.  Google it using the `CSS [problem] [context]` format.
    3.  Check Stack Overflow for quick fixes or specific scenarios.
    4.  Check MDN for deep understanding, syntax rules, and standard usage.
*   **Practice:** Try to solve small layout issues by Googling before asking for help. This builds independence and troubleshooting skills.