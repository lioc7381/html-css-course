# Building a Simple Float Layout

## Overview
This lesson demonstrates how to construct a basic web page layout using the concepts of **floats** and **clearing floats**. The objective is to arrange the main content (`article`) on the left and a sidebar (`aside`) on the right, while ensuring the footer remains at the bottom, unaffected by the floating elements above it.

## Key Concepts

### 1. Identifying the Layout Structure
The goal layout consists of three main parts:
*   **Header:** Spans the full width at the top (already implemented).
*   **Content Area:** Split into two columns:
    *   **Main Content (`article`):** Left side.
    *   **Sidebar (`aside`):** Right side.
*   **Footer:** Spans the full width at the bottom.

### 2. Setting Up the Container
To create a standard page layout, the main container width is increased.
*   **Width:** Set to **1200px**.
*   **Note:** This width will be standard for all layout methods (Float, Flexbox, Grid) used in this course.

### 3. Creating Columns with Floats
To place block-level elements side-by-side, specific widths must be assigned because block elements default to 100% width.

*   **Total Width:** 1200px.
*   **Distribution:**
    *   **Article (Left):** Originally 900px (later adjusted to 825px).
    *   **Aside (Right):** 300px.
*   **CSS Implementation:**
    ```css
    article {
        width: 825px; /* Adjusted to create a gap */
        float: left;
    }
    aside {
        width: 300px;
        float: right;
    }
    ```

### 4. Creating Gaps Between Columns
Instead of using margins, gaps in float layouts can be created by reducing the width of one or both columns.
*   **Technique:** Reduce `article` width from 900px to 825px.
*   **Result:** A 75px empty space appears between the left-floated article and the right-floated aside.

### 5. Clearing the Footer
When elements above the footer are floated, the footer (which comes next in the HTML) naturally tries to wrap around them.
*   **Problem:** The footer floats up and wraps around the content/sidebar.
*   **Solution:** Use the `clear` property on the footer itself.
*   **Why no Clearfix?** Since the footer is an existing element following the floats, we don't need an empty div or a pseudo-element. We can simply apply the rule to the footer.
*   **CSS:**
    ```css
    footer {
        clear: both;
    }
    ```

## Summary & Key Takeaways
*   **Floats for Layout:** By assigning specific widths and floating elements left and right, you can create multi-column layouts.
*   **Gap Management:** Gaps can be created by leaving "empty space" in the container width calculation.
*   **Clearing is Essential:** Any non-floated element following floated elements must be "cleared" to prevent it from wrapping around the floats.
*   **Visual Debugging:** Temporarily adding background colors to layout elements helps visualize their size and position during development.