# Text Elements: Headings, Paragraphs, and Formatting

## Key Concepts & Overview
*   **Summary:** This lesson focuses on the core elements used to structure and format text within an HTML document.
*   **Main Goal:** To apply headings (`<h1>` through `<h6>`), paragraphs (`<p>`), and text styles (bold and italic) to the project while introducing **Semantic HTML** best practices.

## Detailed Breakdown

### 1. Headings
Headings are used to break up large blocks of text into logical sections and establish a hierarchy.

*   **Hierarchy Levels:** There are six heading levels, ranging from `<h1>` (largest) to `<h6>` (smallest).
*   **Visuals:** Browsers automatically render these with different sizes to visually represent importance.
*   **Best Practice:**
    *   **One H1 per page:** An HTML document should typically have only *one* primary heading (`<h1>`).
    *   **Multiple Sub-headings:** You may have multiple `<h2>` through `<h6>` elements as needed.

**Project Application:**
*   `<h1>`: "The Code Magazine" (Main Blog Title)
*   `<h2>`: "The Basic Language of the Web: HTML" (Article Title)
*   `<h3>`: "What is HTML?" and "Why Should You Learn HTML?" (Section Titles)

### 2. Paragraphs
*   **Element:** `<p>`
*   **Purpose:** A generic element used to mark up blocks of text.
*   **Usage:** Used for the main content body of the blog post.

### 3. Comments
Comments allow developers to write code or notes that are **not rendered** in the browser window.

*   **Syntax:** Starts with `<!--` and ends with `-->`.
*   **Uses:**
    *   Leaving notes for developers.
    *   Temporarily hiding code (e.g., hiding the practice H1-H6 tags without deleting them).
*   **Example:** `<!-- This is a comment -->`

### 4. Text Formatting & Semantic HTML
The lesson introduces how to style text (Bold and Italic) and distinguishes between "old" HTML tags and modern "semantic" tags.

#### Bold Text
*   **Old Element:** `<b>`
    *   Stands for "Bold."
    *   **Issue:** It has no specific meaning (non-semantic).
*   **New/Correct Element:** `<strong>`
    *   **Usage:** Used for text that is important and should stand out.
    *   **Semantic Meaning:** Defines text as "strong importance."
    *   **Visual:** Renders as bold by default.

#### Italic Text
*   **Old Element:** `<i>`
    *   Stands for "Italic."
    *   **Issue:** It has no specific meaning (non-semantic).
*   **New/Correct Element:** `<em>`
    *   **Usage:** Used to emphasize specific words.
    *   **Semantic Meaning:** Stands for "Emphasize."
    *   **Visual:** Renders as italic by default.

### 5. Practical Example: Coding Challenge
**Task:** Make the first letter of each word in the phrase "HyperText Markup Language" bold (H, T, M, L).

**Solution:** Wrap the individual letters in `<strong>` tags.
```html
<p>
  <strong>H</strong>yper<strong>T</strong>ext
  <strong>M</strong>arkup
  <strong>L</strong>anguage
</p>
```

## Summary & Key Takeaways
*   **Hierarchy matters:** Use `<h1>` for the main title (limit to one) and `<h2>`-`<h6>` for subsections.
*   **Semantics matter:**
    *   Use `<strong>` instead of `<b>` for bolding.
    *   Use `<em>` instead of `<i>` for italics.
*   **Comments:** Use `<!-- -->` to hide content from the user but keep it in the source code.
*   **Structure:** Wrap standard text blocks in `<p>` tags.