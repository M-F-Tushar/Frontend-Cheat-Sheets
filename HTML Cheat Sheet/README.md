# 📚 HTML Cheat Sheet - Complete Guide

## 🏗️ Document Structure

### `<html></html>`
**Definition:** The root element that wraps all HTML content.

**Explanation:** This is the container for your entire webpage. Everything goes inside these tags.

**Example:**
```html
<html>
  <!-- All your content goes here -->
</html>
```

---

### `<head></head>`
**Definition:** Contains metadata and information about the document.

**Explanation:** This section holds invisible information like the title, links to stylesheets, and other data that browsers need but don't display on the page.

**Example:**
```html
<head>
  <title>My Website</title>
</head>
```

---

### `<body></body>`
**Definition:** Contains all visible content on the webpage.

**Explanation:** Everything users see (text, images, links, etc.) goes inside the body tags.

**Example:**
```html
<body>
  <h1>Welcome to my website!</h1>
  <p>This is visible content.</p>
</body>
```

---

### `<title></title>`
**Definition:** Sets the page title shown in the browser tab.

**Explanation:** This appears in your browser tab and is what shows up when you bookmark a page or see it in search results.

**Example:**
```html
<title>My Amazing Blog</title>
```

---

## 📝 Text Formatting Tags

### `<h1>` to `<h6>`
**Definition:** Create headings of different sizes.

**Explanation:** `<h1>` is the largest/most important heading, `<h6>` is the smallest. Use them to organize content hierarchy.

**Example:**
```html
<h1>Main Title</h1>
<h2>Section Title</h2>
<h3>Subsection Title</h3>
```

---

### `<p></p>`
**Definition:** Creates a paragraph of text.

**Explanation:** Use this for regular text blocks. Browsers automatically add space above and below paragraphs.

**Example:**
```html
<p>This is a paragraph with some text in it.</p>
<p>This is another paragraph.</p>
```

---

### `<strong></strong>`
**Definition:** Makes text bold and emphasizes importance.

**Explanation:** Use this for text that's really important. It makes text bold and tells screen readers it's significant.

**Example:**
```html
<p>This is <strong>very important</strong> information.</p>
```

---

### `<em></em>`
**Definition:** Emphasizes text with italics.

**Explanation:** Use this to stress certain words. It italicizes text and signals emphasis to screen readers.

**Example:**
```html
<p>I <em>really</em> love pizza!</p>
```

---

### `<br>`
**Definition:** Inserts a line break.

**Explanation:** Forces text to start on a new line without creating a new paragraph. It's a self-closing tag (no `</br>` needed).

**Example:**
```html
<p>First line<br>Second line</p>
```

---

### `<code></code>`
**Definition:** Displays text as code.

**Explanation:** Shows text in a monospace font, typically used for displaying programming code inline.

**Example:**
```html
<p>Use the <code>print()</code> function in Python.</p>
```

---

### `<pre></pre>`
**Definition:** Preserves formatting (spaces and line breaks).

**Explanation:** Text inside keeps all spaces, tabs, and line breaks exactly as you type them.

**Example:**
```html
<pre>
This    preserves
  all   spacing
    and line breaks
</pre>
```

---

## 🔗 Links

### `<a href="URL"></a>`
**Definition:** Creates a clickable hyperlink.

**Explanation:** The `href` attribute specifies where the link goes. Text between the tags is what users click.

**Example:**
```html
<a href="https://google.com">Visit Google</a>
```

---

### Email Links
**Definition:** Creates a link that opens the user's email client.

**Explanation:** Use `mailto:` followed by an email address to create an email link.

**Example:**
```html
<a href="mailto:hello@example.com">Send us an email</a>
```

---

### Anchor Links
**Definition:** Links to a specific section on the same page.

**Explanation:** Create a target with `name` or `id`, then link to it with `#` followed by that name.

**Example:**
```html
<a href="#contact">Jump to Contact Section</a>
<!-- Later on the page -->
<h2 id="contact">Contact Us</h2>
```

---

## 🖼️ Images

