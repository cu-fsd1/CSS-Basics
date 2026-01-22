# CSS Grid + Bento Grids

A comprehensive guide and demonstration of CSS Grid layout techniques, including responsive design patterns and bento box layouts.

---

## Project Overview

This project showcases 12 different CSS Grid examples, from basic grid layouts to advanced responsive bento-style designs. It includes interactive demonstrations of grid properties, alignment techniques, and the differences between `auto-fill` and `auto-fit`.

---

## File Explanations

### index.html

The HTML file serves as the structure and container for all grid examples. It contains:

**Key Components:**

1. **Meta Tags & Head Section**
   - `<meta charset="UTF-8">` - Specifies UTF-8 character encoding
   - `<meta name="viewport">` - Enables responsive design for mobile devices
   - Links to `styles.css` for styling

2. **12 Example Sections**
   - **Example 1: Basic Grid (3 Columns)** - Demonstrates a simple 3-column grid with 6 items
   - **Example 2: Responsive Grid** - Uses `auto-fit` with `minmax()` for flexible, responsive layouts
   - **Example 3: Spans** - Shows how items can span multiple columns and rows using `grid-column: span` and `grid-row: span`
   - **Example 4: Bento (Named Areas)** - Creates a bento-style layout using CSS Grid named template areas
   - **Example 5: Bento (12-Column Spans)** - Alternative bento approach using a 12-column grid system
   - **Example 6: justify-content** - Aligns the entire grid horizontally within its container
   - **Example 7: justify-items** - Aligns items horizontally inside their individual grid cells
   - **Example 8: align-content** - Aligns the entire grid vertically within its container
   - **Example 9: align-items** - Aligns items vertically inside their individual grid cells
   - **Example 10: place-items** - Shorthand property that combines `justify-items` and `align-items`
   - **Example 11: auto-fill** - Creates empty grid tracks even when there are no items to fill them
   - **Example 12: auto-fit** - Collapses empty grid tracks, allowing items to expand and fill space

3. **Semantic Structure**
   - Each example is wrapped in `<section>` tags for semantic HTML
   - `.box` divs represent grid items with numbered content
   - `.grid` divs are the grid containers

---

### styles.css

The CSS file defines all styling and grid layout rules. It contains:

**Global Styles:**

```css
body {
  font-family: system-ui, Arial, sans-serif;
  margin: 20px;
  max-width: 1000px;
}
```
- Sets a clean, system font for all text
- Adds margins and constrains max-width for readability

**Grid Container Defaults:**

```css
.grid {
  display: grid;           /* Activates CSS Grid layout */
  gap: 12px;               /* Space between grid items */
  background-color: aqua;  /* Visual container background */
}
```

**Box (Grid Item) Styling:**

```css
.box {
  border: 1px dashed #333;
  padding: 14px;
  background: #f5f5f5;
  display: flex;           /* Flexbox for centering content */
  justify-content: center; /* Horizontal centering */
  align-items: center;     /* Vertical centering */
}
```
- Creates visual boxes with borders and padding
- Uses flexbox internally to center content

**Example-Specific Grid Rules:**

1. **Basic Grid** - `grid-template-columns: repeat(3, 1fr)` creates 3 equal-width columns
2. **Responsive Grid** - `repeat(auto-fit, minmax(180px, 1fr))` makes columns responsive; minimum 180px, expands to fill space
3. **Spans** - Uses `grid-column: span 2` and `grid-row: span 3` to make items larger
4. **Bento Areas** - `grid-template-areas` defines named regions like "hero", "notes", "cta", "mini"
5. **Bento 12-Column** - `repeat(12, 1fr)` creates a 12-column grid system
6. **Alignment Examples** - Various properties:
   - `justify-content: center` - Centers the entire grid
   - `justify-items: center` - Centers items within cells
   - `align-content: center` - Centers grid vertically
   - `align-items: center` - Centers items vertically within cells
   - `place-items: center` - Combines both

