# CSS Notes for Web Development  
*By Mr.Viresh Kariappa*  

---

## 1. **CSS Introduction**  
**Definition**:  
CSS (Cascading Style Sheets) styles HTML elements to control layout, colors, fonts, and responsiveness.  

**Example**:  
```css 
h1 { 
  color: red; 
  text-align: center; 
} 
```  

---

## 2. **Types of CSS**  
1. **Inline CSS**:  
   ```html 
   <p style="color: blue;">This is inline CSS.</p> 
   ```  
2. **Internal CSS**:  
   ```html 
   <style> 
     p { font-size: 16px; } 
   </style> 
   ```  
3. **External CSS**:  
   ```html 
   <link rel="stylesheet" href="styles.css"> 
   ```  

**Best Practice**: Use external CSS for maintainability.  

---

## 3. **CSS Syntax**  
```css 
selector { 
  property: value; /* Declaration */ 
} 
```  
- **Selector**: Targets HTML elements (e.g., `div`, `.class`, `#id`).  
- **Declaration**: `property: value` pairs (e.g., `margin: 10px;`).  

**Common Mistake**: Missing semicolons (`;`).  

---

## 4. **CSS Selectors**  
| Selector          | Example          | Description                  |  
|--------------------|------------------|------------------------------|  
| Element            | `p`             | Selects all `<p>` elements.  |  
| Class              | `.header`       | Selects elements with `class="header"`. |  
| ID                 | `#banner`       | Selects element with `id="banner"`.     |  
| Universal          | `*`             | Selects all elements.        |  

**Combinators**:  
```css 
/* Child selector */ 
div > p { ... } 

/* Adjacent sibling */ 
h2 + p { ... } 
```  

---

## 5. **CSS Comments**  
```css 
/* This is a comment */ 
p { 
  color: red; /* Red text */ 
} 
```  

---

## 6. **CSS Colors**  
**Formats**:  
```css 
color: #FF0000;          /* Hex */ 
color: rgb(255, 0, 0);   /* RGB */ 
color: rgba(255,0,0,0.5);/* RGBA (with opacity) */ 
color: hsl(0, 100%, 50%);/* HSL */ 
```  

---

## 7. **CSS Background & Opacity**  
**Background Properties**:  
```css 
div { 
  background-color: #f0f0f0; 
  opacity: 0.8; /* Affects entire element */ 
} 
```  
**Opacity Tip**: Use `rgba()` for background-only opacity:  
```css 
background: rgba(255, 0, 0, 0.5); /* 50% opacity */ 
```  

---

## 8. **CSS Background Image**  
```css 
body { 
  background-image: url("image.jpg"); 
  background-repeat: no-repeat; /* or repeat-x, repeat-y */ 
  background-position: center top; 
} 
```  

---

## 9. **CSS Border**  
**Properties**:  
```css 
div { 
  border: 2px solid red; /* shorthand */ 
  border-top: 1px dashed #333; 
  border-radius: 10px; /* Rounded corners */ 
} 
```  

---

## 10. **CSS Margin**  
```css 
p { 
  margin: 10px;          /* All sides */ 
  margin: 10px 20px;     /* Top/Bottom, Left/Right */ 
  margin-top: 15px;      /* Individual side */ 
} 
```  

---

## 11. **CSS Padding**  
```css 
div { 
  padding: 20px;         /* All sides */ 
  padding-left: 30px;    /* Individual side */ 
} 
```  

---

## 12. **CSS Height/Width**  
```css 
div { 
  width: 50%; 
  min-width: 200px; 
  max-height: 400px; 
} 
```  

---

## 13. **CSS Outline**  
**Difference from Border**:  
- Outline doesn’t take up space (drawn outside the border).  
```css 
input:focus { 
  outline: 2px solid blue; 
} 
```  

---

## 14. **CSS Text**  
**Properties**:  
```css 
p { 
  text-align: right; 
  text-transform: uppercase; 
  text-indent: 50px; 
  letter-spacing: 2px; 
  line-height: 1.6; 
  text-shadow: 2px 2px 4px rgba(0,0,0,0.5); 
} 
```  

---

## 15. **CSS Fonts**  
**Properties**:  
```css 
p { 
  font-family: "Arial", sans-serif; 
  font-style: italic; 
  font-weight: bold; 
  font-size: 1.2rem; 
} 
```  
**Google Fonts**:  
```html 
<link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet"> 
```  

---

## 16. **CSS Icons**  
**Using Font Awesome**:  
```html 
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css"> 
<i class="fas fa-user"></i> 
```  

---

## 17. **CSS Links**  
**Pseudo-classes**:  
```css 
a:link { color: blue; }      /* Unvisited */ 
a:visited { color: purple; } /* Visited */ 
a:hover { color: red; }      /* Hover */ 
a:active { color: green; }   /* Clicked */ 
```  

---

## 18. **CSS Table Style**  
**Styling**:  
```css 
table { 
  width: 100%; 
  border-collapse: collapse; 
} 
td { 
  padding: 8px; 
  border-bottom: 1px solid #ddd; 
} 
tr:hover { background: #f5f5f5; } 
```  

---

## 19. **CSS Display Properties**  
**Values**:  
- `inline` (no width/height, e.g., `<span>`).  
- `block` (takes full width, e.g., `<div>`).  
- `inline-block` (mix of both).  
- `none` (hides element).  

**Example**:  
```css 
.hidden { 
  display: none; 
} 
```  

---

## 20. **CSS Positioning**  
**Position Types**:  
1. **Static**: Default (not positioned).  
2. **Relative**: Positioned relative to itself.  
3. **Absolute**: Positioned relative to nearest positioned ancestor.  
4. **Fixed**: Positioned relative to the viewport.  
5. **Sticky**: Toggles between relative and fixed.  

