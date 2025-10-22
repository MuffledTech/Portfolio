Suresh Nepali | Portfolio Project Documentation

1. Project Overview

This is a personal portfolio website built to showcase skills, works, certificates, and services. It is designed to be responsive, interactive, and modern, using HTML5, CSS3 (with Flexbox and Grid), and a bit of JavaScript for animations.

**Main Features:**
- Hero section with animated roles
- About Me section
- Skills displayed in a grid
- Work/Projects showcased with cards
- Certificates in a grid layout
- Services offered in card format
- Contact section with clickable icons
- Responsive design for mobile and desktop
- Smooth scroll navigation

2. HTML Structure and Explanation

HTML is structured semantically using HTML5 semantic tags like <section>, <header>, <footer>, and <nav> for better readability and SEO.

**Key HTML Tags Used**
| Tag | Description | Example |
|-----|-------------|---------|
| <header> | Defines the header section of a page, often containing logo and navigation. | `<header class="head"><h1>SURESH NEPALI</h1></header>` |
| <nav> | Defines a navigation menu. | `<nav><ul><li><a href="#home">Home</a></li></ul></nav>` |
| <section> | Defines a standalone section of content (used for hero, about, skills, work, etc.) | `<section id="about" class="about"> ... </section>` |
| <footer> | Defines the footer section. | `<footer>© 2025 Suresh Nepali</footer>` |
| <h1>, <h2>, <h3> | Headings of different levels. Important for structure and SEO. | `<h2>Skills</h2>` |
| <p> | Paragraph text. | `<p>I’m passionate about building tech that’s beautiful...</p>` |
| <ul>, <li> | Unordered list. | `<ul><li>Web Development</li></ul>` |
| <img> | Embeds an image. alt provides alternative text. loading="eager" ensures fast load. | `<img src="user/2.png" alt="Profile Picture">` |
| <a> | Hyperlink. Can open in new tab with target="_blank". | `<a href="https://github.com" target="_blank">GitHub</a>` |
| <span> | Inline element used for styling or JavaScript effects. | `<span class="animated-role"></span>` |
| <link> | Links CSS or fonts. | `<link rel="stylesheet" href="style.css">` |
| <meta> | Provides metadata like charset and viewport. | `<meta charset="UTF-8">` |
| <title> | Sets the page title. | `<title>Suresh Nepali</title>` |
| <hr> | Horizontal rule, used for separating sections. | `<hr>` |

3. Modern HTML Elements Introduced
- `<section>` – Used to define a meaningful standalone section of content.
```html
<section id="skills">
  <h2>Skills</h2>
  <div class="skill-grid"> ... </div>
</section>
```
- `<header>` & `<footer>` – Semantic tags for the top and bottom areas of the page.
- `<nav>` – Clearly indicates the navigation area.
- `<span>` – Inline element useful for animation or text highlighting.
- `loading="eager"` in `<img>` – Forces the image to load immediately.
- `target="_blank"` in `<a>` – Opens links in a new browser tab.

4. CSS Structure and Explanation

Your CSS uses modern techniques like CSS Variables, Flexbox, Grid, transitions, hover effects, and responsive design.

**4.1 Global Styles**
```css
:root {
  --bg: #f5f3ef;
  --primary: #4a3f35;
  --accent: #c19a6b;
  --text: #1f1f1f;
  --highlight: #d2691e;
}
```
- `:root` – Represents the root element of the document (HTML). Used to define CSS variables for easy color/theme management.
- CSS Variables – Defined using `--variable-name` and used with `var(--variable-name)`.

**4.2 Flexbox**
```css
.head {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}
```
- `justify-content: space-between;` – pushes elements to edges.
- `align-items: center;` – vertically aligns items.
- `flex-wrap: wrap;` – wraps elements to the next line on small screens.

**4.3 CSS Grid**
```css
.work-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}
```
- `repeat(auto-fit, minmax(250px, 1fr))` – Automatically fits as many columns as possible; each column is at least 250px and can grow.

**Example:**
```css
.skill-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  gap: 15px;
}
```

**4.4 Responsive Design**
```css
@media (max-width: 600px) {
  .contact-item img {
    width: 60px;
    height: 60px;
  }
  .contact h2 {
    font-size: 1.7rem;
  }
}
```
- `@media` – Applies CSS rules only for screens less than 600px.

**4.5 Hover and Transition Effects**
```css
.work-card:hover img {
  transform: scale(1.05);
  transition: transform 0.3s, box-shadow 0.3s;
}
```
- `transition` – Makes changes smooth.

**4.6 Aspect Ratio**
```css
.certificate-card {
  aspect-ratio: 4 / 3;
}
```
- Keeps cards proportional.

**4.7 Box Shadow and Border Radius**
```css
.work-card {
  border-radius: 15px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.1);
}
```

**4.8 CSS Variables Example**
```css
.skill {
  background-color: var(--accent);
  color: var(--primary);
}
.skill:hover {
  background-color: var(--primary);
  color: var(--bg);
}
```

5. JavaScript Animation
```javascript
const roles = ["Coder", "Programmer", "Developer", "Designer"];
const roleSpan = document.querySelector(".animated-role");
let i = 0;
function changeRole() {
    roleSpan.textContent = roles[i];
    i = (i + 1) % roles.length;
}
setInterval(changeRole, 2000);
```
- `setInterval` – Runs the function every 2 seconds, cycling through array of roles dynamically.

6. List of Modern HTML/CSS Features Used
**HTML:**
- `<header>, <footer>, <nav>, <section>` – Semantic HTML5 tags
- `<span>` – Inline element for JS styling/animation
- `loading="eager"` in `<img>` – Controls image loading
- `target="_blank"` in `<a>` – Opens new tab

**CSS:**
- `:root` – Root element, defines variables
- CSS Variables – `--bg, --primary` etc.
- Flexbox – `display: flex; justify-content; align-items; flex-wrap`
- CSS Grid – `display: grid; grid-template-columns; gap; auto-fit; minmax()`
- `aspect-ratio` – Maintains consistent element dimensions
- `object-fit` – Controls image fit inside container
- `transition` – Smooth animation effects
- `box-shadow` – Depth and elevation
- `border-radius` – Rounded corners
- Media queries – `@media` for responsiveness

7. Example of a CSS Grid
```html
<div class="skill-grid">
  <div class="skill">HTML5</div>
  <div class="skill">CSS3</div>
  <div class="skill">JavaScript</div>
  <div class="skill">Python</div>
</div>
```
```css
.skill-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  gap: 15px;
}
```
- Grid automatically fits as many columns as possible
- Each column is at least 120px, can expand to fill space
- Gap between items: 15px

8. Summary

Your project uses modern HTML5 and CSS3 practices, including:
- Semantic tags for structure
- CSS Variables for theme management
- Flexbox and Grid for responsive layouts
- Hover effects and animations for interactivity
- Media queries for responsiveness
- Aspect ratios for consistent card design

This approach ensures your portfolio is clean, responsive, professional, and easy to maintain.

