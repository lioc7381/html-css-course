# Images and HTML Attributes

## Key Concepts & Overview
*   **Summary:** This lesson introduces the implementation of images in HTML and the concept of **attributes** to provide additional information to elements.
*   **Main Goal:** To insert images into the "Code Magazine" blog post (a main article image and an author photo) and correctly use essential image attributes like `src`, `alt`, `width`, and `height`.
*   **Key Insight:** Images are **void elements** (they have no closing tag and no inner content) and rely entirely on attributes to function.

## Detailed Breakdown

### 1. The Image Element (`<img>`)
*   **Type:** Self-closing (void) element.
*   **Syntax:** `<img ... />` (Note the space and slash at the end, though the slash is optional in HTML5, it's good practice for clarity).
*   **Function:** Embeds an image file into the webpage.

### 2. HTML Attributes
Attributes provide data *about* an element. They are written inside the opening tag (or the only tag for void elements).
*   **Syntax:** `attribute="value"`

#### Essential Image Attributes
1.  **`src` (Source):**
    *   **Purpose:** Specifies the path to the image file.
    *   **Example:** `src="post-img.jpg"`
2.  **`alt` (Alternative Text):**
    *   **Purpose:** Provides a text description of the image.
    *   **Importance:**
        *   **Accessibility:** Screen readers read this text to visually impaired users.
        *   **SEO:** Helps search engines understand image content.
        *   **Fallback:** Displays if the image fails to load.
    *   **Example:** `alt="HTML code on a screen"`
3.  **`width` and `height`:**
    *   **Purpose:** Defines the dimensions of the image in pixels.
    *   **Behavior:** If only one is specified (e.g., width), the browser automatically adjusts the other to maintain the aspect ratio.
    *   **Example:** `width="500" height="200"`

### 3. Practical Examples from the Project

#### Main Blog Image
*   **Placement:** After the author paragraph (barrier between header and article).
*   **Code:**
    ```html
    <img 
      src="post-img.jpg" 
      alt="HTML code on a screen" 
      width="500" 
      height="200" 
    />
    ```

#### Author Image (Coding Challenge)
*   **Placement:** Above the author description paragraph.
*   **Dimensions:** 50x50 pixels.
*   **Code:**
    ```html
    <img 
      src="laura-jones.jpg" 
      alt="Headshot of Laura Jones" 
      height="50" 
      width="50" 
    />
    ```

### 4. Attributes on Other Elements
Attributes are not unique to images. They are used throughout HTML to configure elements.

#### Document Language
*   **Element:** `<html>`
*   **Attribute:** `lang`
*   **Purpose:** Declares the language of the webpage (e.g., `en` for English).
*   **Example:** `<html lang="en">`

#### Character Set (Metadata)
*   **Element:** `<meta>` (placed inside `<head>`)
*   **Attribute:** `charset`
*   **Purpose:** Defines the character encoding (usually UTF-8 for standard English characters).
*   **Code:** `<meta charset="UTF-8" />`

## Summary & Key Takeaways
*   **`<img>` elements** are self-closing and require the `src` attribute to work.
*   **Always include `alt` text** for accessibility and SEO.
*   **Control size** using `width` and `height` attributes to prevent layout shifts or oversized images.
*   **Global Attributes:** Use `lang="en"` on the `<html>` tag and `<meta charset="UTF-8" />` in the `<head>` to ensure the browser interprets the document text correctly.