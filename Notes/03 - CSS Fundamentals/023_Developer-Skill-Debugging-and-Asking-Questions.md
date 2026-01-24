# Developer Skill #2: Debugging and Asking Questions

## Key Concepts
*   **Debugging:** The process of identifying and removing errors (bugs) from your code.
*   **Common HTML/CSS Bugs:** Unclosed tags, validation errors, selector conflicts, and typos.
*   **Tools:** HTML Validator, Diff Checkers, Browser DevTools.
*   **Asking for Help:** How to properly structure questions and share code using CodePen.

---

## 1. Debugging HTML
HTML errors often result in visual glitches where styles apply to more elements than intended or layouts break.

### Common Issues
*   **Unclosed Tags:** Forgetting to close a tag (e.g., `<strong>` or `<div>`) causes the browser to apply that tag's effect to everything following it.
    *   *Symptom:* Text suddenly becomes bold or styled unexpectedly all the way down the page.
    *   *Fix:* Locate where the unexpected styling starts and check the code immediately preceding it.
*   **Incorrect Nesting:** Placing elements where they don't belong (e.g., unclosed `<li>` tags).

### Tools
*   **HTML Validator:** An automated tool to check markup validity.
    *   *How to use:* Copy your HTML code and paste it into a validator like the [W3C Markup Validation Service](https://validator.w3.org/).
    *   *Benefit:* It points out unclosed tags, duplicate attributes (e.g., two `width` attributes), and misspelled attributes.
*   **Diff Checker:** A tool to compare two versions of a file side-by-side.
    *   *Use Case:* Compare your broken code against the instructor's working code to find discrepancies.
    *   *Tool:* [Diffchecker.com](https://www.diffchecker.com/).

---

## 2. Debugging CSS
CSS bugs usually manifest as styles not applying, conflicting styles, or layout issues.

### Common Issues
1.  **Selector Conflicts (Specificity):**
    *   *Problem:* You write a rule (e.g., `margin-top: 10px`), but a previous, more specific rule (e.g., `nav a link { margin-top: 100px; }`) overrides it.
    *   *Fix:* Keep selectors simple. Inspect the element in DevTools to see which rule is crossing out the other. Avoid over-complicated selectors.
2.  **Typos:**
    *   *Problem:* Misspelling a property (e.g., `marrgin-right`) results in the browser ignoring that line.
    *   *Fix:* Use DevTools. Inspect the element; misspelled properties often show an "Unknown property name" warning icon.
3.  **Linking Errors:**
    *   *Problem:* No styles appear at all.
    *   *Fix:* Check the `<link>` tag in the HTML `<head>`. Ensure the `href` path correctly points to the CSS file.

### Using DevTools for Debugging
*   **Inspect Element:** Right-click an element and select "Inspect".
*   **Live Editing:** You can click on property values (e.g., font size numbers) and use the **Up/Down arrow keys** to adjust them in real-time.
    *   *Tip:* Hold `Shift` + `Arrow Key` to increment by 10.
*   **Computed Tab:** Shows the final values applied to an element after all cascading rules are resolved.

---

## 3. Asking Questions Effectively
If you cannot solve a bug after trying the tools above, asking for help is the next step.

### Preparation
1.  **Isolate the Problem:** Don't just say "it doesn't work." Identify what specific part is broken.
2.  **Create a Reproduction:**
    *   **CodePen:** Go to [CodePen.io](https://codepen.io/).
    *   Create a new Pen (`/pen`).
    *   Paste your relevant HTML and CSS.
    *   Save and copy the URL.

### Where to Ask
*   **Stack Overflow:** For general programming questions.
*   **Course Q&A (Udemy):** For specific course-related issues.

### Best Practice
*   **Never** paste huge blocks of code directly into a forum post.
*   **Always** provide a link to a live example (like CodePen) so others can see the code and the result instantly.