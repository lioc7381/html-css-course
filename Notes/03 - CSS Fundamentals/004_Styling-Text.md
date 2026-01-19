# Styling Text

## Overview
This section focuses on styling text using CSS properties. By applying these properties to the HTML elements created in previous lessons, the visual presentation of the project is significantly enhanced. The lesson covers six key properties for manipulating text appearance and introduces the concept of inheritance.

## Key Properties for Styling Text
The following properties are used to alter the appearance of text within HTML elements.

### 1. Font Size
*   **Property:** `font-size`
*   **Function:** Specifies the size of the text.
*   **Values:** Accepts various units, such as length (e.g., `px` for pixels) or keywords.
*   **Example:** `font-size: 26px;` sets the text height to exactly 26 pixels on the screen.
*   **Note:** The default browser font size is typically **16px**.

### 2. Font Family
*   **Property:** `font-family`
*   **Function:** Defines the typeface used for the text.
*   **Values:** Can range from specific font names to generic family names.
    *   **Generic Family:** `sans-serif` (cleaner look, no small lines at the ends of letters).
*   **Constraint:** You cannot simply list a local font unless the user also has it installed. Using a generic keyword like `sans-serif` ensures the browser picks an appropriate available font.
*   **Example:** `font-family: sans-serif;`

### 3. Text Transform
*   **Property:** `text-transform`
*   **Function:** Controls the capitalization of text.
*   **Common Values:**
    *   `uppercase`: Converts all characters to capital letters.
*   **Example:** `text-transform: uppercase;`

### 4. Font Style
*   **Property:** `font-style`
*   **Function:** Specifies the font style, such as italicization.
*   **Common Values:**
    *   `italic`: Slants the text.
*   **Example:** `font-style: italic;`

### 5. Line Height
*   **Property:** `line-height`
*   **Function:** Controls the vertical space between lines of text.
*   **Values:** Often used as a unitless number, acting as a multiplier of the current font size.
*   **Example:** `line-height: 1.5;` means the line height is 1.5 times the size of the font.
*   **Effect:** Increases readability by adding "breathing room" between lines.

### 6. Text Align
*   **Property:** `text-align`
*   **Function:** Sets the horizontal alignment of the text within its container.
*   **Common Values:**
    *   `center`: Centers the text.
    *   `left` / `right`: Aligns text to the left or right.
*   **Example:** `text-align: center;`

---

## Important Concept: Inheritance
During the styling of paragraph (`p`) elements, child elements nested inside them (like `<em>`, `<strong>`, and `<a>`) automatically adopted the styles set on the parent paragraph (such as `font-family` and `font-size`).

*   **Definition:** This mechanism is called **Inheritance**.
*   **Behavior:** Certain CSS properties applied to a parent element are passed down to its children elements.
*   **Significance:** This reduces the need to manually style every single nested element.
*   **Note:** A dedicated lecture on inheritance will follow later in the course.

---

## Practical Examples from the Lesson
The following CSS rules were applied to structure the project's text:

**1. Headings**
*   **H1 (Main Title):**
    *   `font-size: 26px;`
    *   `font-family: sans-serif;`
    *   `font-style: italic;` (demonstration)
*   **H2 (Article Heading):**
    *   `font-size: 40px;` (Demonstrates that H1 doesn't have to be the biggest visually; H1 is about semantic importance).
    *   `font-family: sans-serif;`
*   **H3 & H4:**
    *   Scaled sizes (30px, 20px) and `sans-serif` font.
    *   **H4** specifically used `text-transform: uppercase;` and `text-align: center;`.

**2. Paragraphs (`p`)**
*   `font-size: 22px;`
*   `font-family: sans-serif;`
*   `line-height: 1.5;` (Significantly improved readability).

**3. Lists (`li`)**
*   Styles are applied to the `li` (List Item) elements, **not** the `ul` or `ol` parent containers.
*   `font-size: 20px;`
*   `font-family: sans-serif;`

---

## Summary
*   **Properties Covered:** `font-size`, `font-family`, `text-transform`, `font-style`, `line-height`, `text-align`.
*   **Inheritance:** Nested elements often inherit styles from their parents.
*   **Unitless Line Height:** Best practice is to use a multiplier (e.g., `1.5`) rather than a fixed unit.
*   **Selectors:** Targeting a tag (like `p` or `h3`) applies the style to **all** instances of that tag on the page.