### `<img>`
**Definition:** Embeds an image in the page.

**Explanation:** A self-closing tag that displays images. The `src` attribute tells where to find the image, and `alt` provides text description.

**Example:**
```html
<img src="photo.jpg" alt="A beautiful sunset">
```

---

### Image with Size
**Definition:** Sets specific dimensions for an image.

**Explanation:** Control image size with `width` and `height` attributes (in pixels).

**Example:**
```html
<img src="logo.png" alt="Company Logo" width="200" height="100">
```

---

## 📋 Lists

### `<ul></ul>` - Unordered List
**Definition:** Creates a bulleted list.

**Explanation:** Use for items where order doesn't matter. Each item uses `<li>` tags.

**Example:**
```html
<ul>
  <li>Apples</li>
  <li>Bananas</li>
  <li>Oranges</li>
</ul>
```

---

### `<ol></ol>` - Ordered List
**Definition:** Creates a numbered list.

**Explanation:** Use for items in a specific order. Browsers automatically number each `<li>` item.

**Example:**
```html
<ol>
  <li>Wake up</li>
  <li>Brush teeth</li>
  <li>Eat breakfast</li>
</ol>
```

---

### `<dl></dl>` - Definition List
**Definition:** Creates a list of terms and definitions.

**Explanation:** Use `<dt>` for the term and `<dd>` for the definition. Great for glossaries.

**Example:**
```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
</dl>
```

---

## 📦 Containers & Layout

### `<div></div>`
**Definition:** A generic container for grouping content.

**Explanation:** Use to organize and style sections of your page. It's a block-level element (starts on new line).

**Example:**
```html
<div>
  <h2>Section Title</h2>
  <p>Section content goes here.</p>
</div>
```

---

### `<span></span>`
**Definition:** A generic inline container.

