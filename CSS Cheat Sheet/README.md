# 🎨 CSS Cheat Sheet - Complete Guide

## 📖 What is CSS?

**CSS (Cascading Style Sheets)** is the language used to style and layout web pages. While HTML provides structure, CSS makes it beautiful!

---

## 🔗 How to Add CSS

### Inline CSS
**Definition:** CSS written directly in HTML elements using the `style` attribute.

**Explanation:** Quick for single elements but not recommended for multiple styles.

**Example:**
```html
<p style="color: blue; font-size: 18px;">This is blue text</p>
```

---

### Internal CSS
**Definition:** CSS written in the `<style>` tag inside the HTML `<head>` section.

**Explanation:** Good for single-page styling. All styles stay in one HTML file.

**Example:**
```html
<head>
  <style>
    p {
      color: blue;
      font-size: 18px;
    }
  </style>
</head>
```

---

### External CSS
**Definition:** CSS written in a separate `.css` file and linked to HTML.

**Explanation:** Best practice! Keeps styling separate and reusable across multiple pages.

**Example:**
```html
<!-- In HTML file -->
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

```css
/* In styles.css file */
p {
  color: blue;
  font-size: 18px;
}
```

---

## 🎯 CSS Selectors

### Element Selector
**Definition:** Selects all elements of a specific HTML tag.

**Explanation:** Targets every instance of that tag on the page.

**Example:**
```css
p {
  color: green;
}
/* Makes ALL paragraphs green */
```

---

### Class Selector
**Definition:** Selects elements with a specific class attribute (uses `.`).

**Explanation:** Can be applied to multiple elements. Reusable across different tags.

**Example:**
```css
.highlight {
  background-color: yellow;
}
```
```html
<p class="highlight">This paragraph is highlighted</p>
<span class="highlight">This span too!</span>
```

---

### ID Selector
**Definition:** Selects a single element with a specific ID (uses `#`).

**Explanation:** IDs must be unique on a page. Use for one specific element.

**Example:**
```css
#header {
  font-size: 24px;
  color: navy;
}
```
```html
<div id="header">Main Header</div>
```

---

### Universal Selector
**Definition:** Selects all elements on the page (uses `*`).

**Explanation:** Applies style to everything. Often used for resets.

**Example:**
```css
* {
  margin: 0;
  padding: 0;
}
/* Removes default spacing from all elements */
```

---

### Group Selector
**Definition:** Applies the same styles to multiple selectors (uses `,`).

**Explanation:** Saves time by styling multiple elements at once.

**Example:**
```css
h1, h2, h3 {
  color: darkblue;
  font-family: Arial;
}
/* All headings get the same color and font */
```

---

### Descendant Selector
**Definition:** Selects elements inside another element (uses space).

**Explanation:** Targets nested elements without affecting others.

**Example:**
```css
div p {
  color: red;
}
/* Only paragraphs INSIDE divs turn red */
```
```html
<div>
  <p>This is red</p>
</div>
<p>This stays normal</p>
```

---

### Child Selector
**Definition:** Selects direct children of an element (uses `>`).

**Explanation:** Only targets immediate children, not deeper descendants.

**Example:**
```css
ul > li {
  color: blue;
}
/* Only direct <li> children of <ul>, not nested ones */
```

---

### Pseudo-class Selector
**Definition:** Selects elements in a specific state (uses `:`).

**Explanation:** Styles elements based on user interaction or position.

**Example:**
```css
a:hover {
  color: red;
}
/* Link turns red when you hover over it */

li:first-child {
  font-weight: bold;
}
/* First list item is bold */

input:focus {
  border: 2px solid blue;
}
/* Input gets blue border when clicked */
```

---

## 🎨 Color Properties

### color
**Definition:** Sets the text color.

**Explanation:** Can use color names, hex codes, RGB, or HSL values.

**Example:**
```css
h1 {
  color: blue;
}

p {
  color: #FF5733; /* Hex code */
}

span {
  color: rgb(255, 87, 51); /* RGB */
}

div {
  color: hsl(9, 100%, 60%); /* HSL */
}
```

---

### background-color
**Definition:** Sets the background color of an element.

**Explanation:** Fills the entire element area with color.

**Example:**
```css
body {
  background-color: lightgray;
}

div {
  background-color: #f0f0f0;
}

.box {
  background-color: rgba(255, 0, 0, 0.5); /* Semi-transparent red */
}
```

---

### opacity
**Definition:** Sets the transparency level of an element.

**Explanation:** Value from 0 (invisible) to 1 (fully visible).

**Example:**
```css
.transparent {
  opacity: 0.5; /* 50% transparent */
}

.ghost {
  opacity: 0.2; /* Very transparent */
}
```

---

## 🔤 Font Properties

### font-family
**Definition:** Changes the font of text.

**Explanation:** List fonts in order of preference. Browser uses the first available one.

**Example:**
```css
p {
  font-family: Arial, Helvetica, sans-serif;
}

h1 {
  font-family: "Times New Roman", Times, serif;
}

.code {
  font-family: "Courier New", monospace;
}
```

---

### font-size
**Definition:** Sets the size of text.

**Explanation:** Can use pixels (px), ems (em), rems (rem), or percentages (%).

**Example:**
```css
h1 {
  font-size: 32px;
}

p {
  font-size: 16px;
}

small {
  font-size: 12px;
}

.responsive {
  font-size: 1.5rem; /* Relative to root */
}
```

---

### font-weight
**Definition:** Sets how thick or thin text appears.

**Explanation:** Use keywords (normal, bold) or numbers (100-900).

**Example:**
```css
p {
  font-weight: normal; /* Regular text */
}

strong {
  font-weight: bold;
}

h1 {
  font-weight: 700; /* Bold */
}

.light {
  font-weight: 300; /* Light text */
}
```

---

### font-style
**Definition:** Makes text italic or normal.

**Explanation:** Use for emphasis or stylistic choices.

**Example:**
```css
em {
  font-style: italic;
}

p {
  font-style: normal;
}

.quote {
  font-style: oblique; /* Slanted */
}
```

---

### font-variant
**Definition:** Changes text to small caps.

**Explanation:** Makes lowercase letters appear as smaller uppercase letters.

**Example:**
```css
.fancy {
  font-variant: small-caps;
}
/* "hello" becomes "ʜᴇʟʟᴏ" */
```

---

### line-height
**Definition:** Sets the space between lines of text.

**Explanation:** Improves readability. Higher values = more space.

**Example:**
```css
p {
  line-height: 1.6; /* 1.6 times the font size */
}

.tight {
  line-height: 1.2;
}

.spacious {
  line-height: 2.0;
}
```

---

## 📝 Text Properties

### text-align
**Definition:** Aligns text horizontally.

**Explanation:** Controls whether text is left, right, centered, or justified.

**Example:**
```css
h1 {
  text-align: center;
}

p {
  text-align: left; /* Default */
}

.right-text {
  text-align: right;
}

.newspaper {
  text-align: justify; /* Spreads text to fill width */
}
```

---

### text-decoration
**Definition:** Adds or removes decorations from text.

**Explanation:** Commonly used for underlines, strikethroughs, or removing link underlines.

**Example:**
```css
a {
  text-decoration: none; /* Remove underline from links */
}

.underline {
  text-decoration: underline;
}

.strike {
  text-decoration: line-through;
}

.overline {
  text-decoration: overline;
}
```

---

### text-transform
**Definition:** Changes the capitalization of text.

**Explanation:** Convert text to uppercase, lowercase, or capitalize first letters.

**Example:**
```css
.uppercase {
  text-transform: uppercase; /* "hello" → "HELLO" */
}

.lowercase {
  text-transform: lowercase; /* "HELLO" → "hello" */
}

.capitalize {
  text-transform: capitalize; /* "hello world" → "Hello World" */
}
```

---

### text-indent
**Definition:** Indents the first line of text.

**Explanation:** Creates that classic paragraph indentation.

**Example:**
```css
p {
  text-indent: 50px;
}

.essay {
  text-indent: 2em; /* 2 times the font size */
}
```

---

### letter-spacing
**Definition:** Adjusts space between characters.

**Explanation:** Positive values spread letters apart, negative values squeeze them together.

**Example:**
```css
h1 {
  letter-spacing: 3px; /* More space between letters */
}

.tight {
  letter-spacing: -1px; /* Letters closer together */
}

.spaced {
  letter-spacing: 0.1em;
}
```

---

### word-spacing
**Definition:** Adjusts space between words.

**Explanation:** Similar to letter-spacing but for whole words.

**Example:**
```css
p {
  word-spacing: 5px;
}

.wide {
  word-spacing: 10px;
}
```

---

### text-shadow
**Definition:** Adds shadow to text.

**Explanation:** Creates depth with horizontal offset, vertical offset, blur, and color.

**Example:**
```css
h1 {
  text-shadow: 2px 2px 4px gray;
  /* 2px right, 2px down, 4px blur, gray color */
}

.glowing {
  text-shadow: 0 0 10px blue;
}

.multiple {
  text-shadow: 2px 2px 4px red, -2px -2px 4px blue;
}
```

---

## 📦 Box Model Properties

### margin
**Definition:** Space **outside** the element's border.

**Explanation:** Creates space between elements. Can set all sides or individually.

**Example:**
```css
div {
  margin: 20px; /* All sides 20px */
}

p {
  margin: 10px 20px; /* Top/bottom 10px, left/right 20px */
}

.box {
  margin: 10px 15px 20px 25px; /* Top, right, bottom, left (clockwise) */
}

.centered {
  margin: 0 auto; /* Centers block element horizontally */
}
```

---

### margin-top, margin-right, margin-bottom, margin-left
**Definition:** Sets margin for individual sides.

**Explanation:** Precise control over each side's spacing.

**Example:**
```css
h1 {
  margin-top: 20px;
  margin-bottom: 15px;
}

.sidebar {
  margin-right: 50px;
  margin-left: 10px;
}
```

---

### padding
**Definition:** Space **inside** the element, between content and border.

**Explanation:** Creates breathing room for content inside the element.

**Example:**
```css
div {
  padding: 20px; /* All sides 20px */
}

button {
  padding: 10px 30px; /* Top/bottom 10px, left/right 30px */
}

.card {
  padding: 15px 20px 15px 20px; /* Top, right, bottom, left */
}
```

---

### padding-top, padding-right, padding-bottom, padding-left
**Definition:** Sets padding for individual sides.

**Explanation:** Control spacing inside element on each side independently.

**Example:**
```css
.header {
  padding-top: 30px;
  padding-bottom: 30px;
}

.content {
  padding-left: 50px;
  padding-right: 20px;
}
```

---

### border
**Definition:** Creates a border around an element.

**Explanation:** Specify width, style (solid, dashed, dotted), and color.

**Example:**
```css
div {
  border: 2px solid black;
  /* 2px width, solid style, black color */
}

.dashed {
  border: 3px dashed red;
}

.box {
  border: 1px solid #ccc;
}
```

---

### border-width
**Definition:** Sets the thickness of the border.

**Explanation:** Can set all sides or individually.

**Example:**
```css
div {
  border-width: 5px;
}

.varied {
  border-width: 2px 4px 2px 4px; /* Top, right, bottom, left */
}
```

---

### border-style
**Definition:** Sets the style of the border.

**Explanation:** Options: solid, dashed, dotted, double, groove, ridge, inset, outset, none.

**Example:**
```css
.solid {
  border-style: solid;
}

.dashed {
  border-style: dashed;
}

.dotted {
  border-style: dotted;
}

.double {
  border-style: double;
}
```

---

### border-color
**Definition:** Sets the color of the border.

**Explanation:** Can use any color format (name, hex, RGB, etc.).

**Example:**
```css
div {
  border-color: blue;
}

.multicolor {
  border-color: red green blue yellow; /* Top, right, bottom, left */
}
```

---

### border-radius
**Definition:** Rounds the corners of an element.

**Explanation:** Creates rounded corners. Higher values = more rounded.

**Example:**
```css
.rounded {
  border-radius: 10px;
}

.circle {
  border-radius: 50%; /* Makes square into circle */
}

.custom {
  border-radius: 10px 20px 30px 40px; /* Top-left, top-right, bottom-right, bottom-left */
}
```

---

### width
**Definition:** Sets the width of an element.

**Explanation:** Can use pixels, percentages, or other units.

**Example:**
```css
div {
  width: 500px;
}

.half {
  width: 50%; /* 50% of parent element */
}

.full {
  width: 100%;
}
```

---

### height
**Definition:** Sets the height of an element.

**Explanation:** Controls vertical size of element.

**Example:**
```css
div {
  height: 300px;
}

.tall {
  height: 80vh; /* 80% of viewport height */
}

.auto {
  height: auto; /* Height based on content */
}
```

---

### max-width / min-width
**Definition:** Sets maximum or minimum width limits.

**Explanation:** Prevents elements from getting too wide or too narrow.

**Example:**
```css
.container {
  max-width: 1200px; /* Won't exceed 1200px */
  min-width: 300px; /* Won't shrink below 300px */
}
```

---

### max-height / min-height
**Definition:** Sets maximum or minimum height limits.

**Explanation:** Controls height boundaries for responsive design.

**Example:**
```css
.box {
  max-height: 500px;
  min-height: 200px;
}
```

---

### box-sizing
**Definition:** Changes how width and height are calculated.

**Explanation:** `border-box` includes padding and border in width/height. `content-box` (default) doesn't.

**Example:**
```css
* {
  box-sizing: border-box; /* Most common approach */
}
/* Now padding and border don't add to total width */
```

---

## 🖼️ Background Properties

### background-color
**Definition:** Sets the background color.

**Explanation:** Fills element background with solid color.

**Example:**
```css
body {
  background-color: lightblue;
}

div {
  background-color: #f0f0f0;
}
```

---

### background-image
**Definition:** Sets an image as the background.

**Explanation:** Use `url()` to specify image path.

**Example:**
```css
body {
  background-image: url('background.jpg');
}

.hero {
  background-image: url('hero-banner.png');
}
```

---

### background-repeat
**Definition:** Controls if/how background image repeats.

**Explanation:** Options: repeat, repeat-x, repeat-y, no-repeat.

**Example:**
```css
body {
  background-image: url('pattern.png');
  background-repeat: repeat; /* Tiles in all directions */
}

.header {
  background-image: url('banner.jpg');
  background-repeat: no-repeat; /* Shows once */
}

.horizontal {
  background-repeat: repeat-x; /* Repeats horizontally only */
}
```

---

### background-position
**Definition:** Sets starting position of background image.

**Explanation:** Use keywords (top, bottom, left, right, center) or values.

**Example:**
```css
div {
  background-position: center;
}

.hero {
  background-position: top right;
}

.custom {
  background-position: 50% 50%; /* Center horizontally and vertically */
}
```

