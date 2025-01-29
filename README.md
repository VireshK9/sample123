# HTML Notes for Web Development

## Table of Contents
1. [Introduction to HTML](#1-introduction-to-html)
2. [File Creation](#2-file-creation)
3. [Boilerplate Code](#3-boilerplate-code)
4. [Heading Tags](#4-heading-tags)
5. [Paragraph Tags](#5-paragraph-tags)
6. [Horizontal Rule & Line Break](#6-horizontal-rule--line-break)
7. [Lists](#7-lists)
8. [Image Tag](#8-image-tag)
9. [Tables](#9-tables)
10. [Anchor Tag](#10-anchor-tag)
11. [Text Formatting](#11-text-formatting)
12. [Forms](#12-forms)
13. [Structural Tags](#13-structural-tags)
14. [Favicon](#14-favicon)
15. [Video Tag](#15-video-tag)
16. [YouTube Integration](#16-youtube-integration)

---

## 1. Introduction to HTML

### Definition
HTML (HyperText Markup Language) is the standard language for creating web pages. It defines the structure and content of a webpage using tags.

### Key Concepts
- HTML elements are represented by tags
- Tags typically come in pairs: opening `<tag>` and closing `</tag>`
- Elements can contain attributes that provide additional information

### Basic Structure
```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Page</title>
  </head>
  <body>
    <h1>Hello World!</h1>
  </body>
</html>
```

### Common Mistakes to Avoid
- Unclosed tags
- Incorrect nesting of elements
- Missing required attributes

---

## 2. File Creation

### Steps to Create an HTML File
1. Create a new file with `.html` extension
2. Write HTML code
3. Save and open in a browser

### Best Practices
- Use dedicated code editors (VS Code, Sublime Text)
- Maintain consistent file naming conventions
- Keep files organized in project folders

---

## 3. Boilerplate Code

### Standard HTML5 Template
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <!-- Content goes here -->
</body>
</html>
```

### Essential Elements Explained
- `<!DOCTYPE html>`: Declares HTML5 document
- `<html lang="en">`: Root element with language specification
- `<meta charset="UTF-8">`: Character encoding declaration
- `<meta name="viewport">`: Mobile responsiveness settings

---

## 4. Heading Tags

### Usage and Hierarchy
- `<h1>` to `<h6>` represent different heading levels
- `<h1>` is the main heading
- `<h2>` to `<h6>` are subheadings

### Best Practices
- Use only one `<h1>` per page
- Maintain hierarchical structure
- Don't skip heading levels

---

## 5. Paragraph Tags

### Basic Usage
```html
<p>This is a paragraph of text.</p>
```

### Features
- Automatic spacing before and after
- Can contain inline elements
- Supports text formatting

---

## 6. Horizontal Rule & Line Break

### Usage
```html
<p>First line<br>Second line</p>
<hr>
```

### Best Practices
- Use `<br>` sparingly
- Prefer CSS for spacing when possible
- Use `<hr>` for thematic breaks

---

## 7. Lists

### Ordered Lists
```html
<ol>
  <li>First item</li>
  <li>Second item</li>
</ol>
```

### Unordered Lists
```html
<ul>
  <li>Bullet point</li>
  <li>Another point</li>
</ul>
```

### List Attributes
- `type`: Specifies numbering style
- `start`: Sets starting number
- `reversed`: Reverses order

---

## 8. Image Tag

### Syntax
```html
<img src="image.jpg" alt="Description" width="300" height="200">
```

### Required Attributes
- `src`: Image source path
- `alt`: Alternative text

### Best Practices
- Always include alt text
- Specify dimensions
- Use appropriate file formats
- Optimize image sizes

---

## 9. Tables

### Basic Structure
```html
<table>
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
  </tr>
  <tr>
    <td>Data 1</td>
    <td>Data 2</td>
  </tr>
</table>
```

### Components
- `<table>`: Container element
- `<tr>`: Table row
- `<th>`: Table header
- `<td>`: Table data

### Best Practices
- Use for tabular data only
- Include proper headers
- Consider accessibility

---

## 10. Anchor Tag

### Basic Links
```html
<a href="https://example.com">Visit Website</a>
```

### Advanced Usage
```html
<a href="page.html" target="_blank" rel="noopener">Open in New Tab</a>
```

### Attributes
- `href`: Destination URL
- `target`: Opening behavior
- `rel`: Relationship attribute

---

## 11. Text Formatting

### Semantic Elements
```html
<strong>Important text</strong>
<em>Emphasized text</em>
```

### Presentational Elements
```html
<b>Bold text</b>
<i>Italic text</i>
```

### Best Practices
- Prefer semantic elements
- Use CSS for styling
- Consider accessibility

---

## 12. Forms

### Basic Form Structure
```html
<form action="/submit" method="POST">
  <label for="username">Username:</label>
  <input type="text" id="username" name="username" required>
  
  <label for="password">Password:</label>
  <input type="password" id="password" name="password" required>
  
  <button type="submit">Submit</button>
</form>
```

### Common Input Types
- text
- password
- email
- number
- checkbox
- radio
- date
- file

### Form Validation
- required attribute
- pattern matching
- input types
- custom validation

---

## 13. Structural Tags

### Semantic Elements
```html
<header>
  <nav>
    <!-- Navigation content -->
  </nav>
</header>

<main>
  <section>
    <!-- Section content -->
  </section>
  
  <article>
    <!-- Article content -->
  </article>
</main>

<footer>
  <!-- Footer content -->
</footer>
```

### Best Practices
- Use semantic elements appropriately
- Maintain clear document structure
- Consider SEO implications

---

## 14. Favicon

### Implementation
```html
<head>
  <link rel="icon" type="image/x-icon" href="favicon.ico">
</head>
```

### Requirements
- Small image size (16x16 or 32x32)
- ICO, PNG, or GIF format
- Placed in head section

---

## 15. Video Tag

### Basic Implementation
```html
<video width="320" height="240" controls>
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
  Your browser does not support the video tag.
</video>
```

### Attributes
- controls
- autoplay
- loop
- muted
- poster

---

## 16. YouTube Integration

### Embedding Videos
```html
<iframe 
  width="560" 
  height="315" 
  src="https://www.youtube.com/embed/VIDEO_ID" 
  title="YouTube video player" 
  frameborder="0" 
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope" 
  allowfullscreen>
</iframe>
```

### Best Practices
- Responsive dimensions
- Proper permissions
- Loading optimization

---

## Practice Exercises

### Basic Exercises
1. Create a personal profile page
2. Build a contact form
3. Create a photo gallery
4. Design a navigation menu

### Advanced Projects
1. Portfolio website
2. Blog layout
3. Product catalog
4. Landing page

---
