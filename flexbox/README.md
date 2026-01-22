# Flexbox Learning Project

This project demonstrates various CSS Flexbox properties and techniques through practical examples.

---

## 📁 File Structure

- **index.html** - Main HTML structure with flexbox examples
- **styles.css** - CSS styling and flexbox utilities
- **README.md** - Project documentation (this file)

---

## 📄 index.html - Detailed Explanation

### Document Structure
```html
<!DOCTYPE html>
<html lang="en">
```
- Standard HTML5 document declaration
- Sets language to English for accessibility

### Head Section
```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta http-equiv="X-UA-Compatible" content="ie=edge" />
  <title>HTML + CSS</title>
  <link rel="stylesheet" href="styles.css" />
</head>
```
- **charset**: Sets character encoding to UTF-8
- **viewport**: Makes page responsive for mobile devices
- **X-UA-Compatible**: Ensures compatibility with Internet Explorer
- **link**: Connects external CSS stylesheet

### Body Content

The body contains a main container with 11 different flexbox demonstrations:

#### Example 1: Justify Content - Center
```html
<div class="flex-container justify-center">
  <div class="box">Item 1</div>
  <div class="box">Item 2</div>
</div>
```
- Demonstrates horizontal centering along the main axis
- Uses `justify-content: center`

#### Example 2: Align Items - Center
```html
<div class="flex-container big-container align-center">
  <div class="box">Item 1</div>
  <div class="box">Item 2</div>
</div>
```
- Demonstrates vertical centering along the cross axis
- Uses `align-items: center` with a taller container

#### Example 3: Perfect Centering
```html
<div class="flex-container big-container center-both">
  <div class="box">Centered Box 1</div>
  <div class="box">Centered Box 2</div>
</div>
```
- Combines both horizontal and vertical centering
- Uses both `justify-content: center` and `align-items: center`

#### Example 4: Flex Growth
```html
<div class="flex-container">
  <div class="box flex-1">Flex: 1</div>
  <div class="box flex-1">Flex: 1</div>
  <div class="box flex-1">Flex: 1</div>
</div>
```
- All three boxes grow equally to fill available space
- Each has `flex: 1` property

#### Example 5: Flex Wrap
```html
<div class="flex-container wrap-demo">
  <div class="box">1</div>
  <!-- 6 items total -->
</div>
```
- Demonstrates `flex-wrap: wrap`
- Items wrap to new line when container width is exceeded

#### Example 6: Flex Grow with Different Values
```html
<div class="flex-container">
  <div class="box grow-1">Grow 1</div>
  <div class="box grow-2">Grow 2</div>
  <div class="box">Standard</div>
</div>
```
- Shows proportional growth
- `grow-2` takes twice as much space as `grow-1`

#### Example 7: Row Reverse
```html
<div class="flex-container row-reverse">
  <div class="box">Item 1 (Start)</div>
  <div class="box">Item 2</div>
  <div class="box">Item 3 (End)</div>
</div>
```
- Reverses the order of flex items
- Uses `flex-direction: row-reverse`

#### Example 8: Wrap Reverse
```html
<div class="flex-container wrap-demo wrap-reverse">
  <!-- 6 items -->
</div>
```
- Wraps items in reverse order
- Uses `flex-wrap: wrap-reverse`

#### Example 9: Align Content
```html
<div class="flex-container big-container wrap-demo content-between">
  <div class="box">Row 1</div>
  <!-- 4 items -->
</div>
```
- Controls spacing between wrapped rows
- Uses `align-content: space-between`

#### Example 10: Align Self & Order
```html
<div class="flex-container big-container">
  <div class="box self-start">Self: Start</div>
  <div class="box self-center order-last">Self: Center (Order: last)</div>
  <div class="box self-end order-first">Self: End (Order: first)</div>
</div>
```
- `align-self`: Individual item alignment
- `order`: Changes visual order of items

#### Example 11: Multiple Grow Values
```html
<div class="flex-container big-container justify-center items-center">
  <div class="box grow-1">Apple</div>
  <div class="box grow-2">Orange</div>
  <div class="box grow-3">Mango</div>
</div>
```
- Demonstrates proportional growth with different ratios
- Mango takes 3x, Orange 2x, and Apple 1x of available space

---

## 🎨 styles.css - Detailed Explanation

### Universal Reset
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```
- Removes default browser margins and padding
- `box-sizing: border-box` makes width/height calculations include padding and border

### Body Styling
```css
body {
  margin: 0;
  font-family: system-ui, -apple-system, sans-serif;
  background-color: #ffffff;
  color: #333;
  line-height: 1.6;
}
```
- Uses system fonts for better performance
- Sets clean white background with dark gray text
- Comfortable line height for readability

### Main Container
```css
.container {
  max-width: 800px;
  margin: 40px auto;
  padding: 0 20px;
}
```
- Limits content width to 800px
- Centers container with `margin: auto`
- Adds horizontal padding for mobile devices

### Flex Container Base
```css
.flex-container {
  display: flex;
  gap: 10px;
  background: #f7d4d4;
  padding: 10px;
  border: 1px solid #eee;
  border-radius: 4px;
}
```
- `display: flex` activates flexbox layout
- `gap: 10px` adds spacing between flex items
- Pink background makes container visible
- Rounded corners for modern look

### Alignment Utilities

#### Justify Content (Main Axis)
```css
.justify-center {
  justify-content: center;
}
```
- Centers items horizontally (in row direction)

#### Align Items (Cross Axis)
```css
.align-center {
  align-items: center;
}
```
- Centers items vertically (perpendicular to main axis)

#### Perfect Centering
```css
.center-both {
  justify-content: center;
  align-items: center;
}
```
- Combines both for complete centering

### Wrapping
```css
.wrap-demo {
  flex-wrap: wrap;
}