---

### background-size
**Definition:** Sets the size of background image.

**Explanation:** Options: auto, cover (fills entire area), contain (fits inside), or specific sizes.

**Example:**
```css
.hero {
  background-size: cover; /* Covers entire element */
}

.logo {
  background-size: contain; /* Fits inside without cropping */
}

.custom {
  background-size: 100px 200px; /* Specific width and height */
}
```

---

### background-attachment
**Definition:** Sets whether background scrolls with content or stays fixed.

**Explanation:** `fixed` creates parallax effect, `scroll` moves with content.

**Example:**
```css
body {
  background-attachment: fixed; /* Background stays in place while scrolling */
}

.parallax {
  background-image: url('mountain.jpg');
  background-attachment: fixed;
  background-size: cover;
}
```

---

### background (Shorthand)
**Definition:** Combines all background properties in one line.

**Explanation:** Order: color, image, repeat, position, size, attachment.

**Example:**
```css
body {
  background: lightblue url('bg.jpg') no-repeat center/cover fixed;
}

div {
  background: #f0f0f0 url('pattern.png') repeat;
}
```

---

## 📐 Display & Positioning

### display
**Definition:** Defines how an element is displayed.

**Explanation:** Common values: block, inline, inline-block, flex, grid, none.

**Example:**
```css
.block {
  display: block; /* Takes full width, starts new line */
}

.inline {
  display: inline; /* Flows with text, no line breaks */
}

.inline-block {
  display: inline-block; /* Inline but can set width/height */
}

.hide {
  display: none; /* Element disappears completely */
}

.flex-container {
  display: flex; /* Enables flexbox layout */
}
```

---

### position
**Definition:** Specifies how an element is positioned.

**Explanation:** Values: static (default), relative, absolute, fixed, sticky.

**Example:**
```css
.relative {
  position: relative;
  top: 10px; /* Moves 10px down from normal position */
  left: 20px; /* Moves 20px right from normal position */
}

.absolute {
  position: absolute;
  top: 0;
  right: 0; /* Positioned relative to parent */
}

.fixed {
  position: fixed;
  bottom: 20px;
  right: 20px; /* Stays in place when scrolling */
}

.sticky {
  position: sticky;
  top: 0; /* Sticks to top when scrolling past it */
}
```

---

### top, right, bottom, left
**Definition:** Position values used with positioned elements.

**Explanation:** Only work when `position` is not `static`.

**Example:**
```css
.corner {
  position: absolute;
  top: 10px;
  right: 10px;
}

.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

---

### z-index
**Definition:** Controls stacking order of overlapping elements.

**Explanation:** Higher numbers appear on top. Only works on positioned elements.

**Example:**
```css
.background {
  position: relative;
  z-index: 1;
}

.foreground {
  position: relative;
  z-index: 10; /* Appears above .background */
}

.modal {
  position: fixed;
  z-index: 9999; /* Appears on top of everything */
}
```

---

### float
**Definition:** Floats element to left or right, allowing text to wrap around it.

**Explanation:** Commonly used for images in text. Modern layouts use flexbox/grid instead.

**Example:**
```css
.image-left {
  float: left;
  margin-right: 20px;
}

.image-right {
  float: right;
  margin-left: 20px;
}
```

---

### clear
**Definition:** Prevents elements from wrapping around floated elements.

**Explanation:** Use to control float behavior.

**Example:**
```css
.clear {
  clear: both; /* No floats on either side */
}

.clear-left {
  clear: left; /* No floats on left side */
}

.clear-right {
  clear: right; /* No floats on right side */
}
```

---

### overflow
**Definition:** Controls what happens to content that overflows its container.

**Explanation:** Options: visible, hidden, scroll, auto.

**Example:**
```css
.container {
  overflow: hidden; /* Hides overflow content */
}

.scrollable {
  overflow: scroll; /* Always shows scrollbars */
}

.auto {
  overflow: auto; /* Scrollbars appear only when needed */
}

.horizontal {
  overflow-x: scroll; /* Horizontal scrollbar only */
}
```

---

### visibility
**Definition:** Controls whether element is visible or hidden.

**Explanation:** Unlike `display: none`, element still takes up space.

**Example:**
```css
.hidden {
  visibility: hidden; /* Hidden but space remains */
}

.visible {
  visibility: visible;
}
```

---

## 🎯 Flexbox Properties

### display: flex
**Definition:** Turns element into a flex container.

**Explanation:** Children become flex items that can be easily aligned and distributed.

**Example:**
```css
.container {
  display: flex;
}
```

---

### flex-direction
**Definition:** Sets the direction of flex items.

**Explanation:** Options: row (default), row-reverse, column, column-reverse.

**Example:**
```css
.row {
  display: flex;
  flex-direction: row; /* Left to right */
}

.column {
  display: flex;
  flex-direction: column; /* Top to bottom */
}

.reverse {
  display: flex;
  flex-direction: row-reverse; /* Right to left */
}
```

---

### justify-content
**Definition:** Aligns flex items along main axis (horizontally by default).

**Explanation:** Options: flex-start, flex-end, center, space-between, space-around, space-evenly.

**Example:**
```css
.center {
  display: flex;
  justify-content: center; /* Centers items horizontally */
}

.space-between {
  display: flex;
  justify-content: space-between; /* Space between items */
}

.end {
  display: flex;
  justify-content: flex-end; /* Pushes to right */
}
```

---

### align-items
**Definition:** Aligns flex items along cross axis (vertically by default).

**Explanation:** Options: flex-start, flex-end, center, stretch, baseline.

**Example:**
```css
.center {
  display: flex;
  align-items: center; /* Centers items vertically */
}

.stretch {
  display: flex;
  align-items: stretch; /* Stretches items to fill container */
}

.start {
  display: flex;
  align-items: flex-start; /* Aligns to top */
}
```

---

### flex-wrap
**Definition:** Controls whether flex items wrap to new lines.

**Explanation:** Options: nowrap (default), wrap, wrap-reverse.

**Example:**
```css
.wrap {
  display: flex;
  flex-wrap: wrap; /* Items wrap to next line */
}

.nowrap {
  display: flex;
  flex-wrap: nowrap; /* Items stay on one line */
}
```

---

### gap
**Definition:** Sets spacing between flex items.

**Explanation:** Modern way to add space without margins.

**Example:**
```css
.container {
  display: flex;
  gap: 20px; /* 20px space between items */
}

.custom-gap {
  display: flex;
  gap: 10px 20px; /* 10px vertical, 20px horizontal */
}
```

---

### flex-grow
**Definition:** Defines ability of flex item to grow.

**Explanation:** Number representing growth factor relative to other items.

**Example:**
```css
.item-1 {
  flex-grow: 1; /* Takes 1 part of available space */
}

.item-2 {
  flex-grow: 2; /* Takes 2 parts (twice as much as item-1) */
}
```

---

### flex-shrink
**Definition:** Defines ability of flex item to shrink.

**Explanation:** Number representing shrink factor when space is limited.

**Example:**
```css
.keep-size {
  flex-shrink: 0; /* Won't shrink */
}

.shrinkable {
  flex-shrink: 1; /* Can shrink */
}
```

---

## 🎲 Grid Properties

### display: grid
**Definition:** Turns element into a grid container.

**Explanation:** Creates two-dimensional layout system for rows and columns.

**Example:**
```css
.container {
  display: grid;
}
```

---

### grid-template-columns
**Definition:** Defines the columns of the grid.

**Explanation:** Specify width of each column.

**Example:**
```css
.three-columns {
  display: grid;
  grid-template-columns: 200px 200px 200px;
  /* Three columns, each 200px */
}

.equal-columns {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  /* Three equal-width columns */
}

.mixed {
  display: grid;
  grid-template-columns: 200px 1fr 2fr;
  /* Fixed, flexible, double flexible */
}

.repeat {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  /* Four equal columns */
}
```

---

### grid-template-rows
**Definition:** Defines the rows of the grid.

**Explanation:** Specify height of each row.

**Example:**
```css
.rows {
  display: grid;
  grid-template-rows: 100px 200px 100px;
}

.equal-rows {
  display: grid;
  grid-template-rows: repeat(3, 150px);
}
```

---

### grid-gap / gap
**Definition:** Sets spacing between grid items.

**Explanation:** Creates gutters between rows and columns.

**Example:**
```css
.container {
  display: grid;
  gap: 20px; /* 20px between all items */
}

.custom-gap {
  display: grid;
  gap: 20px 40px; /* 20px row gap, 40px column gap */
}
```

---

### grid-column
**Definition:** Specifies which columns a grid item should span.

**Explanation:** Use with grid items, not container.

**Example:**
```css
.item {
  grid-column: 1 / 3; /* Spans from column line 1 to 3 */
}

.full-width {
  grid-column: 1 / -1; /* Spans all columns */
}

.span-two {
  grid-column: span 2; /* Spans 2 columns */
}
```

---

### grid-row
**Definition:** Specifies which rows a grid item should span.

**Explanation:** Similar to grid-column but for rows.

**Example:**
```css
.item {
  grid-row: 1 / 3; /* Spans from row line 1 to 3 */
}

.tall {
  grid-row: span 2; /* Spans 2 rows */
}
```

---

## 🎭 Transform & Animation

### transform
**Definition:** Applies 2D or 3D transformations to elements.

**Explanation:** Rotate, scale, move, or skew elements.

**Example:**
```css
.rotate {
  transform: rotate(45deg); /* Rotates 45 degrees */
}

.scale {
  transform: scale(1.5); /* Makes 1.5x larger */
}

.move {
  transform: translate(50px, 100px); /* Moves right 50px, down 100px */
}

.combined {
  transform: rotate(45deg) scale(1.2) translate(20px, 20px);
}
```

---

### transition
**Definition:** Creates smooth transitions between property changes.

**Explanation:** Specify property, duration, timing function, and delay.

**Example:**
```css
.smooth {
  transition: all 0.3s ease;
  /* All properties transition smoothly in 0.3 seconds */
}

button {
  background-color: blue;
  transition: background-color 0.5s;
}

button:hover {
  background-color: red;
  /* Color changes smoothly on hover */
}

.custom {
  transition: width 2s, height 1s, transform 0.5s;
}
```

---

### animation
**Definition:** Creates animations using keyframes.

**Explanation:** Define animation with @keyframes, then apply it.

**Example:**
```css
@keyframes slideIn {
  from {
    transform: translateX(-100%);
  }
  to {
    transform: translateX(0);
  }
}

.animated {
  animation: slideIn 1s ease-in-out;
}

.bouncing {
  animation: bounce 2s infinite;
  /* Repeats forever */
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  50% {
    opacity: 0.5;
  }
  100% {
    opacity: 1;
  }
}
```

---

### @keyframes
**Definition:** Defines the animation sequence.

**Explanation:** Specify styles at different points in the animation (0% to 100% or from/to).

**Example:**
```css
@keyframes colorChange {
  0% {
    background-color: red;
  }
  50% {
    background-color: yellow;
  }
  100% {
    background-color: green;
  }
}

.box {
  animation: colorChange 3s infinite;
}
```

---

### animation-duration
**Definition:** Sets how long animation takes to complete.

**Explanation:** Specified in seconds (s) or milliseconds (ms).

**Example:**
```css
.fast {
  animation: slideIn 0.5s; /* Half a second */
}

.slow {
  animation: slideIn 3s; /* 3 seconds */
}
```

---

### animation-delay
**Definition:** Delays the start of an animation.

**Explanation:** Time to wait before animation begins.

**Example:**
```css
.delayed {
  animation: fadeIn 1s;
  animation-delay: 2s; /* Waits 2 seconds before starting */
}
```

---

### animation-iteration-count
**Definition:** Sets how many times animation repeats.

**Explanation:** Use number or `infinite` for continuous loop.

**Example:**
```css
.once {
  animation: bounce 1s;
  animation-iteration-count: 1; /* Plays once */
}

.forever {
  animation: spin 2s;
  animation-iteration-count: infinite; /* Never stops */
}

.three-times {
  animation: pulse 1s;
  animation-iteration-count: 3;
}
```

---

### animation-direction
**Definition:** Sets direction of animation playback.

**Explanation:** Options: normal, reverse, alternate, alternate-reverse.

**Example:**
```css
.normal {
  animation: slideIn 2s normal; /* Forward */
}

.reverse {
  animation: slideIn 2s reverse; /* Backward */
}

.alternate {
  animation: bounce 1s infinite alternate;
  /* Goes forward, then backward, repeating */
}
```

---

## 🎨 Shadow Effects

### box-shadow
**Definition:** Adds shadow around element's box.

**Explanation:** Values: horizontal offset, vertical offset, blur radius, spread radius, color.

**Example:**
```css
.card {
  box-shadow: 5px 5px 10px gray;
  /* 5px right, 5px down, 10px blur, gray color */
}

.elevated {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  /* Subtle elevation effect */
}

.glowing {
  box-shadow: 0 0 20px blue;
  /* Glow effect */
}

.multiple {
  box-shadow: 
    0 2px 4px rgba(0,0,0,0.1),
    0 8px 16px rgba(0,0,0,0.1);
  /* Multiple shadows for depth */
}

.inset {
  box-shadow: inset 0 0 10px gray;
  /* Shadow inside the element */
}
```

---

### text-shadow
**Definition:** Adds shadow to text.

**Explanation:** Values: horizontal offset, vertical offset, blur radius, color.

**Example:**
```css
h1 {
  text-shadow: 2px 2px 4px black;
}

.glowing-text {
  text-shadow: 0 0 10px yellow;
}

.embossed {
  text-shadow: 1px 1px 2px white, -1px -1px 2px black;
}
```

---

## 🎯 List Properties

### list-style-type
**Definition:** Sets the marker type for list items.

**Explanation:** Options for `<ul>`: disc, circle, square, none. For `<ol>`: decimal, upper-alpha, lower-roman, etc.

**Example:**
```css
ul {
  list-style-type: square; /* Square bullets */
}

.no-bullets {
  list-style-type: none; /* No markers */
}

ol {
  list-style-type: upper-roman; /* I, II, III, IV */
}

.letters {
  list-style-type: upper-alpha; /* A, B, C, D */
}
```

---

### list-style-image
**Definition:** Uses an image as the list marker.

**Explanation:** Replaces default bullet with custom image.

**Example:**
```css
ul {
  list-style-image: url('checkmark.png');
}

.custom-bullets {
  list-style-image: url('arrow.svg');
}
```

---

### list-style-position
**Definition:** Sets position of list markers.

**Explanation:** Options: inside (marker inside text block) or outside (default, marker outside).

**Example:**
```css
ul {
  list-style-position: inside;
  /* Text wraps under marker */
}