**Explanation:** Like `<div>` but inline (doesn't break to new line). Use for styling parts of text.

**Example:**
```html
<p>This is <span style="color: red;">red text</span> in a paragraph.</p>
```

---

### `<blockquote></blockquote>`
**Definition:** Indicates a quotation from another source.

**Explanation:** Indents text from both sides. Use for longer quotes.

**Example:**
```html
<blockquote>
  "The only way to do great work is to love what you do." - Steve Jobs
</blockquote>
```

---

## 📊 Tables

### Basic Table Structure
**Definition:** Organizes data in rows and columns.

**Explanation:** `<table>` creates the table, `<tr>` makes rows, `<td>` makes cells, and `<th>` makes header cells.

**Example:**
```html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>John</td>
    <td>25</td>
  </tr>
  <tr>
    <td>Sarah</td>
    <td>28</td>
  </tr>
</table>
```

---

### Table with Border
**Definition:** Adds visible borders to table cells.

**Explanation:** The `border` attribute sets border thickness. Use CSS for modern styling.

**Example:**
```html
<table border="1">
  <tr>
    <td>Cell 1</td>
    <td>Cell 2</td>
  </tr>
</table>
```

---

### Spanning Cells
**Definition:** Makes a cell span multiple rows or columns.

**Explanation:** Use `colspan` to span columns, `rowspan` to span rows.

**Example:**
```html
<table border="1">
  <tr>
    <td colspan="2">Spans 2 columns</td>
  </tr>
  <tr>
    <td>Cell 1</td>
    <td>Cell 2</td>
  </tr>
</table>
```

---

## 📝 Forms

### `<form></form>`
**Definition:** Creates a form for user input.

**Explanation:** Container for all form elements. Usually has `action` (where to send data) and `method` (how to send it) attributes.

**Example:**
```html
<form action="/submit" method="post">
  <!-- Form elements go here -->
</form>
```

---

### `<input type="text">`
**Definition:** Creates a single-line text input field.

**Explanation:** The `name` attribute identifies the field when submitted. `size` controls visible width.

**Example:**
```html
<input type="text" name="username" placeholder="Enter your name">
```

---

### `<input type="email">`
**Definition:** Creates an email input field.

**Explanation:** Validates that input is a proper email format. Mobile keyboards show email-specific layout.

**Example:**
```html
<input type="email" name="email" placeholder="your@email.com">
```

---

### `<input type="password">`
**Definition:** Creates a password input field.

**Explanation:** Hides typed characters with dots or asterisks for security.

**Example:**
```html
<input type="password" name="password" placeholder="Enter password">
```

---

### `<input type="checkbox">`
**Definition:** Creates a checkbox for yes/no options.

**Explanation:** Users can check or uncheck it. Use `checked` to make it selected by default.

**Example:**
```html
<input type="checkbox" name="subscribe" checked>
<label>Subscribe to newsletter</label>
```

---

### `<input type="radio">`
**Definition:** Creates radio buttons (select one option).

**Explanation:** Give the same `name` to group buttons so only one can be selected at a time.

**Example:**
```html
<input type="radio" name="size" value="small"> Small
<input type="radio" name="size" value="large"> Large
```

---

### `<textarea></textarea>`
**Definition:** Creates a multi-line text input area.

**Explanation:** Use `rows` and `cols` to set size, or use CSS for better control.

**Example:**
```html
<textarea name="message" rows="4" cols="50">
Enter your message here...
</textarea>
```

---

### `<select></select>`
**Definition:** Creates a dropdown menu.

**Explanation:** Each option inside uses `<option>` tags. The `value` attribute defines what gets submitted.

**Example:**
```html
<select name="country">
  <option value="us">United States</option>
  <option value="uk">United Kingdom</option>
  <option value="ca">Canada</option>
</select>
```

---

### `<button>` or `<input type="submit">`
**Definition:** Creates a submit button.

**Explanation:** Clicking this sends form data to the server specified in the form's `action` attribute.

**Example:**
```html
<button type="submit">Send Form</button>
<!-- or -->
<input type="submit" value="Submit">
```

---

## 🎨 Semantic HTML5 Elements

### `<header></header>`
**Definition:** Represents introductory content or navigation.

**Explanation:** Typically contains logo, site title, and main navigation. Better for SEO and accessibility than `<div>`.

**Example:**
```html
<header>
  <h1>My Website</h1>
  <nav><!-- navigation links --></nav>
</header>
```

---

### `<nav></nav>`
**Definition:** Contains navigation links.

**Explanation:** Use for menus and navigation sections. Helps screen readers identify navigation areas.

**Example:**
```html
<nav>
  <a href="/">Home</a>
  <a href="/about">About</a>
  <a href="/contact">Contact</a>
</nav>
```

---

### `<main></main>`
**Definition:** Contains the main content of the page.

**Explanation:** Use once per page for the primary content. Excludes headers, footers, and sidebars.

**Example:**
```html
<main>
  <article>
    <h1>Article Title</h1>
    <p>Main content goes here...</p>
  </article>
</main>
```

---

### `<article></article>`
**Definition:** Represents self-contained content.

**Explanation:** Use for blog posts, news articles, or any content that makes sense on its own.

**Example:**
```html
<article>
  <h2>10 Tips for Better HTML</h2>
  <p>Here are some great tips...</p>
</article>
```

---

### `<section></section>`
**Definition:** Represents a thematic grouping of content.

**Explanation:** Use to divide content into meaningful sections. Usually has a heading.

**Example:**
```html
<section>
  <h2>About Us</h2>
  <p>We are a company that...</p>
</section>
```

---

### `<footer></footer>`
**Definition:** Represents footer content.

**Explanation:** Typically contains copyright, links, contact info. Can be used for page or section footers.

**Example:**
```html
<footer>
  <p>&copy; 2024 My Company. All rights reserved.</p>
</footer>
```

---

## 🔧 Other Useful Tags

### `<hr>`
**Definition:** Creates a horizontal line (thematic break).

**Explanation:** Self-closing tag that adds a line across the page. Use to separate content sections.

**Example:**
```html
<p>First section</p>
<hr>
<p>Second section</p>
```

---

### Comments
**Definition:** Adds notes in code that aren't displayed.

**Explanation:** Use to leave notes for yourself or other developers. Browsers ignore everything between `<!--` and `-->`.

**Example:**
```html
<!-- This is a comment that won't show on the page -->
<p>This text will show</p>
```

---

## 💡 Quick Tips

1. **Always close your tags** (except self-closing ones like `<br>`, `<img>`, `<hr>`)
2. **Use semantic HTML** (like `<header>`, `<nav>`) instead of just `<div>` everywhere
3. **Add `alt` text to images** for accessibility
4. **Indent your code** to make it easier to read
5. **Use lowercase** for tag names and attributes
6. **Validate your HTML** at validator.w3.org

---

## 📱 HTML5 Modern Input Types

### `<input type="date">`
**Definition:** Creates a date picker.

**Example:**
```html
<input type="date" name="birthday">
```

### `<input type="color">`
**Definition:** Creates a color picker.

**Example:**
```html
<input type="color" name="favcolor">
```

### `<input type="range">`
**Definition:** Creates a slider control.

**Example:**
```html
<input type="range" name="volume" min="0" max="100">
```

### `<input type="number">`
**Definition:** Creates a numeric input field.

**Example:**
```html
<input type="number" name="quantity" min="1" max="10">
```

---

## 🎯 Basic HTML Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Page Title</title>
</head>
<body>
  <header>
    <h1>Welcome to My Website</h1>
  </header>
  
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
  </nav>
  
  <main>
    <section>
      <h2>Main Content</h2>
      <p>Your content goes here.</p>
    </section>
  </main>
  
  <footer>
    <p>&copy; 2024 My Website</p>
  </footer>
</body>
</html>
```

---

## 🎬 Media Elements

### `<video></video>`
**Definition:** Embeds a video player.

**Explanation:** Allows you to play video files directly in the browser. Use `controls` to show play/pause buttons.

**Example:**
```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  Your browser doesn't support video.
</video>
```

---

### `<audio></audio>`
**Definition:** Embeds an audio player.

**Explanation:** Plays audio files like music or podcasts. Add `controls` to show play buttons.

**Example:**
```html
<audio controls>
  <source src="song.mp3" type="audio/mpeg">
  Your browser doesn't support audio.
</audio>
```

---

### `<iframe></iframe>`
**Definition:** Embeds another webpage inside your page.

**Explanation:** Used to embed maps, videos from YouTube, or other websites within your page.

**Example:**
```html
<iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" 
        width="560" height="315">
</iframe>
```

---

### `<canvas></canvas>`
**Definition:** Creates a drawing area for graphics.

**Explanation:** Use JavaScript to draw shapes, graphs, animations, or games on this element.

**Example:**
```html
<canvas id="myCanvas" width="200" height="100">
  Your browser doesn't support canvas.
</canvas>
```

---

### `<svg></svg>`
**Definition:** Embeds scalable vector graphics.

**Explanation:** Creates graphics using code. Images scale perfectly at any size.

**Example:**
```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" fill="blue" />
</svg>
```

---

## 📑 More Semantic Elements

### `<aside></aside>`
**Definition:** Content tangentially related to main content.

**Explanation:** Use for sidebars, pull quotes, or content that's related but not central to the main topic.

**Example:**
```html
<aside>
  <h3>Did You Know?</h3>
  <p>Interesting fact related to the article...</p>
</aside>
```

---

### `<figure></figure>` & `<figcaption></figcaption>`
**Definition:** Groups media content with its caption.

**Explanation:** Wraps images, diagrams, or code with a caption. Better than just using `<img>` alone.

**Example:**
```html
<figure>
  <img src="chart.png" alt="Sales Chart">
  <figcaption>Q4 Sales Performance 2024</figcaption>
</figure>
```

---

### `<mark></mark>`
**Definition:** Highlights text.

**Explanation:** Shows text with a yellow background (by default) to draw attention, like a highlighter pen.

**Example:**
```html
<p>Please review the <mark>important changes</mark> in section 3.</p>
```

---

### `<time></time>`
**Definition:** Represents a specific time or date.

**Explanation:** Helps search engines and screen readers understand dates. Use `datetime` attribute for machine-readable format.

**Example:**
```html
<p>The event is on <time datetime="2024-12-25">Christmas Day</time>.</p>
```

---

### `<details></details>` & `<summary></summary>`
**Definition:** Creates an expandable/collapsible section.

**Explanation:** User can click to reveal hidden content. Great for FAQs or toggleable information.

**Example:**
```html
<details>
  <summary>Click to see more</summary>
  <p>Here's the hidden content that appears when clicked!</p>
</details>
```

---

### `<progress></progress>`
**Definition:** Displays a progress bar.

**Explanation:** Shows task completion visually. Use `value` for current progress and `max` for total.

**Example:**
```html
<progress value="70" max="100">70%</progress>
```

---

### `<meter></meter>`
**Definition:** Displays a measurement within a range.

**Explanation:** Like a gauge or thermometer. Shows how much of something (disk space, score, etc.).

**Example:**
```html
<meter value="6" min="0" max="10">6 out of 10</meter>
```

---

## 📝 More Text Formatting

### `<small></small>`
**Definition:** Makes text smaller (fine print).

**Explanation:** Use for side comments, legal text, or copyright notices.

**Example:**
```html
<p>Price: $99 <small>(plus tax)</small></p>
```

---

### `<del></del>` & `<ins></ins>`
**Definition:** Shows deleted and inserted text.

**Explanation:** `<del>` shows strikethrough text (removed), `<ins>` shows underlined text (added).

**Example:**
```html
<p>Price: <del>$100</del> <ins>$80</ins> (Sale!)</p>
```

---

### `<sub></sub>` & `<sup></sup>`
**Definition:** Creates subscript and superscript text.

**Explanation:** `<sub>` lowers text (like in H₂O), `<sup>` raises it (like in x²).

**Example:**
```html
<p>Water is H<sub>2</sub>O</p>
<p>E = mc<sup>2</sup></p>
```

---

### `<abbr></abbr>`
**Definition:** Marks an abbreviation or acronym.

**Explanation:** Use `title` attribute to show full meaning on hover.

**Example:**
```html
<p><abbr title="HyperText Markup Language">HTML</abbr> is fun!</p>
```

---

### `<q></q>`
**Definition:** Short inline quotation.

**Explanation:** Automatically adds quotation marks around text. For shorter quotes within text.

**Example:**
```html
<p>He said, <q>I love coding!</q> and continued working.</p>
```

---

### `<kbd></kbd>`
**Definition:** Represents keyboard input.

**Explanation:** Shows text as if it's a key to press. Often styled like a button.

**Example:**
```html
<p>Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.</p>
```

---

### `<samp></samp>`
**Definition:** Represents sample output from a program.

**Explanation:** Used to show computer/program output, usually in monospace font.

**Example:**
```html
<p>The program returned: <samp>Error 404</samp></p>
```

---

### `<var></var>`
**Definition:** Represents a variable in math or programming.

**Explanation:** Typically shown in italics. Use for variable names in explanations.

**Example:**
```html
<p>The formula is <var>x</var> + <var>y</var> = 10</p>
```

---

## 🔤 More Form Elements

### `<label></label>`
**Definition:** Creates a label for form inputs.

**Explanation:** Associates text with an input. Clicking the label focuses the input. Important for accessibility.

**Example:**
```html
<label for="username">Username:</label>
<input type="text" id="username" name="username">
```

---

### `<fieldset></fieldset>` & `<legend></legend>`
**Definition:** Groups related form elements.

**Explanation:** `<fieldset>` draws a box around inputs, `<legend>` adds a title to the box.

**Example:**
```html
<fieldset>
  <legend>Personal Information</legend>
  <label>Name: <input type="text"></label>
  <label>Email: <input type="email"></label>
</fieldset>
```

---

### `<datalist></datalist>`
**Definition:** Provides autocomplete suggestions for inputs.

**Explanation:** Creates a dropdown list of pre-defined options that appear as user types.

**Example:**
```html
<input list="browsers" name="browser">
<datalist id="browsers">
  <option value="Chrome">
  <option value="Firefox">
  <option value="Safari">
</datalist>
```

---

### `<output></output>`
**Definition:** Displays the result of a calculation.

**Explanation:** Shows calculated values from form inputs. Often used with JavaScript.

**Example:**
```html
<form oninput="result.value=parseInt(a.value)+parseInt(b.value)">
  <input type="number" id="a" value="0"> +
  <input type="number" id="b" value="0"> =
  <output name="result">0</output>
</form>
```

---

## 🔗 Meta & Link Tags

### `<meta>`
**Definition:** Provides metadata about the HTML document.

**Explanation:** Goes in `<head>`. Gives info like character encoding, viewport settings, description.

**Example:**
```html
<meta charset="UTF-8">
<meta name="description" content="My website about coding">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

### `<link>`
**Definition:** Links external resources to the document.

**Explanation:** Most commonly used to link CSS stylesheets or favicons.

**Example:**
```html
<link rel="stylesheet" href="styles.css">
<link rel="icon" href="favicon.ico">
```

---

### `<style></style>`
**Definition:** Contains CSS styles for the document.

**Explanation:** Write CSS directly in HTML. Goes in `<head>` section.

**Example:**
```html
<style>
  body { background-color: lightblue; }
  h1 { color: navy; }
</style>
```

---

### `<script></script>`
**Definition:** Embeds or references JavaScript code.

**Explanation:** Add interactivity to your page. Can go in `<head>` or before closing `</body>`.

**Example:**
```html
<script>
  alert('Hello, World!');
</script>
<!-- Or link external file -->
<script src="script.js"></script>
```

---

### `<noscript></noscript>`
**Definition:** Content shown if JavaScript is disabled.

**Explanation:** Displays alternative content for users who have JavaScript turned off.

**Example:**
```html
<noscript>
  <p>This website requires JavaScript to work properly.</p>
</noscript>
```

---

## 📋 Additional List Types

### `<menu></menu>`
**Definition:** Represents a list of commands or options.

**Explanation:** Similar to `<ul>` but semantically for interactive items or toolbars.

**Example:**
```html
<menu>
  <li><button>New File</button></li>
  <li><button>Save</button></li>
  <li><button>Exit</button></li>
</menu>
```

---

## 🎭 More Semantic Tags

### `<dialog></dialog>`
**Definition:** Creates a dialog box or modal window.

**Explanation:** Can be shown/hidden with JavaScript. Use for pop-ups, alerts, or forms.

**Example:**
```html
<dialog id="myDialog" open>
  <p>This is a dialog box!</p>
  <button>Close</button>
</dialog>
```

---

### `<address></address>`
**Definition:** Contains contact information.

**Explanation:** Typically shown in italics. Use for email, physical address, phone numbers.

**Example:**
```html
<address>
  Contact us at: <a href="mailto:info@example.com">info@example.com</a><br>
  123 Main Street, City, State 12345
</address>
```

---

### `<bdi></bdi>`
**Definition:** Isolates text that might be in a different direction.

**Explanation:** Useful for text in languages that read right-to-left (Arabic, Hebrew) mixed with left-to-right text.

**Example:**
```html
<p>User <bdi>إيان</bdi> scored 100 points.</p>
```

---

### `<bdo></bdo>`
**Definition:** Overrides text direction.

**Explanation:** Forces text to display in specified direction using `dir` attribute.

**Example:**
```html
<bdo dir="rtl">This text goes right to left</bdo>
```

---

### `<wbr>`
**Definition:** Suggests a line break opportunity.

**Explanation:** Tells browser where it's okay to break a long word if needed. Doesn't force a break.

**Example:**
```html
<p>This is a super<wbr>cali<wbr>fragi<wbr>listic<wbr>word</p>
```

---

## 🎨 Deprecated Tags (Avoid Using)

These tags still work but are **outdated**. Use CSS instead:

- `<font>` - Use CSS `font-family`, `font-size`, `color` instead
- `<center>` - Use CSS `text-align: center` instead
- `<b>` - Use `<strong>` or CSS `font-weight: bold` instead
- `<i>` - Use `<em>` or CSS `font-style: italic` instead
- `<u>` - Use CSS `text-decoration: underline` instead
- `<strike>` or `<s>` - Use `<del>` or CSS `text-decoration: line-through` instead
- `<big>` - Use CSS `font-size` instead
- `<tt>` - Use `<code>` or CSS `font-family: monospace` instead

---

## 🌐 Special Characters (HTML Entities)

### Common Entities
**Definition:** Special codes to display reserved or special characters.

**Explanation:** HTML uses `&` followed by code or name and `;` to show characters that have special meaning.

**Examples:**
```html
&lt;    <!-- Less than: < -->
&gt;    <!-- Greater than: > -->
&amp;   <!-- Ampersand: & -->
&quot;  <!-- Quote: " -->
&apos;  <!-- Apostrophe: ' -->
&nbsp;  <!-- Non-breaking space -->
&copy;  <!-- Copyright: © -->
&reg;   <!-- Registered: ® -->
&euro;  <!-- Euro: € -->
&hearts; <!-- Heart: ♥ -->
```

---

## 📱 Responsive Meta Tags

### Viewport Meta Tag
**Definition:** Controls layout on mobile browsers.

**Explanation:** Essential for responsive design. Tells mobile devices how to scale the page.

**Example:**
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

### Character Encoding
**Definition:** Specifies character encoding for the document.

**Explanation:** UTF-8 supports all languages and characters. Always include this.

**Example:**
```html
<meta charset="UTF-8">
```

---

## 🔧 Advanced Table Elements

### `<thead></thead>`, `<tbody></tbody>`, `<tfoot></tfoot>`
**Definition:** Groups table sections.

**Explanation:** Organizes table into header, body, and footer. Helps with styling and accessibility.

**Example:**
```html
<table>
  <thead>
    <tr><th>Name</th><th>Score</th></tr>
  </thead>
  <tbody>
    <tr><td>Alice</td><td>95</td></tr>
    <tr><td>Bob</td><td>87</td></tr>
  </tbody>
  <tfoot>
    <tr><td>Average</td><td>91</td></tr>
  </tfoot>
</table>
```

---

### `<colgroup></colgroup>` & `<col>`
**Definition:** Defines column properties in tables.

**Explanation:** Apply styles or attributes to entire columns at once.

**Example:**
```html
<table>
  <colgroup>
    <col style="background-color: lightblue">
    <col style="background-color: lightyellow">
  </colgroup>
  <tr><td>Cell 1</td><td>Cell 2</td></tr>
</table>
```

---

## 🎯 Complete Modern HTML5 Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Character encoding -->
  <meta charset="UTF-8">
  
  <!-- Viewport for responsive design -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
  <!-- SEO Meta tags -->
  <meta name="description" content="Description of your page">
  <meta name="keywords" content="html, css, javascript">
  <meta name="author" content="Your Name">
  
  <!-- Title -->
  <title>My Modern Website</title>
  
  <!-- Favicon -->
  <link rel="icon" href="favicon.ico">
  
  <!-- CSS -->
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Header -->
  <header>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
  
  <!-- Main Content -->
  <main>
    <section id="home">
      <h1>Welcome</h1>
      <p>Main content goes here.</p>
    </section>
    
    <section id="about">
      <h2>About Us</h2>
      <article>
        <h3>Our Story</h3>
        <p>Article content...</p>
      </article>
    </section>
    
    <aside>
      <h3>Sidebar</h3>
      <p>Additional information...</p>
    </aside>
  </main>
  
  <!-- Footer -->
  <footer>
    <address>
      Email: <a href="mailto:info@example.com">info@example.com</a>
    </address>
    <p><small>&copy; 2024 My Website. All rights reserved.</small></p>
  </footer>
  
  <!-- JavaScript -->
  <script src="script.js"></script>
</body>
</html>
```

---

**Happy Coding! 🚀**

Now you have a **complete** HTML reference covering all major tags!
