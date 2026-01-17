# Introduction to HTML

## Key Concepts & Overview
*   **Definition:** HTML stands for **Hypertext Markup Language**.
*   **Role:** It is one of the core web technologies (alongside CSS and JavaScript) used to **structure and describe** the content of a webpage.
*   **Nature:** HTML is a **markup language**, not a programming language. It describes specific content rather than executing programming logic.
*   **Browser Function:** Web browsers (e.g., Google Chrome) understand HTML code and **render** it as a visible website.

## Detailed Breakdown

### 1. HTML Elements
HTML uses **elements** to describe different types of content on a page. 
*   **Purpose:** Elements tell the browser what type of content is being displayed.
*   **Examples:**
    *   Paragraphs (represented by the `<p>` element)
    *   Links
    *   Page headings
    *   Images
    *   Videos

### 2. The Anatomy of an HTML Element
An HTML element typically consists of three distinct parts. The instructor uses the **paragraph element** (`<p>`) to illustrate this structure:

#### A. The Opening Tag
*   Consists of the name of the element wrapped in **less than** (`<`) and **greater than** (`>`) symbols.
*   **Example:** `<p>`

#### B. The Content
*   This is the information located between the tags.
*   **Types of Content:**
    *   **Text:** Simple written content.
    *   **Child Elements:** An element can contain another element inside it.
*   *Note:* Some elements, like images, have no content at all.

#### C. The Closing Tag
*   Identical to the opening tag but includes a **forward slash** before the element name.
*   **Example:** `</p>`

### 3. Visual Structure
| Component | Syntax | Description |
| :--- | :--- | :--- |
| **Opening Tag** | `<p>` | Starts the element. |
| **Content** | `...` | Text or other elements inside. |
| **Closing Tag** | `</p>` | Ends the element. |
| **Full Element** | `<p>...</p>` | The entire structure combined. |

### Practical Examples & Exceptions

*   **Standard Element:**
    > `<p>This is a paragraph.</p>`
    *   Includes opening tag, text content, and closing tag.

*   **Content-less Elements (e.g., Images):**
    *   These elements do **not** have content.
    *   They consist **only** of an opening tag.
    *   They do **not** use a closing tag.

## Summary & Key Takeaways
*   **HTML** is used to markup and structure web content, interpreted by browsers to render websites.
*   The basic unit of HTML is the **element**.
*   **Standard Anatomy:** Opening Tag + Content + Closing Tag.
*   **Closing tags** are distinguished by a slash (e.g., `</p>`).
*   **Empty elements** (like images) omit the closing tag entirely.