.outside {
  list-style-position: outside;
  /* Marker hangs outside text */
}
```

---

### list-style (Shorthand)
**Definition:** Combines all list-style properties.

**Explanation:** Sets type, position, and image in one line.

**Example:**
```css
ul {
  list-style: square inside;
}

.custom {
  list-style: url('icon.png') inside;
}
```

---

## 📱 Responsive Design

### media queries
**Definition:** Applies styles based on device characteristics.

**Explanation:** Use to create responsive designs that adapt to different screen sizes.

**Example:**
```css
/* Default styles for all devices */
.container {
  width: 100%;
}

/* Tablets (768px and up) */
@media (min-width: 768px) {
  .container {
    width: 750px;
  }
}

/* Desktops (1024px and up) */
@media (min-width: 1024px) {
  .container {
    width: 1000px;
  }
}

/* Large screens (1200px and up) */
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}

/* Print styles */
@media print {
  .no-print {
    display: none;
  }
}

/* Dark mode */
@media (prefers-color-scheme: dark) {
  body {
    background-color: black;
    color: white;
  }
}
```

---

### Viewport Units
**Definition:** Units relative to viewport size.

**Explanation:** vw (viewport width), vh (viewport height), vmin, vmax.

**Example:**
```css
.full-screen {
  width: 100vw; /* 100% of viewport width */
  height: 100vh; /* 100% of viewport height */
}

.hero {
  height: 50vh; /* Half of viewport height */
}

.responsive-font {
  font-size: 5vw; /* 5% of viewport width */
}
```

---

## 🎨 Gradient Properties

### linear-gradient()
**Definition:** Creates a linear gradient background.

**Explanation:** Smooth transition between colors in a straight line.

**Example:**
```css
.gradient {
  background: linear-gradient(red, blue);
  /* Top to bottom gradient */
}

.horizontal {
  background: linear-gradient(to right, red, blue);
  /* Left to right */
}

.diagonal {
  background: linear-gradient(45deg, red, blue);
  /* Diagonal gradient */
}

.multi-color {
  background: linear-gradient(red, yellow, green, blue);
  /* Multiple colors */
}

.with-stops {
  background: linear-gradient(red 0%, yellow 50%, green 100%);
  /* Control color positions */
}
```

---

### radial-gradient()
**Definition:** Creates a circular gradient background.

**Explanation:** Gradient radiates from a center point.

**Example:**
```css
.radial {
  background: radial-gradient(red, blue);
  /* Center to edges */
}

.circle {
  background: radial-gradient(circle, red, blue);
  /* Perfect circle */
}

.positioned {
  background: radial-gradient(at top left, red, blue);
  /* Starts from top left */
}
```

---

## 🎭 Filter Properties

### filter
**Definition:** Applies visual effects like blur, brightness, contrast, etc.

**Explanation:** Can be combined for multiple effects.

**Example:**
```css
.blur {
  filter: blur(5px);
}

.grayscale {
  filter: grayscale(100%);
  /* Removes all color */
}

.brightness {
  filter: brightness(150%);
  /* Makes 50% brighter */
}

.contrast {
  filter: contrast(200%);
}

.sepia {
  filter: sepia(100%);
  /* Old photo effect */
}

.combined {
  filter: blur(3px) brightness(120%) contrast(110%);
  /* Multiple effects */
}

img:hover {
  filter: brightness(80%);
  /* Darken on hover */
}
```

---

## 🔤 Advanced Typography

### @font-face
**Definition:** Allows custom fonts to be loaded.

**Explanation:** Use fonts not installed on user's device.

**Example:**
```css
@font-face {
  font-family: 'CustomFont';
  src: url('customfont.woff2') format('woff2'),
       url('customfont.woff') format('woff');
}

body {
  font-family: 'CustomFont', Arial, sans-serif;
}
```

---

### text-overflow
**Definition:** Specifies how overflowing text should be displayed.

**Explanation:** Usually used with `overflow: hidden` and `white-space: nowrap`.

**Example:**
```css
.truncate {
  width: 200px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Shows "Text goes he..." */
}
```

---

### white-space
**Definition:** Controls how whitespace is handled.

**Explanation:** Options: normal, nowrap, pre, pre-wrap, pre-line.

**Example:**
```css
.no-wrap {
  white-space: nowrap;
  /* Text stays on one line */
}

.preserve {
  white-space: pre;
  /* Preserves all spaces and line breaks */
}

.wrap {
  white-space: pre-wrap;
  /* Preserves whitespace but wraps lines */
}
```

---

### word-break
**Definition:** Specifies how words should break at line end.

**Explanation:** Useful for long words or URLs.

**Example:**
```css
.break-all {
  word-break: break-all;
  /* Breaks anywhere */
}

.keep-words {
  word-break: keep-all;
  /* No breaks within words */
}

.break-word {
  word-break: break-word;
  /* Breaks long words to prevent overflow */
}
```

---

## 🎯 Cursor Properties

### cursor
**Definition:** Changes the mouse cursor appearance.

**Explanation:** Many built-in cursor types available.

**Example:**
```css
.pointer {
  cursor: pointer;
  /* Hand cursor (for links/buttons) */
}

.text {
  cursor: text;
  /* I-beam cursor (for text) */
}

.move {
  cursor: move;
  /* Move cursor (for draggable items) */
}

.not-allowed {
  cursor: not-allowed;
  /* Forbidden cursor */
}

.help {
  cursor: help;
  /* Question mark cursor */
}

.custom {
  cursor: url('custom-cursor.png'), auto;
  /* Custom cursor image */
}
```

---

## 🎨 Opacity & Blend Modes

### opacity
**Definition:** Sets transparency of entire element.

**Explanation:** Value from 0 (invisible) to 1 (fully visible). Affects entire element including children.

**Example:**
```css
.transparent {
  opacity: 0.5;
  /* 50% transparent */
}

.fade {
  opacity: 0;
  transition: opacity 0.3s;
}

.fade:hover {
  opacity: 1;
  /* Fades in on hover */
}
```

---

### mix-blend-mode
**Definition:** Blends element with background.

**Explanation:** Creates Photoshop-like blend effects.

**Example:**
```css
.multiply {
  mix-blend-mode: multiply;
  /* Darkens overlapping areas */
}

.screen {
  mix-blend-mode: screen;
  /* Lightens overlapping areas */
}

.overlay {
  mix-blend-mode: overlay;
  /* Combines multiply and screen */
}
```

---

## 📐 Object Properties

### object-fit
**Definition:** Specifies how image/video should be resized to fit container.

**Explanation:** Options: fill, contain, cover, none, scale-down.

**Example:**
```css
img {
  width: 300px;
  height: 200px;
  object-fit: cover;
  /* Covers area, may crop */
}

.contain {
  object-fit: contain;
  /* Fits inside, maintains aspect ratio */
}

.fill {
  object-fit: fill;
  /* Stretches to fill, may distort */
}
```

---

### object-position
**Definition:** Specifies position of image/video within container.

**Explanation:** Works with object-fit. Use keywords or percentages.

**Example:**
```css
img {
  object-fit: cover;
  object-position: top; /* Shows top of image */
}

.centered {
  object-position: center;
}

.custom {
  object-position: 25% 75%;
}
```

---

## 🎯 Pseudo-classes (Advanced)

### :hover
**Definition:** Styles element when mouse hovers over it.

**Example:**
```css
button:hover {
  background-color: lightblue;
  transform: scale(1.05);
}
```

---

### :active
**Definition:** Styles element while being clicked.

**Example:**
```css
button:active {
  transform: scale(0.95);
  /* Shrinks when clicked */
}
```

---

### :focus
**Definition:** Styles element when it has keyboard focus.

**Example:**
```css
input:focus {
  border: 2px solid blue;
  outline: none;
}
```

---

### :first-child / :last-child
**Definition:** Selects first or last child element.

**Example:**
```css
li:first-child {
  font-weight: bold;
  /* First list item is bold */
}

p:last-child {
  margin-bottom: 0;
  /* No margin on last paragraph */
}
```

---

### :nth-child()
**Definition:** Selects elements based on position.

**Example:**
```css
li:nth-child(2) {
  color: red;
  /* Second item */
}

tr:nth-child(odd) {
  background-color: #f0f0f0;
  /* Odd rows (zebra striping) */
}

tr:nth-child(even) {
  background-color: white;
  /* Even rows */
}

div:nth-child(3n) {
  color: blue;
  /* Every 3rd element */
}
```

---

### :not()
**Definition:** Selects elements that don't match a selector.

**Example:**
```css
p:not(.special) {
  color: gray;
  /* All paragraphs except those with class "special" */
}

input:not([type="submit"]) {
  border: 1px solid gray;
  /* All inputs except submit buttons */
}
```

---

### :checked
**Definition:** Styles checked checkboxes or radio buttons.

**Example:**
```css
input[type="checkbox"]:checked {
  background-color: green;
}

input[type="radio"]:checked + label {
  font-weight: bold;
  /* Styles label of checked radio */
}
```

---

### :disabled / :enabled
**Definition:** Styles disabled or enabled form elements.

**Example:**
```css
input:disabled {
  background-color: #e0e0e0;
  cursor: not-allowed;
}

button:enabled:hover {
  background-color: blue;
}
```

---

## 🎭 Pseudo-elements

### ::before
**Definition:** Inserts content before element's content.

**Explanation:** Must include `content` property. Good for decorative elements.

**Example:**
```css
.quote::before {
  content: '"';
  font-size: 2em;
  color: gray;
}

.icon::before {
  content: '★ ';
  color: gold;
}
```

---

### ::after
**Definition:** Inserts content after element's content.

**Example:**
```css
.link::after {
  content: ' →';
}

.clearfix::after {
  content: '';
  display: table;
  clear: both;
  /* Classic clearfix technique */
}
```

---

### ::first-letter
**Definition:** Styles the first letter of text.

**Example:**
```css
p::first-letter {
  font-size: 2em;
  font-weight: bold;
  float: left;
  margin-right: 5px;
  /* Drop cap effect */
}
```

---

### ::first-line
**Definition:** Styles the first line of text.

**Example:**
```css
p::first-line {
  font-weight: bold;
  color: darkblue;
}
```

---

### ::selection
**Definition:** Styles text when selected/highlighted by user.

**Example:**
```css
::selection {
  background-color: yellow;
  color: black;
}

p::selection {
  background-color: lightblue;
}
```

---

## 📊 Table Properties

### border-collapse
**Definition:** Controls whether table borders are collapsed or separated.

**Example:**
```css
table {
  border-collapse: collapse;
  /* Single border between cells */
}

.separated {
  border-collapse: separate;
  /* Separate borders with spacing */
}
```

---

### border-spacing
**Definition:** Sets spacing between table cells (only with `border-collapse: separate`).

**Example:**
```css
table {
  border-collapse: separate;
  border-spacing: 10px;
  /* 10px gap between cells */
}

.custom {
  border-spacing: 5px 10px;
  /* 5px horizontal, 10px vertical */
}
```

---

### caption-side
**Definition:** Positions table caption.

**Example:**
```css
table {
  caption-side: top; /* Default */
}

.bottom-caption {
  caption-side: bottom;
}
```

---

## 🎯 CSS Variables (Custom Properties)

### Defining Variables
**Definition:** Create reusable values with `--variable-name`.

**Explanation:** Usually defined in `:root` for global use.

**Example:**
```css
:root {
  --primary-color: #3498db;
  --secondary-color: #2ecc71;
  --spacing: 20px;
  --border-radius: 8px;
}

.button {
  background-color: var(--primary-color);
  padding: var(--spacing);
  border-radius: var(--border-radius);
}

.card {
  border: 2px solid var(--primary-color);
  margin: var(--spacing);
}
```

---

### Using Variables
**Definition:** Access variables with `var()` function.

**Example:**
```css
:root {
  --main-bg: #f0f0f0;
  --text-color: #333;
}

body {
  background-color: var(--main-bg);
  color: var(--text-color);
}

/* With fallback value */
.box {
  color: var(--text-color, black);
  /* Uses black if --text-color undefined */
}
```

---

## 🎨 Advanced Selectors

### Attribute Selectors
**Definition:** Selects elements based on attributes.

**Example:**
```css
/* Has attribute */
a[target] {
  color: blue;
}

/* Exact value */
input[type="text"] {
  border: 1px solid gray;
}

/* Contains word */
a[href*="example"] {
  color: green;
  /* Links containing "example" */
}

/* Starts with */
a[href^="https"] {
  color: green;
  /* Secure links */
}

/* Ends with */
a[href$=".pdf"] {
  color: red;
  /* PDF links */
}
```

---

### Combinator Selectors
**Definition:** Combines multiple selectors.

**Example:**
```css
/* Descendant (space) */
div p {
  color: blue;
  /* All p inside div */
}

/* Child (>) */
div > p {
  color: red;
  /* Direct children only */
}

/* Adjacent sibling (+) */
h2 + p {
  margin-top: 0;
  /* p immediately after h2 */
}

/* General sibling (~) */
h2 ~ p {
  color: gray;
  /* All p siblings after h2 */
}
```

---

## 💡 Best Practices & Tips

### 1. Use Meaningful Class Names
```css
/* Good */
.header-navigation { }
.button-primary { }
.card-container { }

/* Avoid */
.blue { }
.big { }
.div1 { }
```

---

### 2. Keep Specificity Low
```css
/* Good - low specificity */
.button { }

/* Avoid - high specificity */
body div.container ul li.item a.link { }
```

---

### 3. Use Shorthand Properties
```css
/* Instead of this: */
margin-top: 10px;
margin-right: 20px;
margin-bottom: 10px;
margin-left: 20px;

/* Use this: */
margin: 10px 20px;
```

---

### 4. Mobile-First Approach
```css
/* Base styles for mobile */
.container {
  width: 100%;
  padding: 10px;
}

/* Then add complexity for larger screens */
@media (min-width: 768px) {
  .container {
    width: 750px;
    padding: 20px;
  }
}
```

---

### 5. Use CSS Variables for Themes
```css
:root {
  --primary: #007bff;
  --success: #28a745;
  --danger: #dc3545;
}

/* Easy to change entire theme */
[data-theme="dark"] {
  --primary: #0056b3;
  --success: #1e7e34;
  --danger: #bd2130;
}
```

---

## 🎯 Complete Example

Here's a complete example combining multiple CSS concepts:

```css
/* CSS Variables */
:root {
  --primary-color: #3498db;
  --text-color: #333;
  --spacing: 20px;
  --border-radius: 8px;
}

/* Global Styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  color: var(--text-color);
}

/* Container */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: var(--spacing);
}

