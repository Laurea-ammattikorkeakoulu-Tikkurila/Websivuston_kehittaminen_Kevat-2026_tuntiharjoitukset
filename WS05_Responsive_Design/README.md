# WS05_Responsive_Design – Responsiivinen Suunnittelu

Tämä harjoitus laajentaa WS04:n sivuasettelua responsiiviseksi — sivusto mukautuu
automaattisesti mobiilista pöytätietokoneeseen.

## Mitä on toteutettu

### 1. Moniosainen sivusto
- Etusivu: `index.html`
- Kuvagalleria: `gallery.html`
- Yhteystiedot: `contact.html`

### 2. Viewport-metatag
Jokaisella sivulla on `<meta name="viewport" content="width=device-width, initial-scale=1.0">`,
joka on pakollinen responsiivisen suunnittelun toimimiseksi mobiililla.

### 3. Mobile-first-lähestymistapa
CSS kirjoitetaan ensin mobiilille ja laajennetaan isommille ruuduille
`min-width`-mediakyselyillä:

| Breakpoint | Kuvaus                                 |
|-----------|----------------------------------------|
| perus      | Mobiili (alle 600 px) — yksipalstainen |
| 600 px     | Tabletti — sivupalkki näkyy            |
| 900 px     | Pöytätietokone — CSS Grid kaksipalsta  |
| 1200 px    | Leveä näyttö — lisätilaa sivuille      |

### 4. Responsiivinen navigaatio — CSS-only hamburger-valikko
Mobiilissa nav-linkit piilotetaan ja näytetään "Menu"-painikkeella.
Toteutus käyttää pelkkää CSS:ää (ei JavaScriptiä):
- Piilotettu `<input type="checkbox" id="nav-toggle">`
- `<label>`-elementti toimii näkyvänä painikkeena
- CSS-selektori `#nav-toggle:checked ~ .nav-links` avaa valikon
- Pöytätietokoneella (900 px+) valikko on aina näkyvissä vaakarivissä

### 5. Fluid-typografia — `clamp()`
Otsikkojen fonttikoko skaalautuu automaattisesti näyttöleveyden mukaan
ilman mediakyselyjä:

```css
font-size: clamp(1.2rem, 4vw, 1.7rem);
/* min: 1.2rem | kasvaa viewportin mukaan | max: 1.7rem */
```

### 6. Viewport-yksiköt
Headerin korkeus määritetty `min-height: 30vh`, jolloin se skaalautuu
suhteessa näyttökorkeuden.

### 7. Responsiivinen kuvagalleria — `auto-fit` + `minmax`
Gallery-sivun kuvaruudukko mukautuu ilman mediakyselyjä:

```css
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
/* Mobiili: 1 sarake | Tabletti: 2 saraketta | Desktop: 3+ saraketta */
```

### 8. Responsiivinen lomake
- Mobiililla lomake on täysleveä
- Tabletilla ja pöytätietokoneella rajattu `max-width: 500px`:lla
- `:focus`- ja `:hover`-tehosteet säilytetty WS03:sta

### 9. Semanttinen rakenne (kuten WS04)
`<header>`, `<nav>`, `<aside>`, `<main>`, `<footer>`

### 10. CSS-tehosteet WS03:sta säilytetty
- `@keyframes`-animaatio bannerissa
- Kuvien grayscale → väri hover-siirtymä
- Listausten `:nth-child`-väritys
- `::before` / `::after` otsikoissa
- `::first-letter`-suuraakkonen

## Kansiorakenne

```text
WS05_Responsive_Design/
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

## Oppimistavoitteet

Tämän harjoituksen jälkeen opiskelija osaa:
- Lisätä viewport-metatägin ja selittää sen tarkoituksen
- Kirjoittaa CSS:n mobile-first-periaatteella
- Käyttää `@media`-kyselyjä taiton muuttamiseen eri näyttöko'oilla
- Toteuttaa CSS-only hamburger-valikon ilman JavaScriptiä
- Skaalata typografian `clamp()`-funktiolla
- Rakentaa automaattisesti muotoutuvan kuvagallerian `auto-fit` + `minmax`:lla
- Käyttää viewport-yksiköitä (`vh`, `vw`) suhteelliseen kokoon
