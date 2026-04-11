# WS05 – Responsive Design

This exercise teaches you how to build websites that adapt to any screen size using only HTML and CSS.

---

## What is Responsive Design?

Responsive design means that a web page looks good and works well on all devices — from small smartphones to large desktop monitors. Instead of building separate sites for mobile and desktop, you write one codebase that adapts using CSS.

---

## Mobile-First Approach

The modern best practice is to write **base styles for mobile first**, then progressively add styles for larger screens using `min-width` media queries.

```css
/* Mobile styles (default) */
.layout-grid { display: block; }

/* Tablet and above */
@media (min-width: 600px) {
    .layout-grid { display: grid; }
}
```

This is the opposite of WS04, which used `max-width: 700px` (desktop-first). Mobile-first is the industry standard because most web traffic comes from mobile devices.

---

## Viewport Meta Tag

The viewport meta tag tells the browser not to zoom out on mobile devices:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

- `width=device-width` — use the actual screen width
- `initial-scale=1.0` — do not zoom in or out

Without this tag, a responsive design will not work correctly on mobile.

---

## Media Queries

Media queries apply CSS rules only when certain conditions are met:

```css
@media (min-width: 768px) {
    /* styles for screens 768px wide and above */
}
```

**Breakpoints used in this exercise:**

| Breakpoint | Target |
|---|---|
| Base (no query) | Mobile phones (<600px) |
| `min-width: 600px` | Tablets |
| `min-width: 900px` | Desktop |
| `min-width: 1200px` | Wide screens |

---

## Responsive Typography with `clamp()`

`clamp(min, preferred, max)` creates fluid font sizes that scale smoothly with the viewport:

```css
h1 {
    font-size: clamp(1.2rem, 4vw, 1.7rem);
}
```

- `1.2rem` — minimum size (never smaller)
- `4vw` — preferred size (4% of viewport width)
- `1.7rem` — maximum size (never larger)

No media queries needed for typography!

---

## Responsive Images

Always use these two rules to make images fluid:

```css
img {
    max-width: 100%;
    height: auto;
}
```

This prevents images from overflowing their containers on small screens while still allowing them to grow on larger screens.

For art direction (different images on different screens), the `<picture>` element can be used:

```html
<picture>
    <source srcset="large.jpg" media="(min-width: 900px)">
    <img src="small.jpg" alt="Description">
</picture>
```

---

## CSS-Only Responsive Navigation

This exercise uses the **checkbox hack** to create a mobile hamburger menu without JavaScript:

```html
<input type="checkbox" id="nav-toggle" class="nav-toggle">
<label for="nav-toggle" class="nav-toggle-label">☰</label>
<div class="nav-links">
    <a href="index.html">Home</a>
</div>
```

```css
/* Hide links on mobile by default */
.nav-links { display: none; }

/* Show when checkbox is checked */
#nav-toggle:checked ~ .nav-links { display: flex; }

/* Hide checkbox itself */
.nav-toggle { display: none; }

/* Hide hamburger on desktop */
@media (min-width: 900px) {
    .nav-toggle-label { display: none; }
    .nav-links { display: flex; }  /* always visible */
}
```

---

## Fluid Grid Layouts

CSS Grid's `auto-fit` with `minmax()` creates a responsive grid without any media queries:

```css
.gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 16px;
}
```

- Columns are at least 250px wide
- They grow to fill available space equally (`1fr`)
- Columns automatically wrap to new rows when they don't fit
- On mobile: 1 column. On tablet: 2 columns. On desktop: 3+ columns

---

## Viewport Units

CSS viewport units make elements proportional to the screen size:

| Unit | Meaning |
|---|---|
| `vw` | 1% of viewport width |
| `vh` | 1% of viewport height |
| `vmin` | 1% of the smaller dimension |
| `vmax` | 1% of the larger dimension |

Example:
```css
header {
    min-height: 30vh;  /* always at least 30% of screen height */
}
```

---

## CSS Custom Properties (Variables)

CSS variables make your color palette maintainable:

```css
:root {
    --color-primary: steelblue;
    --color-dark: #1a3a5c;
    --color-bg: #f0f4f8;
}

/* Use anywhere */
nav { background-color: var(--color-dark); }
a:hover { color: var(--color-primary); }
```

---

## Testing Responsive Design

Use your browser's **DevTools** to simulate different screen sizes:

1. Press **F12** (or right-click → Inspect)
2. Click the **device toolbar** icon (mobile/tablet icon)
3. Choose a device preset or drag to resize
4. Test all breakpoints: 360px, 600px, 900px, 1200px

---

## Further Reading

- [W3Schools – CSS Media Queries](https://www.w3schools.com/css/css3_mediaqueries.asp)
- [W3Schools – Responsive Web Design](https://www.w3schools.com/css/css_rwd_intro.asp)
- [W3Schools – CSS clamp()](https://www.w3schools.com/cssref/func_clamp.php)
- [W3Schools – CSS Grid auto-fit](https://www.w3schools.com/cssref/pr_grid-template-columns.php)
- [W3Schools – Viewport Units](https://www.w3schools.com/css/css_viewport.asp)
- [W3Schools – CSS Variables](https://www.w3schools.com/css/css3_variables.asp)

---

Copyright © Jari Kovis, Laurea. Content created with the assistance of GitHub Copilot.