/* Card Component */
.card {
  background: white;
  border-radius: var(--border-radius);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: var(--spacing);
  transition: transform 0.3s, box-shadow 0.3s;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

/* Button */
.button {
  background-color: var(--primary-color);
  color: white;
  padding: 12px 24px;
  border: none;
  border-radius: var(--border-radius);
  cursor: pointer;
  transition: background-color 0.3s;
}

.button:hover {
  background-color: #2980b9;
}

/* Responsive Grid */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: var(--spacing);
}

/* Media Query */
@media (max-width: 768px) {
  .container {
    padding: 10px;
  }
  
  .grid {
    grid-template-columns: 1fr;
  }
}
```

---

## 📚 Resources & Next Steps

- **Practice:** Build real projects to solidify concepts
- **Experiment:** Use browser DevTools to test CSS live
- **Learn Flexbox:** Master modern layout techniques
- **Learn Grid:** Understand powerful 2D layouts
- **Study Animations:** Create engaging user experiences
- **Responsive Design:** Make sites work on all devices

---

## 🎪 Advanced Layout Properties

### align-self
**Definition:** Overrides align-items for individual flex/grid items.

**Explanation:** Controls alignment of a single item independently.

**Example:**
```css
.container {
  display: flex;
  align-items: flex-start;
}

.special-item {
  align-self: center; /* This item centers vertically */
}

.stretch-item {
  align-self: stretch; /* This item stretches */
}
```

---

### justify-self
**Definition:** Aligns individual grid item along inline axis.

**Explanation:** Only works in CSS Grid, not Flexbox.

**Example:**
```css
.grid {
  display: grid;
}

.item {
  justify-self: center; /* Centers this grid item horizontally */
}

.end-item {
  justify-self: end; /* Pushes to the end */
}
```

---

### place-items
**Definition:** Shorthand for align-items and justify-items.

**Explanation:** Centers items in both directions at once.

**Example:**
```css
.grid {
  display: grid;
  place-items: center; /* Centers all items */
}

.custom {
  place-items: start end; /* align-items: start, justify-items: end */
}
```

---

### place-content
**Definition:** Shorthand for align-content and justify-content.

**Explanation:** Controls alignment of entire grid/flex container.

**Example:**
```css
.container {
  display: grid;
  place-content: center; /* Centers the entire grid */
}
```

---

### order
**Definition:** Changes the visual order of flex/grid items.

**Explanation:** Default is 0. Lower numbers appear first.

**Example:**
```css
.first {
  order: -1; /* Appears first */
}

.last {
  order: 999; /* Appears last */
}

.second {
  order: 2;
}
```

---

### flex
**Definition:** Shorthand for flex-grow, flex-shrink, and flex-basis.

**Explanation:** Controls how flex items grow, shrink, and their base size.

**Example:**
```css
.item {
  flex: 1; /* flex-grow: 1, flex-shrink: 1, flex-basis: 0% */
}

.fixed {
  flex: 0 0 200px; /* Don't grow/shrink, 200px wide */
}

.grow-only {
  flex: 1 0 auto; /* Grows but doesn't shrink */
}
```

---

### flex-basis
**Definition:** Sets initial size of flex item before space distribution.

**Explanation:** Like width/height but for flex items.

**Example:**
```css
.item {
  flex-basis: 200px; /* Starts at 200px */
}

.auto {
  flex-basis: auto; /* Based on content */
}

.percentage {
  flex-basis: 33.33%; /* One-third of container */
}
```

---

### align-content
**Definition:** Aligns flex/grid lines when there's extra space.

**Explanation:** Only works with multiple lines (flex-wrap: wrap or multiple grid rows).

**Example:**
```css
.container {
  display: flex;
  flex-wrap: wrap;
  height: 400px;
  align-content: space-between; /* Distributes rows */
}

.centered {
  align-content: center;
}
```

---

### grid-auto-flow
**Definition:** Controls how auto-placed grid items are inserted.

**Explanation:** Options: row (default), column, dense.

**Example:**
```css
.grid {
  display: grid;
  grid-auto-flow: column; /* Items flow in columns */
}

.dense {
  grid-auto-flow: dense; /* Fills gaps tightly */
}

.row-dense {
  grid-auto-flow: row dense;
}
```

---

### grid-auto-columns / grid-auto-rows
**Definition:** Sets size of implicitly created grid tracks.

**Explanation:** Controls size of auto-generated columns/rows.

**Example:**
```css
.grid {
  display: grid;
  grid-auto-columns: 200px; /* Auto columns are 200px */
  grid-auto-rows: 100px; /* Auto rows are 100px */
}

.flexible {
  grid-auto-rows: minmax(100px, auto);
}
```

---

### grid-area
**Definition:** Shorthand for grid position (row-start, column-start, row-end, column-end).

**Explanation:** Can also reference named grid areas.

**Example:**
```css
.item {
  grid-area: 1 / 2 / 3 / 4;
  /* row-start / column-start / row-end / column-end */
}

/* With named areas */
.container {
  grid-template-areas: 
    "header header header"
    "sidebar content content"
    "footer footer footer";
}

.header {
  grid-area: header;
}
```

---

## 🎨 Color Functions

### rgb() / rgba()
**Definition:** Defines colors using Red, Green, Blue (and Alpha for transparency).

**Explanation:** Values 0-255 for RGB, 0-1 for alpha.

**Example:**
```css
.red {
  color: rgb(255, 0, 0);
}

.semi-transparent {
  background-color: rgba(0, 0, 255, 0.5); /* Blue at 50% opacity */
}

.custom {
  color: rgb(100, 150, 200);
}
```

---

### hsl() / hsla()
**Definition:** Defines colors using Hue, Saturation, Lightness (and Alpha).

**Explanation:** Hue (0-360), Saturation (0-100%), Lightness (0-100%).

**Example:**
```css
.red {
  color: hsl(0, 100%, 50%);
}

.blue {
  color: hsl(240, 100%, 50%);
}

.pastel {
  background-color: hsl(200, 50%, 80%); /* Light blue */
}

.semi-transparent {
  color: hsla(120, 100%, 50%, 0.7); /* Green at 70% opacity */
}
```

---

### currentColor
**Definition:** Keyword that represents the current value of color property.

**Explanation:** Useful for inheriting text color to borders, SVG fills, etc.

**Example:**
```css
.box {
  color: red;
  border: 2px solid currentColor; /* Border will be red */
}

.icon {
  color: blue;
  fill: currentColor; /* SVG fill will be blue */
}
```

---

## 📏 Sizing Units

### Absolute Units
**Definition:** Fixed sizes that don't change.

**Explanation:** px, pt, cm, mm, in.

**Example:**
```css
.pixels {
  font-size: 16px; /* Most common */
}

.points {
  font-size: 12pt; /* Commonly for print */
}

.inches {
  width: 2in; /* Physical inches */
}
```

---

### Relative Units
**Definition:** Sizes relative to something else.

**Explanation:** em, rem, %, vw, vh, vmin, vmax.

**Example:**
```css
.em-unit {
  font-size: 2em; /* 2 times parent's font size */
}

.rem-unit {
  font-size: 1.5rem; /* 1.5 times root font size */
}

.percentage {
  width: 50%; /* 50% of parent width */
}

.viewport {
  width: 50vw; /* 50% of viewport width */
  height: 100vh; /* 100% of viewport height */
}

.vmin-vmax {
  font-size: 5vmin; /* 5% of smaller viewport dimension */
  width: 80vmax; /* 80% of larger viewport dimension */
}
```

---

### ch and ex Units
**Definition:** Relative to font metrics.

**Explanation:** ch = width of "0" character, ex = height of "x" character.

**Example:**
```css
.input {
  width: 20ch; /* Wide enough for 20 characters */
}

.small {
  font-size: 2ex;
}
```

---

## 🎭 More Pseudo-classes

### :nth-of-type()
**Definition:** Selects elements of same type by position.

**Example:**
```css
p:nth-of-type(2) {
  color: red; /* Second paragraph only */
}

div:nth-of-type(odd) {
  background-color: #f0f0f0;
}
```

---

### :first-of-type / :last-of-type
**Definition:** Selects first or last element of its type.

**Example:**
```css
p:first-of-type {
  font-weight: bold; /* First paragraph */
}

img:last-of-type {
  margin-bottom: 0; /* Last image */
}
```

---

### :only-child / :only-of-type
**Definition:** Selects elements that are the only child or only of their type.

**Example:**
```css
p:only-child {
  text-align: center; /* Paragraph that's the only child */
}

li:only-of-type {
  list-style: none; /* Single list item */
}
```

---

### :empty
**Definition:** Selects elements with no children (including text).

**Example:**
```css
div:empty {
  display: none; /* Hide empty divs */
}

p:empty::before {
  content: "No content";
  color: gray;
}
```

---

### :target
**Definition:** Selects element that is the target of URL fragment.

**Example:**
```css
:target {
  background-color: yellow; /* Highlights anchored section */
}

#section1:target {
  border: 2px solid blue;
}
```

---

### :valid / :invalid
**Definition:** Styles form elements based on validation.

**Example:**
```css
input:valid {
  border: 2px solid green;
}

input:invalid {
  border: 2px solid red;
}

input:required:invalid {
  background-color: #ffe0e0;
}
```

---

### :in-range / :out-of-range
**Definition:** Styles inputs based on min/max constraints.

**Example:**
```css
input[type="number"]:in-range {
  border-color: green;
}

input[type="number"]:out-of-range {
  border-color: red;
}
```

---

### :optional / :required
**Definition:** Styles form fields based on required attribute.

**Example:**
```css
input:required {
  border-left: 3px solid red;
}

input:optional {
  border-left: 3px solid gray;
}
```

---

### :read-only / :read-write
**Definition:** Styles based on whether element is editable.

**Example:**
```css
input:read-only {
  background-color: #f0f0f0;
  cursor: not-allowed;
}

input:read-write {
  background-color: white;
}
```

---

### :placeholder-shown
**Definition:** Selects input when placeholder is visible.

**Example:**
```css
input:placeholder-shown {
  border: 1px solid gray;
}

input:not(:placeholder-shown) {
  border: 1px solid blue; /* When user types */
}
```

---

## 🎨 More Pseudo-elements

### ::placeholder
**Definition:** Styles the placeholder text in inputs.

**Example:**
```css
input::placeholder {
  color: lightgray;
  font-style: italic;
}

textarea::placeholder {
  color: #999;
  opacity: 0.7;
}
```

---

### ::marker
**Definition:** Styles the marker of list items.

**Example:**
```css
li::marker {
  color: red;
  font-size: 1.5em;
}

::marker {
  content: "✓ ";
}
```

---

### ::backdrop
**Definition:** Styles the backdrop of dialog/fullscreen elements.

**Example:**
```css
dialog::backdrop {
  background-color: rgba(0, 0, 0, 0.8);
  backdrop-filter: blur(5px);
}
```

---

## 📐 Advanced Sizing

### aspect-ratio
**Definition:** Maintains width-to-height ratio.

**Explanation:** Great for responsive videos and images.

**Example:**
```css
.video-container {
  aspect-ratio: 16 / 9; /* 16:9 ratio */
}

.square {
  aspect-ratio: 1 / 1; /* Perfect square */
}

.portrait {
  aspect-ratio: 3 / 4;
}
```

---

### resize
**Definition:** Allows user to resize element.

**Explanation:** Options: none, both, horizontal, vertical.

**Example:**
```css
textarea {
  resize: vertical; /* Only vertical resize */
}

.resizable {
  resize: both; /* Resize in both directions */
  overflow: auto;
}

.no-resize {
  resize: none;
}
```

---

### min(), max(), clamp()
**Definition:** CSS functions for responsive sizing.

**Explanation:** min() picks smallest, max() picks largest, clamp() sets min/preferred/max.

**Example:**
```css
.responsive {
  width: min(100%, 800px); /* Never wider than 800px */
}

.large-enough {
  font-size: max(16px, 1vw); /* At least 16px */
}

.fluid {
  font-size: clamp(16px, 2vw, 32px);
  /* Min 16px, preferred 2vw, max 32px */
}

.container {
  width: clamp(300px, 80%, 1200px);
}
```

---

### calc()
**Definition:** Performs calculations for property values.

**Explanation:** Can mix units (px, %, em, etc.).

**Example:**
```css
.sidebar {
  width: calc(100% - 250px); /* Full width minus sidebar */
}

.centered {
  margin-left: calc(50% - 200px);
}

.responsive {
  font-size: calc(16px + 1vw);
}

.complex {
  height: calc(100vh - 80px - 2rem);
}
```

---

## 🎨 Backdrop & Filters

### backdrop-filter
**Definition:** Applies filter effects to area behind element.

**Explanation:** Creates frosted glass effect. Requires transparency.

**Example:**
```css
.glass {
  background-color: rgba(255, 255, 255, 0.3);
  backdrop-filter: blur(10px);
  /* Frosted glass effect */
}

.dark-glass {
  background-color: rgba(0, 0, 0, 0.4);
  backdrop-filter: blur(5px) brightness(80%);
}
```

---

### More Filter Functions
**Definition:** Additional filter effects.

**Example:**
```css
.saturate {
  filter: saturate(200%); /* More colorful */
}

.desaturate {
  filter: saturate(50%); /* Less colorful */
}

.hue-rotate {
  filter: hue-rotate(90deg); /* Shift colors */
}

.invert {
  filter: invert(100%); /* Negative effect */
}

.drop-shadow {
  filter: drop-shadow(0 4px 8px rgba(0,0,0,0.3));
  /* Shadow that follows element shape */
}
```

---

## 🔤 More Text Properties

### hyphens
**Definition:** Controls hyphenation of text.

**Explanation:** Options: none, manual, auto.

**Example:**
```css
p {
  hyphens: auto; /* Automatic hyphenation */
}

.no-hyphens {
  hyphens: none;
}

.manual {
  hyphens: manual; /* Only at &shy; */
}
```

---

### writing-mode
**Definition:** Changes text direction (horizontal/vertical).

**Explanation:** For different writing systems.

**Example:**
```css
.vertical {
  writing-mode: vertical-rl; /* Right to left, vertical */
}

.sideways {
  writing-mode: sideways-lr;
}
```

---

### text-orientation
**Definition:** Sets orientation of text in vertical mode.

**Example:**
```css
.vertical {
  writing-mode: vertical-rl;
  text-orientation: upright; /* Characters stay upright */
}
```

---

### tab-size
**Definition:** Sets width of tab character.

**Example:**
```css
pre {
  tab-size: 4; /* Tab equals 4 spaces */
}

.wide-tabs {
  tab-size: 8;
}
```

---

### column-count / column-width
**Definition:** Creates multi-column text layout.

**Explanation:** Like newspaper columns.

**Example:**
```css
.newspaper {
  column-count: 3; /* Three columns */
  column-gap: 40px; /* Space between columns */
}

.flexible {
  column-width: 250px; /* Auto columns at 250px width */
}