.wrap-reverse {
  flex-wrap: wrap-reverse;
}
```
- `wrap`: Items wrap to next line when needed
- `wrap-reverse`: Items wrap in reverse order

### Container Sizing
```css
.big-container {
  height: 300px;
}
```
- Creates taller container to demonstrate vertical alignment

### Flex Properties
```css
.flex-1 {
  flex: 1;
}
```
- Shorthand for `flex-grow: 1, flex-shrink: 1, flex-basis: 0`
- Item grows to fill available space

### Box (Flex Item) Styling
```css
.box {
  border: 2px dashed #333;
  padding: 14px;
  background: #f5f5f5;
  display: flex;
  align-items: center;
  justify-content: center;
  min-width: 140px;
}
```
- Dashed border for visibility
- Light gray background
- Centers text inside box
- Minimum width prevents boxes from becoming too small

### Growth Utilities
```css
.grow-1 { flex-grow: 1; }
.grow-2 { flex-grow: 2; }
.grow-3 { flex-grow: 3; }
.grow-4 { flex-grow: 4; }
```
- Controls proportional growth of flex items
- Higher number = more space allocated

### Direction Utilities
```css
.row-reverse {
  flex-direction: row-reverse;
}

.column {
  flex-direction: column;
}

.column-reverse {
  flex-direction: column-reverse;
}
```
- Changes the direction and order of flex items
- `row-reverse`: Right to left
- `column`: Top to bottom
- `column-reverse`: Bottom to top

### Align Content (Multi-line)
```css
.content-between {
  align-content: space-between;
}

.content-around {
  align-content: space-around;
}
```
- Controls spacing between wrapped rows
- Only works with `flex-wrap: wrap`

### Align Self (Individual Items)
```css
.self-start {
  align-self: flex-start;
}

.self-end {
  align-self: flex-end;
}

.self-center {
  align-self: center;
}
```
- Overrides container's `align-items` for individual items
- Allows one item to align differently

### Order Control
```css
.order-first {
  order: -1;
}

.order-last {
  order: 1;
}
```
- Changes visual order without modifying HTML
- Lower numbers appear first
- Default order is 0

---

## 📝 Note

There is no **script.js** file in this project. This is a pure HTML and CSS demonstration focused on Flexbox layouts without JavaScript functionality.

---

## 🎯 Key Flexbox Concepts Demonstrated

1. **Main Axis vs Cross Axis**: Understanding the two dimensions of flexbox
2. **Justify Content**: Alignment along the main axis
3. **Align Items**: Alignment along the cross axis
4. **Flex Grow**: How items expand to fill space
5. **Flex Wrap**: Multi-line flex containers
6. **Direction**: Changing layout direction and order
7. **Align Self**: Individual item alignment
8. **Order**: Visual reordering of items
9. **Align Content**: Multi-line alignment

---

## 🚀 How to Use

1. Open `index.html` in a web browser
2. Observe how different flexbox properties affect the layout
3. Resize the browser window to see responsive behavior
4. Modify the HTML classes to experiment with different combinations

---

## 💡 Learning Tips

- **Experiment**: Try combining different utility classes
- **Browser DevTools**: Use browser inspector to see applied styles
- **Resize**: Adjust window size to see wrapping behavior
- **Modify**: Change grow values and observe the differences

---

## 📖 Glossary of Terms

| Abbreviation | Full Form | Description |
|--------------|-----------|-------------|
| **HTML** | HyperText Markup Language | Standard markup language for creating web pages |
| **CSS** | Cascading Style Sheets | Style sheet language for describing presentation of HTML |
| **UTF-8** | Unicode Transformation Format - 8-bit | Character encoding for text files |
| **IE** | Internet Explorer | Microsoft's legacy web browser |
| **px** | Pixels | Absolute unit of measurement in CSS |
| **rem** | Root Em | Relative unit based on root element's font size |
| **vh** | Viewport Height | 1% of the viewport's height |
| **vw** | Viewport Width | 1% of the viewport's width |
| **DevTools** | Developer Tools | Browser's built-in inspection and debugging tools |

### Common Flexbox Terms

| Term | Description |
|------|-------------|
| **Main Axis** | Primary axis along which flex items are laid out (horizontal for row, vertical for column) |
| **Cross Axis** | Axis perpendicular to the main axis |
| **Flex Container** | Parent element with `display: flex` |
| **Flex Item** | Direct child of a flex container |
| **Justify** | Alignment along the main axis |
| **Align** | Alignment along the cross axis |
| **Gap** | Space between flex items |
| **Wrap** | Allows items to wrap to new lines |
| **Grow** | Defines ability of item to expand |
| **Shrink** | Defines ability of item to contract |
| **Basis** | Default size of an item before space distribution |

---

Happy Learning! 🎉