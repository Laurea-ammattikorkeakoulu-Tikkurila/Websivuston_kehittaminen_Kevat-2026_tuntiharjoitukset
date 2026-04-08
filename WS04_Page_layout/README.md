# WS04_Page_layout - Page Layout with CSS Grid and Flexbox

This exercise expands the WS03 advanced CSS work into a multi-page website with a consistent page layout.

## What was implemented

1. Multi-page structure
- Home page: `index.html`
- Gallery page: `gallery.html`
- Contact page: `contact.html`

2. Shared semantic layout on every page
- `<header>` for page title/banner
- `<nav>` for page navigation
- `<aside>` for supporting content
- `<main>` for primary page content
- `<footer>` for footer information

3. CSS Grid for page structure
- A two-column layout is used for the content area:
  - Left column: sidebar (`<aside>`)
  - Right column: main content (`<main>`)

4. Flexbox for navigation
- The top navigation bar is built with Flexbox for horizontal alignment and spacing of links.

5. Responsive behavior
- On smaller screens (max-width: 700px), the layout changes from two columns to one column.
- Sidebar sticky behavior is disabled on mobile for better usability.

6. Reused and extended WS03 advanced CSS features
- `@keyframes` animation for the banner
- Hover transitions on images
- Styled lists with pseudo-classes (`:nth-child`, `:first-child`, `:last-child`)
- Pseudo-elements (`::before`, `::after`, `::first-letter`)
- Styled form with focus and hover states

7. Aside content improvements
- Basic page layout concept explanation
- Semantic elements summary
- External learning links:
  - W3Schools CSS Flexbox
  - W3Schools CSS Grid

## Folder structure

```text
WS04_Page_layout/
├── README.md
└── tuntiharjoitus/
    ├── index.html
    ├── gallery.html
    ├── contact.html
    ├── images/
    │   ├── Berfin.jpg
    │   └── Jari_Hki.JPG
    └── styles/
        └── style.css
```

## Learning goals

After this exercise, you should be able to:
- Build a multi-page website with a shared layout
- Use semantic HTML structure clearly
- Apply CSS Grid for high-level page layout
- Apply Flexbox for component-level layout
- Keep styling reusable with one external stylesheet
- Add responsive behavior with media queries