.with-rule {
  column-count: 2;
  column-rule: 2px solid gray; /* Line between columns */
}
```

---

### column-gap / row-gap
**Definition:** Sets spacing between columns or rows.

**Explanation:** Works with flexbox, grid, and multi-column.

**Example:**
```css
.grid {
  display: grid;
  column-gap: 20px;
  row-gap: 30px;
}

/* Or shorthand */
.container {
  gap: 30px 20px; /* row-gap column-gap */
}
```

---

## 🎯 Pointer Events

### pointer-events
**Definition:** Controls whether element responds to mouse events.

**Example:**
```css
.disabled {
  pointer-events: none; /* Can't be clicked */
  opacity: 0.5;
}

.clickable {
  pointer-events: auto; /* Normal behavior */
}

.pass-through {
  pointer-events: none; /* Clicks go through to elements below */
}
```

---

### user-select
**Definition:** Controls whether user can select text.

**Example:**
```css
.no-select {
  user-select: none; /* Can't select text */
}

.selectable {
  user-select: text; /* Can select */
}

.select-all {
  user-select: all; /* Selects everything on click */
}
```

---

## 🎨 Scroll Behavior

### scroll-behavior
**Definition:** Controls smooth scrolling.

**Example:**
```css
html {
  scroll-behavior: smooth; /* Smooth anchor scrolling */
}

.instant {
  scroll-behavior: auto; /* Instant jump */
}
```

---

### scroll-snap-type
**Definition:** Creates scroll snapping container.

**Explanation:** Makes scrolling snap to specific points.

**Example:**
```css
.container {
  scroll-snap-type: x mandatory; /* Horizontal snapping */
  overflow-x: scroll;
}

.item {
  scroll-snap-align: start; /* Snap to start of item */
}

.vertical-snap {
  scroll-snap-type: y proximity;
}
```

---

### scroll-padding / scroll-margin
**Definition:** Adjusts scroll snap positions.

**Example:**
```css
.container {
  scroll-padding: 20px; /* Offset for snap positions */
}

.item {
  scroll-margin: 10px; /* Margin around snap point */
}
```

---

### overscroll-behavior
**Definition:** Controls behavior when scrolling past limits.

**Example:**
```css
body {
  overscroll-behavior: contain; /* Prevents scroll chaining */
}

.modal {
  overscroll-behavior: none; /* Prevents pull-to-refresh */
}
```

---

## 🎭 Content & Counters

### content (Advanced)
**Definition:** More advanced uses of content property.

**Example:**
```css
/* Attribute values */
a::after {
  content: " (" attr(href) ")";
  /* Shows link URL */
}

/* Counters */
body {
  counter-reset: section;
}

h2::before {
  counter-increment: section;
  content: "Section " counter(section) ": ";
}

/* Multiple counters */
ol {
  counter-reset: item;
}

li::before {
  counter-increment: item;
  content: counter(item) ". ";
}
```

---

### quotes
**Definition:** Sets quotation marks for q element.

**Example:**
```css
q {
  quotes: "«" "»" "‹" "›";
}

.english {
  quotes: """ """ "'" "'";
}
```

---

## 🎨 Appearance & UI

### appearance
**Definition:** Controls native appearance of UI elements.

**Example:**
```css
button {
  appearance: none; /* Removes default button style */
}

select {
  appearance: none; /* Custom dropdown styling */
}

input[type="checkbox"] {
  appearance: none; /* Custom checkbox */
  width: 20px;
  height: 20px;
  border: 2px solid blue;
}
```

---

### caret-color
**Definition:** Sets color of text input cursor.

**Example:**
```css
input {
  caret-color: blue; /* Blue cursor */
}

textarea {
  caret-color: red;
}

.auto {
  caret-color: auto; /* Matches text color */
}
```

---

### outline
**Definition:** Draws outline outside border (doesn't affect layout).

**Explanation:** Similar to border but doesn't take up space.

**Example:**
```css
button:focus {
  outline: 2px solid blue;
  outline-offset: 2px; /* Space between element and outline */
}

.no-outline {
  outline: none; /* Remove outline (be careful with accessibility!) */
}

.dashed-outline {
  outline: 3px dashed red;
}
```

---

### accent-color
**Definition:** Sets accent color for form controls.

**Explanation:** Modern way to style checkboxes, radios, range inputs.

**Example:**
```css
input[type="checkbox"] {
  accent-color: blue;
}

input[type="radio"] {
  accent-color: green;
}

input[type="range"] {
  accent-color: purple;
}
```

---

## 🎯 Clipping & Masking

### clip-path
**Definition:** Clips element to specific shape.

**Example:**
```css
.circle {
  clip-path: circle(50%); /* Circular clip */
}

.triangle {
  clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
}

.rounded {
  clip-path: inset(0 round 20px); /* Rounded rectangle */
}

.custom {
  clip-path: ellipse(40% 50% at 50% 50%);
}
```

---

### mask
**Definition:** Applies mask to hide/show parts of element.

**Example:**
```css
.masked {
  mask-image: url('mask.png');
  mask-size: cover;
}

.gradient-mask {
  mask-image: linear-gradient(to bottom, black, transparent);
}
```

---

## 🎨 Break Properties

### break-before / break-after / break-inside
**Definition:** Controls page/column breaks for printing.

**Example:**
```css
h1 {
  break-before: page; /* Start on new page */
}

.keep-together {
  break-inside: avoid; /* Don't break element */
}

@media print {
  .section {
    break-after: page;
  }
}
```

---

## 📱 Touch & Mobile

### touch-action
**Definition:** Controls touch gestures on element.

**Example:**
```css
.no-zoom {
  touch-action: manipulation; /* Prevents double-tap zoom */
}

.pan-y {
  touch-action: pan-y; /* Only vertical panning */
}

.none {
  touch-action: none; /* No touch interactions */
}
```

---

### -webkit-tap-highlight-color
**Definition:** Controls tap highlight color on mobile.

**Example:**
```css
button {
  -webkit-tap-highlight-color: transparent; /* Remove tap highlight */
}

a {
  -webkit-tap-highlight-color: rgba(0, 0, 255, 0.3);
}
```

---

## 🎭 Blending & Compositing

### background-blend-mode
**Definition:** Blends background layers together.

**Example:**
```css
.blended {
  background: 
    url('texture.png'),
    linear-gradient(blue, purple);
  background-blend-mode: multiply;
}

.screen {
  background-blend-mode: screen;
}
```

---

### isolation
**Definition:** Creates new stacking context for blending.

**Example:**
```css
.isolated {
  isolation: isolate; /* Isolates blend modes */
}
```

---

## 🎯 CSS Shapes

### shape-outside
**Definition:** Wraps text around shapes.

**Explanation:** Works with floated elements.

**Example:**
```css
.circle-wrap {
  float: left;
  width: 200px;
  height: 200px;
  shape-outside: circle(50%);
  /* Text wraps around circle */
}

.polygon-wrap {
  float: right;
  shape-outside: polygon(0 0, 100% 0, 100% 100%);
}
```

---

### shape-margin
**Definition:** Adds margin around shape.

**Example:**
```css
.image {
  shape-outside: circle(50%);
  shape-margin: 20px; /* Space around shape */
}
```

---

## 🎨 Image Rendering

### image-rendering
**Definition:** Controls how images are scaled.

**Example:**
```css
.pixelated {
  image-rendering: pixelated; /* For pixel art */
}

.crisp {
  image-rendering: crisp-edges; /* Sharp edges */
}

.smooth {
  image-rendering: auto; /* Default smooth */
}
```

---

## 📐 Other Useful Properties

### all
**Definition:** Resets all properties to initial or inherited values.

**Example:**
```css
.reset {
  all: initial; /* Resets everything */
}

.inherit-all {
  all: inherit; /* Inherits everything from parent */
}

.unset {
  all: unset; /* Inherits or resets as appropriate */
}
```

---

### will-change
**Definition:** Hints browser about upcoming changes for optimization.

**Explanation:** Use sparingly for performance.

**Example:**
```css
.animated {
  will-change: transform, opacity;
  /* Browser optimizes these properties */
}

/* Remove after animation */
.animated.done {
  will-change: auto;
}
```

---

### contain
**Definition:** Improves performance by limiting scope of calculations.

**Example:**
```css
.card {
  contain: layout style paint;
  /* Isolates layout, style, and paint operations */
}

.strict {
  contain: strict; /* All containment types */
}
```

---

### font-display
**Definition:** Controls how fonts display while loading.

**Example:**
```css
@font-face {
  font-family: 'CustomFont';
  src: url('font.woff2');
  font-display: swap; /* Shows fallback first, then swaps */
}

/* Options: auto, block, swap, fallback, optional */
```

---

### direction
**Definition:** Sets text direction (left-to-right or right-to-left).

**Example:**
```css
.rtl {
  direction: rtl; /* Right to left (Arabic, Hebrew) */
}

.ltr {
  direction: ltr; /* Left to right (default) */
}
```

---

### unicode-bidi
**Definition:** Controls bidirectional text algorithm.

**Example:**
```css
.bidi-override {
  unicode-bidi: bidi-override;
  direction: rtl;
}

.embed {
  unicode-bidi: embed;
}
```

---

## 🎨 Print Styles

### @page
**Definition:** Modifies page properties when printing.

**Example:**
```css
@page {
  size: A4;
  margin: 2cm;
}

@page :first {
  margin-top: 5cm; /* First page different margin */
}

@page :left {
  margin-left: 3cm; /* Left pages */
}

@page :right {
  margin-right: 3cm; /* Right pages */
}
```

---

### orphans / widows
**Definition:** Controls lines at page/column breaks.

**Example:**
```css
p {
  orphans: 3; /* Min lines at bottom of page */
  widows: 3; /* Min lines at top of page */
}
```

---

## 🎯 CSS Logical Properties

### Logical Margin & Padding
**Definition:** Direction-independent spacing (adapts to writing mode).

**Example:**
```css
.box {
  margin-inline-start: 20px; /* Left in LTR, right in RTL */
  margin-inline-end: 20px; /* Right in LTR, left in RTL */
  margin-block-start: 10px; /* Top */
  margin-block-end: 10px; /* Bottom */
}

.padding {
  padding-inline: 20px; /* Horizontal */
  padding-block: 10px; /* Vertical */
}
```

---

### Logical Border
**Definition:** Direction-independent borders.

**Example:**
```css
.box {
  border-inline-start: 2px solid blue; /* Left in LTR */
  border-block-start: 2px solid red; /* Top */
}
```

---

### Logical Size
**Definition:** Direction-independent sizing.

**Example:**
```css
.box {
  inline-size: 200px; /* Width in horizontal writing */
  block-size: 100px; /* Height in horizontal writing */
}

.max {
  max-inline-size: 800px;
  max-block-size: 600px;
}
```

---

### inset
**Definition:** Shorthand for top, right, bottom, left.

**Example:**
```css
.positioned {
  position: absolute;
  inset: 10px; /* All sides 10px */
}

.custom {
  inset: 10px 20px 30px 40px; /* top right bottom left */
}

/* Logical versions */
.logical {
  inset-block-start: 10px; /* top */
  inset-inline-end: 20px; /* right in LTR */
}
```

---

## 🎨 Advanced Animations

### animation-timing-function
**Definition:** Controls animation speed curve.

**Example:**
```css
.ease {
  animation: slide 2s ease; /* Slow start and end */
}

.linear {
  animation: slide 2s linear; /* Constant speed */
}

.ease-in {
  animation: slide 2s ease-in; /* Slow start */
}

.ease-out {
  animation: slide 2s ease-out; /* Slow end */
}

.ease-in-out {
  animation: slide 2s ease-in-out; /* Slow start and end */
}

.cubic-bezier {
  animation: slide 2s cubic-bezier(0.68, -0.55, 0.265, 1.55);
  /* Custom easing curve */
}

.steps {
  animation: slide 2s steps(4); /* 4 discrete steps */
}
```

---

### animation-fill-mode
**Definition:** Specifies styles before/after animation.

**Example:**
```css
.forwards {
  animation: fadeIn 1s forwards;
  /* Keeps final animation state */
}

.backwards {
  animation: fadeIn 1s backwards;
  /* Applies initial animation state before start */
}

.both {
  animation: fadeIn 1s both;
  /* Applies both forwards and backwards */
}

.none {
  animation: fadeIn 1s none;
  /* Default, no fill mode */
}
```

---

### animation-play-state
**Definition:** Pauses or runs animation.

**Example:**
```css
.animation {
  animation: spin 2s infinite;
}

.paused {
  animation-play-state: paused;
}

.running {
  animation-play-state: running;
}

/* Pause on hover */
.box:hover {
  animation-play-state: paused;
}
```

---

## 🎯 Transition Properties

### transition-property
**Definition:** Specifies which properties should transition.

**Example:**
```css
.button {
  transition-property: background-color, transform;
  /* Only these properties transition */
}

.all {
  transition-property: all; /* All properties */
}

.specific {
  transition-property: width, height, opacity;
}
```

---

### transition-duration
**Definition:** How long transition takes.

**Example:**
```css
.fast {
  transition-duration: 0.2s;
}

.slow {
  transition-duration: 2s;
}

.multiple {
  transition-duration: 0.3s, 1s, 0.5s;
  /* Different durations for different properties */
}
```

---

### transition-timing-function
**Definition:** Speed curve of transition.

**Example:**
```css
.ease {
  transition-timing-function: ease;
}

.linear {
  transition-timing-function: linear;
}

