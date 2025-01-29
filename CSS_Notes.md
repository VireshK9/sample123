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

*(Continued in next comment due to length...)*  

Let me know if you want me to continue with the remaining topics (21-37) or adjust the format! 🚀
