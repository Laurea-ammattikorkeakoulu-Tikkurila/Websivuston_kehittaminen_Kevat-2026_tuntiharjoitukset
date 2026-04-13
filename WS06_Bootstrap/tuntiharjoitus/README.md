# WS06 – Bootstrap

## What is Bootstrap?

Bootstrap is an open-source CSS framework originally created by Twitter in 2011.
It provides a collection of pre-built components, a responsive grid system, and utility
classes that let you build responsive, mobile-first websites quickly — without writing
all the CSS yourself.

Bootstrap 5 (the current version) removed the jQuery dependency and is now pure
HTML, CSS and JavaScript.

## Bootstrap vs. Custom CSS

| Feature | WS05 (Custom CSS) | WS06 (Bootstrap) |
|---|---|---|
| Responsive grid | CSS Grid + media queries | `container` / `row` / `col-*` classes |
| Navigation | CSS-only checkbox hack | `navbar` + `navbar-toggler` (JS) |
| Cards | Manual `.card` CSS rules | `card` / `card-body` / `card-img-top` classes |
| Forms | Custom input styles | `form-control` / `form-label` / `btn` classes |
| Hamburger menu | `#nav-toggle:checked ~ .nav-links` | Built-in `data-bs-toggle="collapse"` |
| Breakpoints | Custom (`600px`, `900px`, `1200px`) | Bootstrap defaults (`sm` 576px, `md` 768px, `lg` 992px) |

**Key takeaway:** Bootstrap trades flexibility for speed. Custom CSS gives full control;
Bootstrap gives ready-made, tested, accessible components.

## Bootstrap Grid System

Bootstrap uses a **12-column grid** based on Flexbox:

```html
<div class="container">
  <div class="row">
    <div class="col-md-4">One third</div>
    <div class="col-md-4">One third</div>
    <div class="col-md-4">One third</div>
  </div>
</div>
```

Breakpoint prefixes:
- (none) — all screen sizes
- `sm` — ≥ 576 px
- `md` — ≥ 768 px
- `lg` — ≥ 992 px
- `xl` — ≥ 1200 px
- `xxl` — ≥ 1400 px

## Exercise Files

| File | Demonstrates |
|---|---|
| `index.html` | Navbar, hero section, Bootstrap cards grid |
| `gallery.html` | `row-cols-*` responsive image gallery |
| `contact.html` | Bootstrap form components |
| `info.html` | Accordion component, image gallery, Bootstrap intro |
| `styles/style.css` | Minimal custom overrides on top of Bootstrap |

## How to Include Bootstrap

```html
<!-- In <head> — Bootstrap CSS -->
<link rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css">

<!-- Before </body> — Bootstrap JS bundle (includes Popper.js) -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
```