.bounce {
  transition-timing-function: cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.steps {
  transition-timing-function: steps(5, jump-end);
}
```

---

### transition-delay
**Definition:** Delay before transition starts.

**Example:**
```css
.delayed {
  transition-delay: 0.5s; /* Waits 0.5s */
}

.staggered {
  transition-delay: 0.1s, 0.2s, 0.3s;
  /* Different delays for different properties */
}
```

---

## 🎨 Transform Functions

### translate() / translateX() / translateY() / translateZ()
**Definition:** Moves element from its position.

**Example:**
```css
.move {
  transform: translate(50px, 100px);
  /* 50px right, 100px down */
}

.move-x {
  transform: translateX(100px); /* Horizontal only */
}

.move-y {
  transform: translateY(-50px); /* Vertical only */
}

.move-3d {
  transform: translateZ(100px); /* Depth (requires perspective) */
}
```

---

### scale() / scaleX() / scaleY() / scaleZ()
**Definition:** Resizes element.

**Example:**
```css
.bigger {
  transform: scale(1.5); /* 150% size */
}

.smaller {
  transform: scale(0.5); /* 50% size */
}

.stretch-x {
  transform: scaleX(2); /* Double width */
}

.stretch-y {
  transform: scaleY(1.5); /* 150% height */
}

.flip {
  transform: scaleX(-1); /* Horizontal flip */
}
```

---

### rotate() / rotateX() / rotateY() / rotateZ()
**Definition:** Rotates element.

**Example:**
```css
.rotate {
  transform: rotate(45deg); /* 45 degrees clockwise */
}

.rotate-counter {
  transform: rotate(-90deg); /* Counter-clockwise */
}

.flip-x {
  transform: rotateX(180deg); /* Flip vertically */
}

.flip-y {
  transform: rotateY(180deg); /* Flip horizontally */
}

.spin-z {
  transform: rotateZ(360deg); /* Same as rotate() */
}
```

---

### skew() / skewX() / skewY()
**Definition:** Skews element along axis.

**Example:**
```css
.skew {
  transform: skew(20deg, 10deg);
  /* 20deg X-axis, 10deg Y-axis */
}

.skew-x {
  transform: skewX(15deg);
}

.skew-y {
  transform: skewY(10deg);
}

.parallelogram {
  transform: skewX(-20deg);
}
```

---

### matrix() / matrix3d()
**Definition:** Combines all transformations in one.

**Explanation:** Complex but powerful. Usually auto-generated.

**Example:**
```css
.matrix {
  transform: matrix(1, 0, 0, 1, 50, 100);
  /* Equivalent to translate(50px, 100px) */
}

.matrix3d {
  transform: matrix3d(1,0,0,0, 0,1,0,0, 0,0,1,0, 50,100,0,1);
}
```

---

### perspective
**Definition:** Sets distance for 3D transformations.

**Example:**
```css
.container {
  perspective: 1000px; /* Container perspective */
}

.card {
  transform: perspective(500px) rotateY(45deg);
  /* Element perspective */
}

.deep {
  perspective: 2000px; /* Less dramatic */
}

.shallow {
  perspective: 300px; /* More dramatic */
}
```

---

### perspective-origin
**Definition:** Sets vanishing point for 3D transforms.

**Example:**
```css
.container {
  perspective: 1000px;
  perspective-origin: top left; /* Vanishing point at top-left */
}

.centered {
  perspective-origin: 50% 50%; /* Default center */
}

.bottom {
  perspective-origin: bottom;
}
```

---

### transform-origin
**Definition:** Sets origin point for transformations.

**Example:**
```css
.rotate-corner {
  transform-origin: top left; /* Rotates from top-left */
  transform: rotate(45deg);
}

.scale-center {
  transform-origin: center; /* Default */
  transform: scale(1.5);
}

.custom {
  transform-origin: 100px 50px; /* Specific point */
}

.bottom-right {
  transform-origin: bottom right;
}
```

---

### transform-style
**Definition:** Preserves 3D space for child elements.

**Example:**
```css
.preserve-3d {
  transform-style: preserve-3d; /* Children in 3D space */
}

.flat {
  transform-style: flat; /* Default, children flattened */
}

.card-flip {
  transform-style: preserve-3d;
  transition: transform 0.6s;
}
```

---

### backface-visibility
**Definition:** Shows or hides back face of element.

**Example:**
```css
.card-back {
  backface-visibility: hidden; /* Hide when rotated away */
}

.visible {
  backface-visibility: visible; /* Default */
}

/* Useful for card flip animations */
.flip-card {
  transform-style: preserve-3d;
}

.flip-card-front,
.flip-card-back {
  backface-visibility: hidden;
}

.flip-card-back {
  transform: rotateY(180deg);
}
```

---

## 🎨 CSS Grid (Advanced)

### grid-template-areas
**Definition:** Defines named grid areas.

**Example:**
```css
.container {
  display: grid;
  grid-template-areas:
    "header header header"
    "sidebar main main"
    "footer footer footer";
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
.footer { grid-area: footer; }

/* Responsive layout */
@media (max-width: 768px) {
  .container {
    grid-template-areas:
      "header"
      "main"
      "sidebar"
      "footer";
  }
}
```

---

### minmax()
**Definition:** Sets minimum and maximum size for grid tracks.

**Example:**
```css
.grid {
  display: grid;
  grid-template-columns: minmax(200px, 1fr) minmax(300px, 2fr);
  /* Min 200px, max 1fr | Min 300px, max 2fr */
}

.flexible {
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  /* Responsive columns */
}

.rows {
  grid-template-rows: minmax(100px, auto);
  /* Min 100px, grows with content */
}
```

---

### auto-fit vs auto-fill
**Definition:** Controls how auto-placed columns behave.

**Example:**
```css
.auto-fit {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  /* Expands columns to fill space */
}

.auto-fill {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  /* Creates empty columns if space available */
}
```

---

### dense
**Definition:** Fills gaps in grid layout.

**Example:**
```css
.grid {
  display: grid;
  grid-auto-flow: dense;
  /* Items fill gaps in grid */
}

.masonry-like {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-flow: dense;
}
```

---

## 🎯 Flexbox (Advanced)

### flex-flow
**Definition:** Shorthand for flex-direction and flex-wrap.

**Example:**
```css
.container {
  display: flex;
  flex-flow: row wrap;
  /* direction: row, wrapping enabled */
}

.column-nowrap {
  flex-flow: column nowrap;
}

.reverse-wrap {
  flex-flow: row-reverse wrap;
}
```

---

### align-self
**Definition:** Overrides align-items for individual flex item.

**Example:**
```css
.container {
  display: flex;
  align-items: flex-start;
}

.special {
  align-self: center; /* This item centers */
}

.stretch {
  align-self: stretch; /* This item stretches */
}

.end {
  align-self: flex-end; /* This item goes to end */
}
```

---

## 🎨 Advanced Backgrounds

### Multiple Backgrounds
**Definition:** Layer multiple background images.

**Example:**
```css
.layered {
  background:
    url('top-layer.png') no-repeat center top,
    url('middle.png') repeat-x bottom,
    linear-gradient(to bottom, transparent, white),
    url('bottom.jpg') no-repeat center;
}

.complex {
  background-image: 
    url('pattern.png'),
    linear-gradient(135deg, blue, purple);
  background-size: 
    auto,
    cover;
  background-position: 
    0 0,
    center;
}
```

---

### background-clip
**Definition:** Defines how far background extends.

**Example:**
```css
.border-box {
  background-clip: border-box; /* Default, includes border */
}

.padding-box {
  background-clip: padding-box; /* Stops at padding */
}

.content-box {
  background-clip: content-box; /* Only content area */
}

.text-clip {
  background-clip: text;
  -webkit-background-clip: text;
  color: transparent;
  background-image: linear-gradient(45deg, blue, purple);
  /* Gradient text effect */
}
```

---

### background-origin
**Definition:** Specifies positioning area of background.

**Example:**
```css
.border-box {
  background-origin: border-box; /* Starts from border */
}

.padding-box {
  background-origin: padding-box; /* Default, starts from padding */
}

.content-box {
  background-origin: content-box; /* Starts from content */
}
```

---

## 🎯 Advanced Borders

### border-image
**Definition:** Uses image as border.

**Example:**
```css
.fancy-border {
  border: 10px solid transparent;
  border-image: url('border.png') 30 round;
}

.gradient-border {
  border: 5px solid;
  border-image: linear-gradient(45deg, red, blue) 1;
}

.repeating {
  border-image: url('pattern.png') 30 repeat;
}
```

---

### border-image-slice
**Definition:** Slices border image into regions.

**Example:**
```css
.sliced {
  border-image-source: url('border.png');
  border-image-slice: 30; /* Pixels from edge */
}

.percentage {
  border-image-slice: 30%; /* Percentage */
}

.fill {
  border-image-slice: 30 fill; /* Also fills center */
}
```

---

### Individual Border Radius
**Definition:** Different radius for each corner.

**Example:**
```css
.custom {
  border-radius: 10px 20px 30px 40px;
  /* top-left, top-right, bottom-right, bottom-left */
}

.organic {
  border-top-left-radius: 50% 30%;
  border-top-right-radius: 30% 50%;
  border-bottom-right-radius: 50% 30%;
  border-bottom-left-radius: 30% 50%;
  /* Creates organic shape */
}

.pill-left {
  border-radius: 50px 0 0 50px;
}
```

---

## 🎨 CSS Functions (Advanced)

### var() with Fallbacks
**Definition:** CSS variables with default values.

**Example:**
```css
:root {
  --primary: blue;
}

.element {
  color: var(--primary, red);
  /* Uses red if --primary undefined */
}

.nested {
  color: var(--secondary, var(--primary, black));
  /* Multiple fallbacks */
}
```

---

### attr()
**Definition:** Uses HTML attribute values in CSS.

**Example:**
```css
a::after {
  content: " (" attr(href) ")";
  /* Shows link URL */
}

.tooltip {
  position: relative;
}

.tooltip::after {
  content: attr(data-tooltip);
  /* Uses data-tooltip attribute value */
}

[data-size]::before {
  content: "Size: " attr(data-size);
}
```

---

### url()
**Definition:** References external resources.

**Example:**
```css
.background {
  background-image: url('image.jpg');
}

.absolute {
  background-image: url('https://example.com/image.jpg');
}

.relative {
  background-image: url('../images/bg.png');
}

.data-uri {
  background-image: url('data:image/svg+xml;base64,PHN2Zy...');
}
```

---

## 🎯 Layout Modes

### display: table
**Definition:** Makes element behave like table.

**Example:**
```css
.table {
  display: table;
  width: 100%;
}

.row {
  display: table-row;
}

.cell {
  display: table-cell;
  padding: 10px;
  border: 1px solid gray;
}

.caption {
  display: table-caption;
  caption-side: top;
}
```

---

### display: inline-block
**Definition:** Inline element that can have width/height.

**Example:**
```css
.inline-block {
  display: inline-block;
  width: 200px;
  height: 100px;
  /* Flows inline but respects dimensions */
}

.button {
  display: inline-block;
  padding: 10px 20px;
  /* Perfect for navigation items */
}
```

---

### display: contents
**Definition:** Element disappears, children take its place.

**Example:**
```css
.wrapper {
  display: contents;
  /* Wrapper ignored in layout, children participate directly */
}

/* Useful for flex/grid layouts */
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.ignore-wrapper {
  display: contents;
  /* Children become direct grid items */
}
```

---

## 🎨 Advanced Positioning

### sticky Positioning
**Definition:** Switches between relative and fixed based on scroll.

**Example:**
```css
.sticky-header {
  position: sticky;
  top: 0; /* Sticks to top when scrolled to */
  background: white;
  z-index: 100;
}

.sidebar {
  position: sticky;
  top: 20px; /* Sticks 20px from top */
}

.bottom-sticky {
  position: sticky;
  bottom: 0; /* Sticks to bottom */
}
```

---

### Multi-layer z-index
**Definition:** Creating stacking contexts.

**Example:**
```css
/* Stacking context */
.layer-1 {
  position: relative;
  z-index: 1;
}

.layer-1-child {
  position: absolute;
  z-index: 9999; /* Only higher within .layer-1 */
}

.layer-2 {
  position: relative;
  z-index: 2; /* Appears above all .layer-1 children */
}

/* Common z-index scale */
.dropdown { z-index: 1000; }
.modal { z-index: 2000; }
.tooltip { z-index: 3000; }
.notification { z-index: 4000; }
```

---

## 🎯 Advanced Selectors

### :is() and :where()
**Definition:** Groups selectors, :where() has 0 specificity.

**Example:**
```css
/* Instead of */
h1 a, h2 a, h3 a { color: blue; }

/* Use :is() */
:is(h1, h2, h3) a { color: blue; }

/* :where() has 0 specificity */
:where(h1, h2, h3) a { color: blue; }
/* Can be easily overridden */

:is(section, article) :is(h1, h2, h3) {
  margin-top: 0;
}
```

---

### :has()
**Definition:** Parent selector - selects element that contains something.

**Example:**
```css
/* Select article that has img */
article:has(img) {
  grid-column: span 2;
}

/* Select div with .error class inside */
div:has(.error) {
  border: 2px solid red;
}

/* Form with invalid input */
form:has(input:invalid) {
  border-color: red;
}

/* Card with no image */
.card:not(:has(img)) {
  padding: 20px;
}
```

---

### :focus-within
**Definition:** Selects element when it or a descendant has focus.

**Example:**
```css
form:focus-within {
  box-shadow: 0 0 0 3px rgba(0, 123, 255, 0.25);
  /* Highlights form when any input focused */
}

.search-container:focus-within {
  border-color: blue;
}

nav:focus-within {
  background-color: lightblue;
}
```

---

### :focus-visible
**Definition:** Matches focused element only when focus should be visible.

**Example:**
```css
/* Show focus for keyboard navigation only */
button:focus-visible {
  outline: 2px solid blue;
}

/* Hide focus for mouse clicks */
button:focus:not(:focus-visible) {
  outline: none;
}

input:focus-visible {
  border: 2px solid blue;
}
```

---

### ::backdrop (fullscreen)
**Definition:** Styles backdrop of fullscreen elements.

**Example:**
```css
video::backdrop {
  background: black;
}

dialog::backdrop {
  background: rgba(0, 0, 0, 0.8);
  backdrop-filter: blur(5px);
}

.fullscreen::backdrop {
  background: linear-gradient(45deg, purple, blue);
}
```

---

## 🎨 Color Spaces & Modern Colors

### color-mix()
**Definition:** Mixes two colors together.

**Example:**
```css
.mixed {
  background: color-mix(in srgb, red 50%, blue);
  /* 50% red, 50% blue */
}

.lighter {
  background: color-mix(in srgb, var(--primary) 80%, white);
  /* Lightens primary color */
}

.darker {
  background: color-mix(in srgb, blue 70%, black);
}
```

---

### oklch() / oklab()
**Definition:** Modern perceptually uniform color spaces.

**Example:**
```css
.oklch {
  color: oklch(60% 0.2 180);
  /* Lightness, Chroma, Hue */
}

.oklab {
  color: oklab(60% -0.1 0.1);
  /* Lightness, a-axis, b-axis */
}
```

---

## 🎯 Container Queries

### @container
**Definition:** Styles based on container size, not viewport.

**Example:**
```css
.container {
  container-type: inline-size;
  container-name: card;
}

@container card (min-width: 400px) {
  .card-title {
    font-size: 2rem;
  }
}

/* Without name */
.parent {
  container-type: inline-size;
}

@container (min-width: 500px) {
  .child {
    display: flex;
  }
}
```

---

### container-type
**Definition:** Defines container for queries.

**Example:**
```css
.size-container {
  container-type: size; /* Width and height */
}

.inline-container {
  container-type: inline-size; /* Width only (most common) */
}

.normal {
  container-type: normal; /* Not a container */
}
```

---

## 🎨 Scroll-driven Animations

### animation-timeline
**Definition:** Links animation to scroll position.

**Example:**
```css
@keyframes fade-in {
  from { opacity: 0; }
  to { opacity: 1; }
}

.scroll-animate {
  animation: fade-in linear;
  animation-timeline: scroll();
  /* Animates based on page scroll */
}

.container-scroll {
  animation-timeline: scroll(nearest);
  /* Animates based on nearest scrollable ancestor */
}
```

---

### animation-range
**Definition:** Controls when scroll animation starts/ends.

**Example:**
```css
.element {
  animation: fade-in linear;
  animation-timeline: scroll();
  animation-range: 0% 100%;
  /* Animates through entire scroll */
}

.partial {
  animation-range: 20% 80%;
  /* Only animates in middle portion */
}
```

---

## 🎯 Cascade Layers

### @layer
**Definition:** Controls specificity with layers.

**Example:**
```css
/* Define layer order */
@layer reset, base, components, utilities;

@layer reset {
  * { margin: 0; padding: 0; }
}

@layer base {
  body { font-family: Arial; }
}

@layer components {
  .button { padding: 10px 20px; }
}

@layer utilities {
  .hidden { display: none !important; }
}

/* Utilities layer wins regardless of specificity */
```

---

## 🎨 Nesting (Native CSS)

### & (Nesting Selector)
**Definition:** Native CSS nesting without preprocessors.

**Example:**
```css
.card {
  padding: 20px;
  
  & .title {
    font-size: 24px;
    /* .card .title */
  }
  
  &:hover {
    transform: scale(1.05);
    /* .card:hover */
  }
  
  & > .content {
    margin-top: 10px;
    /* .card > .content */
  }
  
  @media (min-width: 768px) {
    & {
      padding: 40px;
    }
  }
}
```

---

## 🎯 View Transitions API

### view-transition-name
**Definition:** Names elements for smooth transitions between views.

**Example:**
```css
.hero {
  view-transition-name: hero-image;
}

/* Customize transition */
::view-transition-old(hero-image) {
  animation: fade-out 0.3s;
}

::view-transition-new(hero-image) {
  animation: fade-in 0.3s;
}
```

---

## 🎨 Advanced Tips & Tricks

### Custom Scrollbars
**Definition:** Style scrollbars (WebKit browsers).

**Example:**
```css
/* Webkit browsers (Chrome, Safari) */
::-webkit-scrollbar {
  width: 12px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1;
}

::-webkit-scrollbar-thumb {
  background: #888;
  border-radius: 6px;
}

::-webkit-scrollbar-thumb:hover {
  background: #555;
}

/* Firefox */
* {
  scrollbar-width: thin;
  scrollbar-color: #888 #f1f1f1;
}
```

---

### Text Selection Styling
**Definition:** Style selected text appearance.

**Example:**
```css
::selection {
  background-color: #ffeb3b;
  color: black;
  text-shadow: none;
}

::-moz-selection {
  background-color: #ffeb3b;
  color: black;
}

.special::selection {
  background-color: blue;
  color: white;
}
```

---

### Placeholder Styling
**Definition:** Style placeholder text in inputs.

**Example:**
```css
::placeholder {
  color: #999;
  opacity: 1;
  font-style: italic;
}

::-webkit-input-placeholder { /* Chrome/Opera/Safari */
  color: #999;
}

::-moz-placeholder { /* Firefox 19+ */
  color: #999;
}

:-ms-input-placeholder { /* IE 10-11 */
  color: #999;
}
```

---

### Truncate Text with Ellipsis
**Definition:** Show "..." for overflowing text.

**Example:**
```css
/* Single line */
.truncate {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

/* Multiple lines (WebKit) */
.truncate-multiline {
  display: -webkit-box;
  -webkit-line-clamp: 3; /* Number of lines */
  -webkit-box-orient: vertical;
  overflow: hidden;
}
```

---

### Center Element Perfectly
**Definition:** Various centering techniques.

**Example:**
```css
/* Flexbox centering */
.flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Grid centering */
.grid-center {
  display: grid;
  place-items: center;
}

/* Absolute centering */
.absolute-center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

/* Margin auto centering (block elements) */
.margin-center {
  width: 300px;
  margin: 0 auto;
}
```

---

### Aspect Ratio Box (Old Method)
**Definition:** Maintain aspect ratio before aspect-ratio property.

**Example:**
```css
/* Padding hack */
.aspect-ratio-box {
  position: relative;
  width: 100%;
  padding-bottom: 56.25%; /* 16:9 ratio */
}

.aspect-ratio-content {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

/* Modern way */
.modern-aspect {
  aspect-ratio: 16 / 9; /* Much simpler! */
}
```

---

### Glass Morphism Effect
**Definition:** Popular frosted glass design trend.

**Example:**
```css
.glass {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px) saturate(180%);
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.2);
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}

.glass-dark {
  background: rgba(0, 0, 0, 0.3);
  backdrop-filter: blur(15px);
  border: 1px solid rgba(255, 255, 255, 0.1);
}
```

---

### Neumorphism Effect
**Definition:** Soft UI design with subtle shadows.

**Example:**
```css
.neumorphism {
  background: #e0e0e0;
  border-radius: 20px;
  box-shadow: 
    20px 20px 60px #bebebe,
    -20px -20px 60px #ffffff;
}

.neumorphism-pressed {
  box-shadow: 
    inset 20px 20px 60px #bebebe,
    inset -20px -20px 60px #ffffff;
}
```

---

### Smooth Scrolling
**Definition:** Smooth page scrolling behavior.

**Example:**
```css
html {
  scroll-behavior: smooth;
}

/* Smooth scrolling for specific container */
.scroll-container {
  scroll-behavior: smooth;
  overflow-y: scroll;
}

/* Disable for reduced motion preference */
@media (prefers-reduced-motion: reduce) {
  html {
    scroll-behavior: auto;
  }
}
```

---

## 📱 Responsive Design Patterns

### Mobile-First Media Queries
**Definition:** Start with mobile, add complexity for larger screens.

**Example:**
```css
/* Base: Mobile styles */
.container {
  width: 100%;
  padding: 10px;
}

/* Tablet */
@media (min-width: 768px) {
  .container {
    width: 750px;
    padding: 20px;
  }
}

/* Desktop */
@media (min-width: 1024px) {
  .container {
    width: 1000px;
    padding: 30px;
  }
}

/* Large Desktop */
@media (min-width: 1200px) {
  .container {
    width: 1140px;
    padding: 40px;
  }
}
```

---

### Desktop-First Media Queries
**Definition:** Start with desktop, scale down for smaller screens.

**Example:**
```css
/* Base: Desktop styles */
.grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 40px;
}

/* Tablet */
@media (max-width: 1024px) {
  .grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
  }
}

