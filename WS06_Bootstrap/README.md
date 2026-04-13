# WS06_Bootstrap – Bootstrap-kehys

Tämä harjoitus laajentaa WS05:n responsiivisen suunnittelun periaatteet käyttämällä
Bootstrap 5 -kehystä. Vertaamme, miten Bootstrap korvaa tai täydentää omia CSS-ratkaisujamme.

## Mitä on toteutettu

### 1. Neliosainen sivusto
- Etusivu: `index.html`
- Kuvagalleria: `gallery.html`
- Yhteystiedot: `contact.html`
- Tietoa Bootstrap-kehyksestä: `info.html`

### 2. Bootstrap 5 CDN
Bootstrap ladataan CDN:stä — ei paikallisia tiedostoja eikä build-työkaluja:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
```

### 3. Bootstrap Grid -järjestelmä
Bootstrap korvaa WS04–WS05:n CSS Grid- ja Flexbox-pohjaisen asettelun:
- `container` → sivun maksimileveys ja keskitys
- `row` → rivit
- `col-*`, `col-sm-*`, `col-md-*` → sarakkeet eri näytöillä

### 4. Responsiivinen navigaatio
Bootstrap `navbar`-komponentti korvaa WS05:n CSS-only checkbox-hamburger-valikon.
JavaScript-pohjainen `navbar-toggler` toimii kaikilla laitteilla.

### 5. Kortit (Cards)
Bootstrap `card`-komponentti korvaa WS04–WS05:n käsin tehdyn korttityylin.

### 6. Lomake-komponentit
Bootstrap `form-control`, `form-label` ja `btn`-luokat korvaavat omia lomaketyylimme.

### 7. Accordioni (info.html)
Bootstrap Accordion -komponentti näyttää tietoa Bootstrap-kehyksestä laajennetuissa osioissa.
Toimii Bootstrapin JS-bundlen avulla.

### 8. Utility-luokat
Bootstrap tarjoaa kattavan jogurttijoukko utility-luokkia:
`mt-*`, `mb-*`, `py-*`, `px-*`, `text-center`, `d-flex`, `gap-*`, `rounded`, `shadow-sm`

### 9. Mukautettu CSS (styles/style.css)
Pieni `style.css`-tiedosto sisältää värimuutoksia ja muutamia Bootstrap-ylikirjoituksia —
kaikki muu tulee suoraan Bootstrapista.

## Kansiorakenne

```
WS06_Bootstrap/
├── README.md
└── tuntiharjoitus/
    ├── README.md
    ├── index.html
    ├── gallery.html
    ├── contact.html
    ├── info.html
    ├── images/
    │   ├── Berfin.jpg
    │   └── Jari_Hki.JPG
    └── styles/
        └── style.css
```
