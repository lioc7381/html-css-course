# CHALLENGE-3

## Overview
**Coding Challenge #3** revisits the layout from the previous challenge but refactors it to use **CSS Grid** instead of Flexbox. The goal is to create a 2-dimensional layout that includes a product title, three columns (image + 2 info sections), and a button footer, all within a single grid container.

**Main Goal:** Convert the previous Flexbox-based product layout into a CSS Grid layout, ensuring proper column sizing and item spanning.

---

## Detailed Breakdown

### 1. Preparation
*   **Remove Wrapper Div:** In the previous challenge, the three middle columns were wrapped in a `<div>` to create a flex row. This wrapper must be deleted.
*   **Target Element:** The `article` with the class `.product` now acts as the single parent container for all items (title, image, info boxes, button).
*   **Cleanup:** Remove old Flexbox properties (like `display: flex`) and helper classes (like clearfix) that are no longer needed.

### 2. Defining the Grid Container
The `.product` element becomes the grid container.
*   **Property:** `display: grid;`

### 3. Setting Column Sizes
We need three columns in total.
*   **Column 1 (Image):** The image has a fixed width of `250px`. To ensure the column fits perfectly around it, we set this column explicitly to `250px`.
*   **Column 2 & 3 (Info):** These should share the remaining space equally.
*   **Code:**
    ```css
    .product {
        grid-template-columns: 250px 1fr 1fr;
    }
    ```

### 4. Spanning Full-Width Items
The product title and the "Add to Cart" button need to stretch across the top and bottom of the container, covering all three columns.
*   **Elements:** `.product-title` and `.add-cart` (button).
*   **Technique:** Use the `grid-column` property with the value `1 / -1` to span from the first line to the very last line.
    ```css
    .product-title,
    .add-cart {
        grid-column: 1 / -1;
    }
    ```

### 5. Managing Gaps
The previous Flexbox layout used the `gap` property (or margins). CSS Grid uses `column-gap` to space the columns horizontally.
*   **Property:** `column-gap` (e.g., `20px` or whatever was used previously).
*   **Note:** Vertical gaps were not explicitly added in the solution, implying the default behavior or existing margins were sufficient, but `row-gap` could be used if needed.

---

## Key Takeaways
*   **Simplification:** CSS Grid often removes the need for nested wrapper `div`s required by Flexbox.
*   **Fixed + Flexible Mixing:** You can easily mix fixed widths (pixels) and flexible widths (`fr`) in `grid-template-columns`.
*   **Full Span Trick:** `grid-column: 1 / -1` is the standard way to make headers and footers span the full width of an explicit grid.
*   **Implicit Rows:** The row containing the image and info boxes automatically adjusted its height to `250px` (the height of the image), demonstrating how Grid adapts to content size.