/* Mobile */
@media (max-width: 768px) {
  .grid {
    grid-template-columns: 1fr;
    gap: 10px;
  }
}
```

---

### Common Breakpoints
**Definition:** Standard responsive breakpoints.

**Example:**
```css
/* Extra small devices (phones, less than 576px) */
@media (max-width: 575.98px) { }

/* Small devices (landscape phones, 576px and up) */
@media (min-width: 576px) { }

/* Medium devices (tablets, 768px and up) */
@media (min-width: 768px) { }

/* Large devices (desktops, 992px and up) */
@media (min-width: 992px) { }

/* Extra large devices (large desktops, 1200px and up) */
@media (min-width: 1200px) { }

/* Extra extra large devices (1400px and up) */
@media (min-width: 1400px) { }
```

---

### Orientation Queries
**Definition:** Styles based on device orientation.

**Example:**
```css
/* Portrait orientation */
@media (orientation: portrait) {
  .container {
    flex-direction: column;
  }
}

/* Landscape orientation */
@media (orientation: landscape) {
  .container {
    flex-direction: row;
  }
}

/* Combine with size */
@media (max-width: 768px) and (orientation: landscape) {
  .header {
    height: 60px; /* Shorter header in landscape */
  }
}
```

---

### Aspect Ratio Queries
**Definition:** Target specific aspect ratios.

**Example:**
```css
/* Widescreen */
@media (min-aspect-ratio: 16/9) {
  .video {
    width: 100%;
  }
}

/* Square or portrait */
@media (max-aspect-ratio: 1/1) {
  .sidebar {
    display: none;
  }
}
```

---

### Resolution Queries
**Definition:** Target high-DPI (Retina) displays.

**Example:**
```css
/* Standard resolution */
.logo {
  background-image: url('logo.png');
}

/* High DPI (Retina) */
@media (-webkit-min-device-pixel-ratio: 2),
       (min-resolution: 192dpi) {
  .logo {
    background-image: url('logo@2x.png');
    background-size: 200px 100px;
  }
}

/* Extra high DPI */
@media (-webkit-min-device-pixel-ratio: 3),
       (min-resolution: 288dpi) {
  .logo {
    background-image: url('logo@3x.png');
    background-size: 200px 100px;
  }
}
```

---

### Hover Capability Queries
**Definition:** Detect if device supports hover.

**Example:**
```css
/* Touch devices (no hover) */
@media (hover: none) {
  .button {
    /* Always show button state */
    background-color: blue;
  }
}

/* Devices with hover capability */
@media (hover: hover) {
  .button:hover {
    background-color: darkblue;
    transform: scale(1.05);
  }
}

/* Pointer precision */
@media (pointer: coarse) {
  /* Touch devices - make buttons bigger */
  .button {
    min-height: 44px;
    min-width: 44px;
  }
}

@media (pointer: fine) {
  /* Mouse/trackpad - can be smaller */
  .button {
    min-height: 32px;
  }
}
```

---

### Reduced Motion Queries
**Definition:** Respect user's motion preferences.

**Example:**
```css
/* Normal animations */
.element {
  transition: transform 0.3s ease;
}

.element:hover {
  transform: translateY(-10px);
}

/* Reduce or remove animations for users who prefer it */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
  
  .element:hover {
    transform: none; /* Remove transform */
  }
}
```

---

### Color Scheme Queries
**Definition:** Detect light/dark mode preference.

**Example:**
```css
/* Light mode (default) */
:root {
  --bg-color: white;
  --text-color: black;
}

body {
  background-color: var(--bg-color);
  color: var(--text-color);
}

/* Dark mode */
@media (prefers-color-scheme: dark) {
  :root {
    --bg-color: #1a1a1a;
    --text-color: #f0f0f0;
  }
  
  img {
    opacity: 0.8; /* Slightly dim images */
  }
}

/* No preference */
@media (prefers-color-scheme: no-preference) {
  /* Fallback styles */
}
```

---

### Contrast Queries
**Definition:** Detect contrast preference.

**Example:**
```css
/* High contrast */
@media (prefers-contrast: high) {
  .button {
    border: 3px solid black;
    font-weight: bold;
  }
}

/* Low contrast */
@media (prefers-contrast: low) {
  .card {
    box-shadow: none;
  }
}
```

---

## 🎨 Performance Optimization

### content-visibility
**Definition:** Skips rendering off-screen content.

**Example:**
```css
.article {
  content-visibility: auto;
  /* Browser skips rendering until needed */
  contain-intrinsic-size: 0 500px;
  /* Estimated size for layout */
}

.hidden {
  content-visibility: hidden;
  /* Similar to display: none but keeps state */
}

.visible {
  content-visibility: visible;
  /* Always render (default) */
}
```

---

### Hardware Acceleration
**Definition:** Use GPU for better performance.

**Example:**
```css
.accelerated {
  transform: translateZ(0);
  /* Forces GPU acceleration */
}

.smooth-animation {
  will-change: transform, opacity;
  /* Hint browser to optimize */
}

/* Remove will-change after animation */
.smooth-animation.done {
  will-change: auto;
}

/* Only animate transform and opacity for best performance */
.performant {
  transition: transform 0.3s, opacity 0.3s;
}
```

---

### Font Loading Strategies
**Definition:** Control font display during loading.

**Example:**
```css
@font-face {
  font-family: 'CustomFont';
  src: url('font.woff2') format('woff2');
  font-display: swap;
  /* Shows fallback font immediately, swaps when loaded */
}

/* Options */
@font-face {
  font-display: block;
  /* Invisible text while loading (up to 3s) */
}

@font-face {
  font-display: fallback;
  /* Extremely short block period */
}

@font-face {
  font-display: optional;
  /* Use cached font or skip */
}

@font-face {
  font-display: auto;
  /* Browser decides */
}
```

---

## 🎯 CSS Hacks & Browser-Specific

### Browser-Specific Selectors
**Definition:** Target specific browsers (use sparingly).

**Example:**
```css
/* IE 10-11 only */
@media all and (-ms-high-contrast: none), (-ms-high-contrast: active) {
  .element {
    /* IE-specific styles */
  }
}

/* Edge only (old Edge) */
@supports (-ms-ime-align: auto) {
  .element {
    /* Edge-specific styles */
  }
}

/* Firefox only */
@-moz-document url-prefix() {
  .element {
    /* Firefox-specific styles */
  }
}

/* Safari only */
@media not all and (min-resolution:.001dpcm) {
  @supports (-webkit-appearance:none) {
    .element {
      /* Safari-specific styles */
    }
  }
}

/* Chrome only */
@media screen and (-webkit-min-device-pixel-ratio:0) 
  and (min-resolution:.001dpcm) {
  .element {
    /* Chrome-specific styles */
  }
}
```

---

### Feature Detection with @supports
**Definition:** Test if browser supports CSS features.

**Example:**
```css
/* Check if browser supports grid */
@supports (display: grid) {
  .container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }
}

/* Fallback for browsers without grid */
@supports not (display: grid) {
  .container {
    display: flex;
  }
}

/* Check multiple features */
@supports (display: grid) and (gap: 20px) {
  .modern-grid {
    display: grid;
    gap: 20px;
  }
}

/* Check if any feature is supported */
@supports (display: -webkit-box) or (display: flex) {
  .flexible {
    display: flex;
  }
}

/* Selector support */
@supports selector(:has(*)) {
  .parent:has(.child) {
    /* Use :has() if supported */
  }
}
```

---

## 🎨 Print Styles

### @media print
**Definition:** Styles specifically for printing.

**Example:**
```css
@media print {
  /* Hide non-essential elements */
  nav, footer, .sidebar, .ads {
    display: none;
  }
  
  /* Reset colors for printing */
  body {
    background: white;
    color: black;
    font-size: 12pt;
  }
  
  /* Ensure links are visible */
  a {
    color: black;
    text-decoration: underline;
  }
  
  /* Show link URLs */
  a[href]::after {
    content: " (" attr(href) ")";
  }
  
  /* Prevent page breaks inside elements */
  h1, h2, h3, h4, h5, h6 {
    page-break-after: avoid;
    break-after: avoid;
  }
  
  /* Prevent orphans and widows */
  p {
    orphans: 3;
    widows: 3;
  }
  
  /* Force page breaks */
  .chapter {
    page-break-before: always;
    break-before: page;
  }
}
```

---

## 🎯 Accessibility Improvements

### Focus Styles
**Definition:** Clear focus indicators for keyboard navigation.

**Example:**
```css
/* Always maintain focus styles */
:focus {
  outline: 2px solid blue;
  outline-offset: 2px;
}