**Example**:  
```css 
.header { 
  position: fixed; 
  top: 0; 
} 
```  

---

Here’s the continuation of the **CSS Notes** for topics **21-37** in GitHub-friendly markdown:

---

## 21. **Positioning Text in an Image**  
**Example**:  
```html
<div class="image-container">
  <img src="nature.jpg" alt="Nature">
  <div class="text-overlay">Welcome to the Forest</div>
</div>
```

```css
.image-container {
  position: relative;
}

.text-overlay {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
}
```  
**Tip**: Use `z-index` to control overlapping layers.  

---

## 22. **CSS z-index**  
**Definition**:  
Controls the stacking order of positioned elements. Higher values appear on top.  

**Example**:  
```css
.box1 { 
  position: absolute; 
  z-index: 2; 
}
.box2 { 
  position: relative; 
  z-index: 1; 
}
```  
**Note**: `z-index` only works on elements with `position` set (e.g., `absolute`, `relative`).  

---

## 23. **CSS Overflow**  
**Properties**:  
- `visible` (default): Content overflows the container.  
- `hidden`: Clips overflow content.  
- `scroll`: Adds scrollbars.  
- `auto`: Adds scrollbars only when needed.  

**Example**:  
```css
div {
  width: 200px;
  height: 100px;
  overflow: auto;
}
```  

---

## 24. **CSS Float**  
**Definition**:  
Positions elements to the left/right, allowing text/content to wrap around them.  

**Example**:  
```css
img {
  float: left;
  margin-right: 20px;
}
```  
**Common Mistake**: Forgetting to clear floats (use `clearfix`).  

---

## 25. **CSS Clear & Clearfix**  
**Clear**:  
```css
.clear-div {
  clear: both; /* Clears left/right floats */
}
```  

**Clearfix Hack**:  
```css
.clearfix::after {
  content: "";
  display: block;
  clear: both;
}
```  

---

## 26. **CSS Combinators**  
| Combinator              | Example           | Description                          |  
|-------------------------|-------------------|--------------------------------------|  
| Descendant (` `)         | `div p`          | All `<p>` inside `<div>`.           |  
| Child (`>`)             | `div > p`        | Direct child `<p>` of `<div>`.      |  
| Adjacent Sibling (`+`)  | `h1 + p`         | `<p>` immediately after `<h1>`.     |  
| General Sibling (`~`)   | `h1 ~ p`         | All `<p>` siblings after `<h1>`.    |  

---

## 27. **CSS Dropdowns**  
**Example**:  
```html
<div class="dropdown">
  <button>Hover Me</button>
  <div class="dropdown-content">
    <a href="#">Link 1</a>
    <a href="#">Link 2</a>
  </div>
</div>
```

```css
.dropdown-content {
  display: none; /* Hidden by default */
  position: absolute;
}

.dropdown:hover .dropdown-content {
  display: block; /* Show on hover */
}
```  

---

## 28. **CSS Forms**  
**Styling Inputs**:  
```css
input[type="text"] {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

input:focus {
  border-color: blue;
}
```  

---

## 29. **CSS Units**  
| Unit  | Description                     | Example         |  
|-------|---------------------------------|-----------------|  
| `px`  | Pixels (absolute)               | `font-size: 16px` |  
| `%`   | Relative to parent              | `width: 50%`     |  
| `em`  | Relative to font size of parent | `padding: 2em`  |  
| `rem` | Relative to root font size      | `margin: 1.5rem`|  
| `vw`  | 1% of viewport width            | `width: 100vw`  |  

---

## 30. **Linear Gradient**  
**Example**:  
```css
div {
  background: linear-gradient(45deg, red, blue);
}
```  
**Advanced**:  
```css
background: linear-gradient(to right, #ff0000 0%, #0000ff 100%);
```  

---

## 31. **CSS Transitions**  
**Definition**:  
Smoothly animate property changes over a duration.  

**Example**:  
```css
.button {
  transition: all 0.3s ease-in-out;
}
.button:hover {
  transform: scale(1.1);
}
```  

---

## 32. **CSS Animations**  
**Keyframes**:  
```css
@keyframes bounce {
  0%   { transform: translateY(0); }
  50%  { transform: translateY(-20px); }
  100% { transform: translateY(0); }
}

.element {
  animation: bounce 2s infinite;
}
```  

---

## 33. **CSS Tooltip**  
**Example**:  
```html
<span class="tooltip" data-tooltip="Hello!">Hover Me</span>
```

```css
.tooltip:hover::after {
  content: attr(data-tooltip);
  position: absolute;
  background: black;
  color: white;
  padding: 5px;
  border-radius: 3px;
}
```  

---

## 34. **CSS Masking**  
**Example**:  
```css
.masked-image {
  mask-image: linear-gradient(to bottom, transparent 20%, black 80%);
  -webkit-mask-image: linear-gradient(to bottom, transparent 20%, black 80%);
}
```  

---

## 35. **CSS Flexbox**  
**Core Properties**:  
```css
.container {
  display: flex;
  justify-content: center; /* Main axis */
  align-items: center;     /* Cross axis */
  gap: 10px;
}

.item {
  flex: 1; /* Grow/shrink equally */
}
```  

---

## 36. **CSS Media Queries**  
**Responsive Breakpoints**:  
```css
/* Mobile-first approach */
.container { padding: 10px; }

/* Tablet */
@media (min-width: 768px) {
  .container { padding: 20px; }
}

/* Desktop */
@media (min-width: 1024px) {
  .container { padding: 30px; }
}
```  
---

# Exercises  
1. **Flexbox Layout**: Create a responsive navbar using Flexbox.  
2. **Media Queries**: Build a grid layout that switches from 2 columns (desktop) to 1 column (mobile).  

---

