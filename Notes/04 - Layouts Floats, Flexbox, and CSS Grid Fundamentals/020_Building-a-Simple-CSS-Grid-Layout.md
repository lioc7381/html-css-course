# Building a Simple CSS Grid Layout

## Overview
This lesson demonstrates how to rebuild the blog post layout using CSS Grid, replacing previous methods like float and Flexbox for the main 2-dimensional structure. The goal is to create a robust layout with a header, article, sidebar (aside), and footer.

**Main Goal:** To implement a full 2-dimensional page layout using CSS Grid properties for columns, gaps, and item spanning.

---

## Detailed Breakdown

### 1. Strategy: Hybrid Approach
The lesson emphasizes using the right tool for the right job.
*   **CSS Grid:** Used for the overall, high-level **2-dimensional** page layout (Header, Article + Aside, Footer).
*   **Flexbox:** Retained for smaller, **1-dimensional** component layouts (e.g., navigation menu, author info, related posts row).

### 2. Setup
*   **Clean Up:** Remove or comment out old Flexbox code used for the main layout (specifically the `.row` wrapper and flex properties on the container).
*   **HTML Structure:** The container now directly holds the four main semantic elements: `<header>`, `<article>`, `<aside>`, and `<footer>`.

### 3. Grid Container Definition
The main container is turned into a grid.
*   **Display:** `display: grid;`
*   **Columns:** Defined to match the previous design requirements.
    *   **Article:** Takes up the remaining flexible space (`1fr`).
    *   **Aside:** Fixed width of `300px`.
    *   **Code:** `grid-template-columns: 1fr 300px;`

### 4. Item Placement & Spanning
By default, the 4 items (header, article, aside, footer) will fill the first 4 cells (2 rows of 2 columns). We need to span the header and footer across the full width.

*   **Header & Footer:** Spanning from the first grid line to the very end.
    *   **Property:** `grid-column: 1 / -1;`
    *   **Why -1?** It ensures the item spans to the very last line regardless of how many columns exist.

*   **Article & Aside:** Automatically fall into place in the middle row (Article in col 1, Aside in col 2) because they naturally follow the Header in the source order.

### 5. Managing Spacing (Gaps)
Instead of using margins on individual elements, CSS Grid allows centralized spacing control on the container.

*   **Horizontal Space:** Replaces margins between article and sidebar.
    *   **Property:** `column-gap: 75px;`
*   **Vertical Space:** Replaces bottom margins on header and article.
    *   **Property:** `row-gap: 60px;`
*   **Benefit:** Keeps spacing logic in one place (the container) rather than scattered across child elements.

### 6. Alignment Adjustment
By default, grid items stretch to fill the height of their row. The sidebar (`aside`) was stretching to match the height of the `article`.

*   **Goal:** Make the sidebar sit at the top of its cell, matching its natural content height.
*   **Property:** `align-items: start;` (applied to the container).
*   **Result:** The sidebar aligns to the top (start) of the row and does not stretch.

---

## Key Takeaways
*   **Implicit Rows:** We did not define `grid-template-rows`. CSS Grid automatically created rows based on the content height (e.g., the height of the Article defined the height of the middle row).
*   **Clean Code:** Grid reduces the need for wrapper `<div>`s (like `.row`) and scattered `margin` rules.
*   **Separation of Concerns:** Use Grid for the main layout structure and Flexbox for internal component alignment.