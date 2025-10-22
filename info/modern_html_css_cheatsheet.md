Modern HTML & CSS Cheat Sheet – Portfolio Project

1️⃣ HTML5 Semantic Tags
| Tag | Purpose | Mini Example | Visual |
|-----|---------|-------------|--------|
| <header> | Header of page or section (logo + nav) | `<header><h1>Logo</h1></header>` | 📌 Top bar with site name & menu |
| <nav> | Navigation menu | `<nav><ul><li><a href="#home">Home</a></li></ul></nav>` | 🧭 Menu links |
| <section> | Logical sections (hero, about, skills) | `<section id="about">...</section>` | 📄 Separate content blocks |
| <footer> | Page footer | `<footer>© 2025 Suresh Nepali</footer>` | 🔚 Bottom bar with copyright |
| <span> | Inline text element (styling/animation) | `<h3>I'm a <span class="animated-role"></span></h3>` | ✨ Inline animated text |
| <img> + loading="eager" | Embed images & prioritize loading | `<img src="pic.png" loading="eager">` | 🖼️ Image shown immediately |
| <a> + target="_blank" | Links, open in new tab | `<a href="url" target="_blank">GitHub</a>` | 🔗 Opens new browser tab |

2️⃣ CSS Variables & Root
```css
:root {
  --bg: #f5f3ef;
  --primary: #4a3f35;
  --accent: #c19a6b;
}
```
- `:root` → top-level HTML element
- `--variable` → defines reusable values
- `var(--variable)` → uses the variable anywhere

**Example Usage:**
```css
body {
  background-color: var(--bg);
  color: var(--primary);
}
```
Visual: 🎨 Centralized colors make styling consistent and easy to manage.

3️⃣ Flexbox
```css
.head {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```
- `display: flex;` → makes container flexible
- `justify-content` → horizontal alignment
- `align-items` → vertical alignment
- `flex-wrap` → wraps items to the next line

Visual: [Item 1]    [Item 2]    [Item 3]

**Example HTML:**
```html
<div class="head">
  <h1>Logo</h1>
  <nav>Menu</nav>
</div>
```

4️⃣ CSS Grid
```css
.work-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}
```
- `display: grid;` → enables grid layout
- `grid-template-columns` → defines columns
- `repeat(auto-fit, minmax(...))` → responsive columns
- `gap` → space between grid items

Visual:
[Card] [Card] [Card]
[Card] [Card] [Card]

**Mini Example:**
```html
<div class="skill-grid">
  <div>HTML5</div>
  <div>CSS3</div>
  <div>JS</div>
</div>
```

5️⃣ Aspect Ratio
```css
.certificate-card {
  aspect-ratio: 4 / 3;
}
```
- Ensures consistent width:height ratio
- Auto-resizes for responsiveness
Visual: +---------+
        |         |
        |         |  4:3 ratio
        +---------+

6️⃣ Object-Fit
```css
img {
  object-fit: cover;
}
```
- Makes image fill container without distortion
- Options: cover, contain, fill
Visual: [Image fits nicely inside box without stretching]

7️⃣ Transitions & Hover Effects
```css
.skill:hover {
  background-color: var(--primary);
  color: var(--bg);
  transition: 0.3s;
}
```
- `transition` → smooth change on hover
- `hover` → triggers effect when mouse is over element
Visual: Normal: [HTML5] → Hover: [HTML5 changes color smoothly]

8️⃣ Media Queries (Responsive Design)
```css
@media (max-width: 600px) {
  .contact h2 {
    font-size: 1.7rem;
  }
}
```
- Makes layout responsive for mobile
- Applies CSS only if screen width ≤ 600px
Visual: Desktop → large header, Mobile → smaller header

9️⃣ JavaScript Animation (Dynamic Text)
```javascript
const roles = ["Coder", "Programmer", "Designer"];
let i = 0;
const roleSpan = document.querySelector(".animated-role");

function changeRole() {
  roleSpan.textContent = roles[i];
  i = (i + 1) % roles.length;
}

setInterval(changeRole, 2000);
```
- Cycles through roles every 2 seconds
- Updates `<span>` text dynamically
Visual: Hello, I'm a Coder → Programmer → Designer → Coder...

🔟 Box Shadow & Border Radius
```css
.work-card {
  border-radius: 15px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.1);
}
```
- `border-radius` → rounded corners
- `box-shadow` → soft shadow for depth
Visual: +---------------+
        |   Card Box    |
        +---------------+

11️⃣ Cheat Sheet Summary Table
| Feature | CSS/HTML | Use | Visual |
|---------|----------|-----|--------|
| Semantic Tags | <header>, <section>, <footer> | Structure & SEO | 📄 Blocks |
| CSS Variables | --primary | Reusable colors | 🎨 Palette |
| Flexbox | display: flex; | Horizontal/Vertical alignment | ↔️ |
| CSS Grid | display: grid; | Layout cards & items | 🔲 |
| Aspect Ratio | aspect-ratio: 4/3; | Fixed proportions | ⬛ |
| Object-Fit | object-fit: cover; | Images inside containers | 🖼️ |
| Transition | transition: 0.3s; | Smooth hover effect | ✨ |
| Media Queries | @media | Responsive design | 📱 |
| JS Dynamic Text | setInterval() | Animated roles | 🔤 |
| Box Shadow | box-shadow | Depth | 🌑 |
| Border Radius | border-radius | Rounded corners | 🔵 |