/* Better focus for buttons */
button:focus-visible {
  outline: 3px solid #0066ff;
  outline-offset: 3px;
}

/* Focus within containers */
.card:focus-within {
  box-shadow: 0 0 0 3px rgba(0, 100, 255, 0.3);
}

/* High contrast mode */
@media (prefers-contrast: high) {
  :focus {
    outline: 3px solid;
    outline-offset: 3px;
  }
}
```

---

### Screen Reader Only Content
**Definition:** Hide visually but keep for screen readers.

**Example:**
```css
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}

/* Show on focus (skip links) */
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  overflow: visible;
  clip: auto;
  white-space: normal;
}
```

---

### Minimum Touch Target Size
**Definition:** Ensure interactive elements are large enough.

**Example:**
```css
/* Minimum 44x44px for touch targets */
button, a, input, select {
  min-height: 44px;
  min-width: 44px;
}

/* Or use padding */
.touch-target {
  padding: 12px 16px;
}

/* On mobile */
@media (max-width: 768px) {
  button {
    min-height: 48px;
    min-width: 48px;
  }
}
```

---

### Color Contrast
**Definition:** Ensure sufficient color contrast.

**Example:**
```css
/* Good contrast ratio (4.5:1 for normal text) */
.good-contrast {
  background-color: #ffffff;
  color: #333333;
}

/* Use tools to check contrast:
   - WCAG AA: 4.5:1 for normal text, 3:1 for large text
   - WCAG AAA: 7:1 for normal text, 4.5:1 for large text
*/

.accessible-button {
  background-color: #0066cc;
  color: #ffffff; /* Passes WCAG AA */
}

/* Don't rely on color alone */
.error {
  color: red;
  border-left: 4px solid red; /* Additional indicator */
}

.error::before {
  content: "⚠ "; /* Icon indicator */
}
```

---

## 🎨 Dark Mode Implementation

### CSS Variable Approach
**Definition:** Use CSS variables for theme switching.

**Example:**
```css
/* Light theme (default) */
:root {
  --bg-primary: #ffffff;
  --bg-secondary: #f5f5f5;
  --text-primary: #333333;
  --text-secondary: #666666;
  --border-color: #dddddd;
  --shadow: rgba(0, 0, 0, 0.1);
}

/* Dark theme */
[data-theme="dark"] {
  --bg-primary: #1a1a1a;
  --bg-secondary: #2d2d2d;
  --text-primary: #f0f0f0;
  --text-secondary: #b0b0b0;
  --border-color: #404040;
  --shadow: rgba(0, 0, 0, 0.5);
}

/* Auto dark mode */
@media (prefers-color-scheme: dark) {
  :root {
    --bg-primary: #1a1a1a;
    --bg-secondary: #2d2d2d;
    --text-primary: #f0f0f0;
    --text-secondary: #b0b0b0;
    --border-color: #404040;
    --shadow: rgba(0, 0, 0, 0.5);
  }
}

/* Apply variables */
body {
  background-color: var(--bg-primary);
  color: var(--text-primary);
}

.card {
  background-color: var(--bg-secondary);
  border: 1px solid var(--border-color);
  box-shadow: 0 2px 8px var(--shadow);
}
```

---

### Class-Based Dark Mode
**Definition:** Toggle dark mode with body class.

**Example:**
```css
/* Light mode */
body {
  background-color: white;
  color: black;
}

/* Dark mode */
body.dark-mode {
  background-color: #1a1a1a;
  color: #f0f0f0;
}

body.dark-mode .card {
  background-color: #2d2d2d;
  border-color: #404040;
}

body.dark-mode a {
  color: #4da6ff;
}

body.dark-mode img {
  opacity: 0.9;
  filter: brightness(0.9);
}
```

---

## 🎯 Animation Best Practices

### Performant Animations
**Definition:** Animate only transform and opacity.

**Example:**
```css
/* ✅ Good - GPU accelerated */
.good-animation {
  transition: transform 0.3s, opacity 0.3s;
}

.good-animation:hover {
  transform: translateY(-5px) scale(1.05);
  opacity: 0.9;
}

/* ❌ Bad - causes reflows */
.bad-animation {
  transition: width 0.3s, height 0.3s, top 0.3s;
}

/* Use transform instead of position */
.move-element {
  transform: translate(50px, 100px); /* ✅ */
  /* Instead of: left: 50px; top: 100px; ❌ */
}

/* Use transform instead of width/height */
.scale-element {
  transform: scale(1.5); /* ✅ */
  /* Instead of: width: 150%; height: 150%; ❌ */
}
```

---

### Stagger Animations
**Definition:** Delay animations for multiple elements.

**Example:**
```css
.list-item {
  opacity: 0;
  animation: fadeIn 0.5s forwards;
}

.list-item:nth-child(1) { animation-delay: 0.1s; }
.list-item:nth-child(2) { animation-delay: 0.2s; }
.list-item:nth-child(3) { animation-delay: 0.3s; }
.list-item:nth-child(4) { animation-delay: 0.4s; }
.list-item:nth-child(5) { animation-delay: 0.5s; }

/* Or with calc */
.grid-item {
  animation: slideIn 0.5s ease-out backwards;
  animation-delay: calc(var(--index) * 0.1s);
}

@keyframes fadeIn {
  to { opacity: 1; }
}

@keyframes slideIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
```

---

### Loading Animations
**Definition:** Common loading spinner patterns.

**Example:**
```css
/* Spinner */
.spinner {
  width: 40px;
  height: 40px;
  border: 4px solid #f3f3f3;
  border-top: 4px solid #3498db;
  border-radius: 50%;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

/* Pulse */
.pulse {
  width: 40px;
  height: 40px;
  background: #3498db;
  border-radius: 50%;
  animation: pulse 1.5s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(1.3);
    opacity: 0.5;
  }
}

/* Skeleton loader */
.skeleton {
  background: linear-gradient(
    90deg,
    #f0f0f0 25%,
    #e0e0e0 50%,
    #f0f0f0 75%
  );
  background-size: 200% 100%;
  animation: loading 1.5s infinite;
}

@keyframes loading {
  to { background-position: -200% 0; }
}

/* Dots */
.dots {
  display: flex;
  gap: 8px;
}

.dot {
  width: 10px;
  height: 10px;
  background: #3498db;
  border-radius: 50%;
  animation: bounce 1.4s infinite ease-in-out both;
}

.dot:nth-child(1) { animation-delay: -0.32s; }
.dot:nth-child(2) { animation-delay: -0.16s; }

@keyframes bounce {
  0%, 80%, 100% {
    transform: scale(0);
  }
  40% {
    transform: scale(1);
  }
}
```

---

## 🎨 Utility Classes (Inspired by Tailwind)

### Common Utility Patterns
**Definition:** Reusable single-purpose classes.

**Example:**
```css
/* Display */
.block { display: block; }
.inline-block { display: inline-block; }
.inline { display: inline; }
.flex { display: flex; }
.inline-flex { display: inline-flex; }
.grid { display: grid; }
.hidden { display: none; }

/* Flexbox */
.flex-row { flex-direction: row; }
.flex-col { flex-direction: column; }
.flex-wrap { flex-wrap: wrap; }
.items-center { align-items: center; }
.items-start { align-items: flex-start; }
.items-end { align-items: flex-end; }
.justify-center { justify-content: center; }
.justify-between { justify-content: space-between; }
.justify-around { justify-content: space-around; }

/* Spacing */
.m-0 { margin: 0; }
.m-1 { margin: 0.25rem; }
.m-2 { margin: 0.5rem; }
.m-4 { margin: 1rem; }
.m-8 { margin: 2rem; }

.p-0 { padding: 0; }
.p-1 { padding: 0.25rem; }
.p-2 { padding: 0.5rem; }
.p-4 { padding: 1rem; }
.p-8 { padding: 2rem; }

/* Text */
.text-left { text-align: left; }
.text-center { text-align: center; }
.text-right { text-align: right; }
.text-sm { font-size: 0.875rem; }
.text-base { font-size: 1rem; }
.text-lg { font-size: 1.125rem; }
.text-xl { font-size: 1.25rem; }
.text-2xl { font-size: 1.5rem; }
.font-bold { font-weight: bold; }
.font-normal { font-weight: normal; }
.uppercase { text-transform: uppercase; }
.lowercase { text-transform: lowercase; }
.capitalize { text-transform: capitalize; }

/* Colors */
.text-white { color: white; }
.text-black { color: black; }
.text-gray { color: #666; }
.bg-white { background-color: white; }
.bg-black { background-color: black; }
.bg-gray { background-color: #f5f5f5; }

/* Borders */
.border { border: 1px solid #ddd; }
.border-0 { border: 0; }
.border-t { border-top: 1px solid #ddd; }
.border-r { border-right: 1px solid #ddd; }
.border-b { border-bottom: 1px solid #ddd; }
.border-l { border-left: 1px solid #ddd; }
.rounded { border-radius: 0.25rem; }
.rounded-lg { border-radius: 0.5rem; }
.rounded-full { border-radius: 9999px; }

/* Width & Height */
.w-full { width: 100%; }
.w-1\/2 { width: 50%; }
.w-1\/3 { width: 33.333%; }
.w-1\/4 { width: 25%; }
.h-full { height: 100%; }
.h-screen { height: 100vh; }

/* Position */
.relative { position: relative; }
.absolute { position: absolute; }
.fixed { position: fixed; }
.sticky { position: sticky; }

/* Shadow */
.shadow-sm { box-shadow: 0 1px 2px rgba(0,0,0,0.05); }
.shadow { box-shadow: 0 2px 4px rgba(0,0,0,0.1); }
.shadow-lg { box-shadow: 0 4px 8px rgba(0,0,0,0.15); }
```

---

## 🎯 CSS Reset / Normalize

### Modern CSS Reset
**Definition:** Remove browser inconsistencies.

**Example:**
```css
/* Box sizing */
*, *::before, *::after {
  box-sizing: border-box;
}

/* Remove default margin */
* {
  margin: 0;
}

/* Body setup */
body {
  line-height: 1.5;
  -webkit-font-smoothing: antialiased;
}

/* Media defaults */
img, picture, video, canvas, svg {
  display: block;
  max-width: 100%;
}

/* Form elements */
input, button, textarea, select {
  font: inherit;
}

/* Remove button styling */
button {
  background: none;
  border: none;
  padding: 0;
  cursor: pointer;
}

/* Text overflow */
p, h1, h2, h3, h4, h5, h6 {
  overflow-wrap: break-word;
}

/* Root stacking context */
#root, #__next {
  isolation: isolate;
}

/* Remove list styles */
ul, ol {
  list-style: none;
  padding: 0;
}

/* Remove link styles */
a {
  text-decoration: none;
  color: inherit;
}
```

---

## 🎨 Final Pro Tips

### CSS Organization
**Definition:** Structure your CSS for maintainability.

**Example:**
```css
/* 1. CSS Variables */
:root {
  --primary: #3498db;
  --secondary: #2ecc71;
}

/* 2. Reset/Normalize */
* { margin: 0; padding: 0; box-sizing: border-box; }

/* 3. Base styles */
body { font-family: Arial, sans-serif; }

/* 4. Layout */
.container { max-width: 1200px; margin: 0 auto; }

/* 5. Components */
.button { /* ... */ }
.card { /* ... */ }

/* 6. Utilities */
.text-center { text-align: center; }

/* 7. Media queries */
@media (max-width: 768px) { /* ... */ }
```

---

### Naming Conventions (BEM)
**Definition:** Block Element Modifier methodology.

**Example:**
```css
/* Block */
.card { }

/* Element */
.card__title { }
.card__body { }
.card__footer { }

/* Modifier */
.card--featured { }
.card--large { }

/* Combined */
.card__title--highlighted { }

/* Example usage in HTML:
<div class="card card--featured">
  <h2 class="card__title card__title--highlighted">Title</h2>
  <div class="card__body">Content</div>
  <div class="card__footer">Footer</div>
</div>
*/
```

---

### CSS Comments
**Definition:** Document your code effectively.

**Example:**
```css
/* ==========================================================================
   Section comment block
   ========================================================================== */

/* Sub-section comment block
   ========================================================================== */

/**
 * Short description using Doxygen-style comment format
 *
 * Long description with more details about what this
 * CSS does and why it's needed.
 *
 * @tag This is a tag named 'tag'
 */

/* Basic comment */

.selector {
  /* TODO: Fix this later */
  /* HACK: Workaround for IE bug */
  /* NOTE: Important information */
}
```

---

## 📚 Learning Resources

### Practice Exercises
1. **Build a responsive navigation menu** (Flexbox/Grid)
2. **Create a card component** (Box model, shadows)
3. **Make an image gallery** (Grid, transitions)
4. **Design a landing page** (Positioning, backgrounds)
5. **Animate a loading spinner** (Keyframes, transforms)
6. **Implement dark mode** (CSS variables, media queries)
7. **Style a form** (Pseudo-classes, transitions)
8. **Create a timeline** (Positioning, pseudo-elements)

---

### Key Takeaways

✅ **Understand the Box Model**: margin, border, padding, content  
✅ **Master Flexbox & Grid**: Modern layout systems  
✅ **Learn Positioning**: relative, absolute, fixed, sticky  
✅ **Use CSS Variables**: Maintainable, themeable code  
✅ **Think Responsive**: Mobile-first approach  
✅ **Optimize Performance**: Transform & opacity only  
✅ **Ensure Accessibility**: Focus states, contrast, screen readers  
✅ **Keep Learning**: CSS is always evolving!

---

## 🎯 CSS Cheat Sheet Summary

This comprehensive cheat sheet covers:

- ✅ **300+ CSS properties** with clear explanations
- ✅ **Selectors** (element, class, ID, pseudo, attribute)
- ✅ **Layout Systems** (Flexbox, Grid, positioning)
- ✅ **Colors & Backgrounds** (gradients, images, filters)
- ✅ **Typography** (fonts, text effects, line-height)
- ✅ **Box Model** (margin, padding, border, sizing)
- ✅ **Transforms & Animations** (2D, 3D, keyframes)
- ✅ **Responsive Design** (media queries, viewport units)
- ✅ **Modern CSS** (container queries, layers, nesting)
- ✅ **Performance** (hardware acceleration, content-visibility)
- ✅ **Accessibility** (focus states, contrast, screen readers)
- ✅ **Dark Mode** (CSS variables, prefers-color-scheme)
- ✅ **Best Practices** (naming, organization, comments)

---
