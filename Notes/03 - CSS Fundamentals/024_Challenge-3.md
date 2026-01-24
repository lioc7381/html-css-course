# CHALLENGE #3: Final Product Card Features

## Key Concepts
*   **Goal:** Finalize the "Shoe Product Card" by adding a "Sale" label and a color selection area.
*   **Techniques:** Absolute positioning, `display: inline-block`, using `<span>` or `<div>` for styling, and applying letter spacing.

---

## 1. The "Sale" Label
We need to create a red "SALE" badge positioned in the top-left corner of the product image.

### HTML Structure
Add a paragraph element with a class of `sale`. Place it semantically near the product details (e.g., near price/shipping).
```html
<p class="sale">Sale</p>
```

### CSS Styling
1.  **Visuals:** Red background, white text, uppercase, bold font.
2.  **Sizing:** Use `padding` to give it breathing room.
3.  **Display Behavior:** Set `display: inline-block` so the background only wraps the text content (and padding), rather than stretching the full width.
4.  **Letter Spacing:** Use `letter-spacing` (found via Googling) to spread the characters apart for a stylistic touch.

```css
.sale {
    background-color: #ec2f2f;
    color: white;
    font-size: 12px;
    text-transform: uppercase;
    font-weight: bold;
    padding: 7px 15px;
    display: inline-block; /* Crucial for sizing */
    letter-spacing: 2px;   /* Adds space between letters */
    
    /* Absolute Positioning Setup */
    position: absolute;
    top: -17px;
    left: -34px;
}
```

### Positioning Logic
To place the badge precisely:
1.  **Parent Context:** The container (article with class `product`) needs `position: relative`.
2.  **Child Placement:** The `.sale` element uses `position: absolute`.
3.  **Coordinates:** Use negative values for `top` and `left` to pull the badge slightly outside the container boundaries for an overlapping effect.

---

## 2. The Color Selection Swatches
We need a row of 6 colored squares representing product options.

### HTML Structure
Create a container div (`colors`) holding six empty divs, each with a `color` class and a specific modifier class for its background color.

```html
<div class="colors">
    <div class="color color-black"></div>
    <div class="color color-blue"></div>
    <div class="color color-red"></div>
    <div class="color color-yellow"></div>
    <div class="color color-green"></div>
    <div class="color color-brown"></div>
</div>
```

### CSS Styling
1.  **Shape:** Give the `.color` class a fixed `height` and `width` (e.g., 22px) to create squares.
2.  **Layout:** Use `display: inline-block` to place them side-by-side.
    *   *Note:* `inline` won't work because inline elements ignore height/width.
3.  **Spacing:** Add `margin-right` to separate the squares.

```css
.color {
    height: 22px;
    width: 22px;
    display: inline-block; /* Side-by-side squares */
    margin-right: 10px;
}
```

4.  **Specific Colors:** Target the modifier classes to apply background colors.

```css
.color-black { background-color: #000; }
.color-blue  { background-color: #2f6ee2; }
/* ... define red, yellow, green, brown ... */
```

---

## 3. Fixing Vertical Spacing (The Inline Element Issue)
We noticed a spacing issue where `margin-bottom` on the "Add to Cart" link wasn't pushing the color swatches down.

*   **Problem:** Anchor tags (`<a>`) are **inline** elements by default. Vertical margins (`top` and `bottom`) **do not apply** to inline elements.
*   **Solution:** Change the link's display property.

```css
.product-link {
    display: inline-block; /* Enables vertical margins */
    margin-bottom: 30px;
}
```

---

## Summary of New CSS Properties Used
*   **`letter-spacing`**: Controls the horizontal space between characters in text.
*   **`display: inline-block`**: Used extensively here for:
    *   The "Sale" badge (to fit content size).
    *   The Color squares (to sit side-by-side while respecting height/width).
    *   The Link (to respect vertical margins).