7. **auto-fill vs auto-fit**
   - `auto-fill` creates empty tracks with light pink background
   - `auto-fit` collapses empty tracks with light blue background

**Responsive Design:**

```css
@media (max-width: 700px) {
  .bento-areas {
    grid-template-columns: 1fr;
    grid-template-areas: "hero" "notes" "cta" "mini";
  }
}
```
- On mobile (screens ≤ 700px wide), bento layouts stack into single columns

**Visual Enhancements:**

- `.note` class adds highlighted note boxes with yellow background
- `.comparison-box` uses nested grid for side-by-side comparison layout
- Color-coded backgrounds help visualize grid behavior (aqua, pink, light blue)

---

## Glossary of Terms

| Abbreviation | Full Form | Description |
|---|---|---|
| **CSS** | Cascading Style Sheets | Language used for styling web pages and layouts |
| **HTML** | HyperText Markup Language | Standard markup language for creating web page structure |
| **1fr** | Fraction Unit | A relative unit in CSS Grid representing one fraction of available space |
| **minmax()** | Minimum-Maximum Function | CSS Grid function that sets minimum and maximum track sizes |
| **auto-fit** | Automatic Fit | CSS Grid property that creates grid tracks and collapses empty ones |
| **auto-fill** | Automatic Fill | CSS Grid property that creates grid tracks including empty ones |
| **px** | Pixels | Fixed unit of measurement for screen display |
| **gap** | Grid Gap | Space between grid items (rows and columns) |
| **grid-column** | Grid Column Property | Specifies which column(s) a grid item occupies |
| **grid-row** | Grid Row Property | Specifies which row(s) a grid item occupies |
| **grid-area** | Grid Area Property | Assigns a grid item to a named template area |
| **grid-template-columns** | Grid Template Columns | Defines the number and size of columns in a grid |
| **grid-template-rows** | Grid Template Rows | Defines the number and size of rows in a grid |
| **grid-template-areas** | Grid Template Areas | Defines named grid regions using ASCII-art layout |
| **repeat()** | Repeat Function | CSS function to repeat grid track definitions |
| **justify-content** | Justify Content Property | Aligns entire grid horizontally within its container |
| **justify-items** | Justify Items Property | Aligns grid items horizontally within their cells |
| **align-content** | Align Content Property | Aligns entire grid vertically within its container |
| **align-items** | Align Items Property | Aligns grid items vertically within their cells |
| **place-items** | Place Items Property | Shorthand combining `justify-items` and `align-items` |
| **span** | Span Keyword | Keyword to make a grid item occupy multiple tracks |
| **meta** | Metadata | Information about the HTML document (charset, viewport, etc.) |
| **semantic** | Semantic HTML | HTML that carries meaning about the content (e.g., `<section>`, `<header>`) |
| **flexbox** | Flexible Box Layout | CSS layout module for flexible, responsive layouts |
| **responsive** | Responsive Design | Web design that adapts to different screen sizes |
| **bento** | Bento Box Layout | Grid layout style inspired by Japanese bento boxes with varied-sized compartments |
| **media query** | Media Query | CSS technique to apply styles based on device characteristics |
| **rgba** | Red-Green-Blue-Alpha | Color model with transparency (alpha) channel |

---

## How to Use

1. Open `index.html` in your web browser
2. Scroll through each example to see CSS Grid in action
3. Inspect elements using browser DevTools (F12 or Right-click → Inspect) to examine:
   - Grid structure and layout properties
   - How items span columns and rows
   - Alignment and spacing behavior
   - Responsive behavior at different screen widths

---

## Key Learning Points

- **Grid vs Flexbox**: Grid is 2D (rows and columns), Flexbox is 1D (single direction)
- **Responsive Design**: Use `auto-fit` or `auto-fill` with `minmax()` for mobile-friendly layouts
- **Named Areas**: `grid-template-areas` provides readable, ASCII-art style grid definitions
- **Alignment Properties**: Different properties align different things (container vs items, horizontal vs vertical)
- **Bento Layouts**: Combine spans and named areas to create visually interesting, magazine-style designs

