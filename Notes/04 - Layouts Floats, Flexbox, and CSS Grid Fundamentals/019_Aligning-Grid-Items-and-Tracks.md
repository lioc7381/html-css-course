# Aligning Grid Items and Tracks

## Overview
Alignment in CSS Grid shares similarities with Flexbox but offers more control due to the two-dimensional nature of grids. You can align the entire grid within its container (distributing empty space) and align individual items within their specific grid cells.

**Main Goal:** To master the four key alignment properties: `justify-content`, `align-content`, `justify-items`, and `align-items`, along with individual overrides using `self`.

---

## Detailed Breakdown

### 1. Aligning Tracks Inside the Container
These properties are used to distribute **empty space** within the grid container when the total size of the grid tracks (columns/rows) is smaller than the container itself.

*   **Properties ending in `-content`**: Control the alignment of the *entire grid structure* relative to the container.
*   **Prerequisite:** The grid must be smaller than the container for these to have a visible effect.

#### Horizontal Alignment (Row Axis)
*   **Property:** `justify-content`
*   **Values:**
    *   `center`: Centers the whole grid horizontally.
    *   `space-between`: Pushes the first column to the start and the last to the end, distributing space evenly between them.
    *   `start` / `end`: Aligns the grid to the left or right edge.
    *   *Note:* Unlike Flexbox, use `start` and `end`, not `flex-start` or `flex-end`.

#### Vertical Alignment (Column Axis)
*   **Property:** `align-content`
*   **Values:**
    *   `center`: Centers the whole grid vertically.
    *   `start` / `end`: Aligns grid to top or bottom.
    *   `space-between`: Distributes rows to the top and bottom edges.

**Example:**
```css
.container {
    /* Centers the grid block both horizontally and vertically inside the container */
    justify-content: center;
    align-content: center;
}
```

### 2. Aligning Items Inside Cells
These properties control the position of grid items *within their defined grid cells*.

*   **Properties ending in `-items`**: Control the alignment of *items* relative to their specific cell boundaries.
*   **Default Behavior:** Both properties default to `stretch`, causing items to fill the entire cell.

#### Horizontal Alignment (Row Axis)
*   **Property:** `justify-items`
*   **Values:**
    *   `stretch` (default): Item fills the width of the cell.
    *   `center`: Item is centered horizontally within the cell.
    *   `start` / `end`: Item aligns to the left or right edge of the cell.

#### Vertical Alignment (Column Axis)
*   **Property:** `align-items`
*   **Values:**
    *   `stretch` (default): Item fills the height of the cell.
    *   `center`: Item is centered vertically within the cell.
    *   `start` / `end`: Item aligns to the top or bottom edge of the cell.

**Example:**
```css
.container {
    /* Centers all items perfectly in the middle of their respective cells */
    justify-items: center;
    align-items: center;
}
```

### 3. Overriding Alignment for Individual Items
Just like in Flexbox, you can override the container-level alignment settings for specific grid items.

*   **Properties:** `justify-self` and `align-self`.
*   **Usage:** Applied directly to the grid **item**, not the container.

**Example:**
```css
.item-3 {
    /* Overrides the container's align-items setting */
    align-self: end;   /* Moves this item to the bottom of its cell */
    
    /* Overrides the container's justify-items setting */
    justify-self: end; /* Moves this item to the right of its cell */
}
```

---

## Key Takeaways

| Alignment Scope | Horizontal (Row Axis) | Vertical (Column Axis) |
| :--- | :--- | :--- |
| **Grid Inside Container** (Distributes empty space) | `justify-content` | `align-content` |
| **Items Inside Cells** (Moves items within cell) | `justify-items` | `align-items` |
| **Individual Item Override** (Specific item only) | `justify-self` | `align-self` |

*   **Terminology:** Properties ending in `-content` align the whole grid (tracks). Properties ending in `-items` align the content (items) within the cells.
*   **Syntax Difference:** CSS Grid uses `start` and `end`, whereas Flexbox uses `flex-start` and `flex-end`.
*   **Centering:** A common pattern for perfect centering of an item is `justify-items: center;` and `align-items: center;`.