# WS04_Page_layout – Sivuasettelu CSS Grid- ja Flexbox-menetelmillä

Tämä harjoitus laajentaa WS03:n edistyneen CSS:n moniosaisen sivuston rakentamiseen
yhtenäisellä sivuasettelulla.

## Mitä on toteutettu

1. Moniosainen sivusto
- Etusivu: `index.html`
- Kuvagalleria: `gallery.html`
- Yhteystiedot: `contact.html`

2. Yhteinen semanttinen rakenne jokaisella sivulla
- `<header>` — sivun otsikko ja banneri
- `<nav>` — sivuston navigaatio
- `<aside>` — sivupalkki, täydentävä sisältö
- `<main>` — sivun pääsisältö
- `<footer>` — alatunniste

3. CSS Grid sivurakenteessa
- Sisältöalue on toteutettu kaksipalstaisena asetteluna:
  - Vasen sarake: sivupalkki (`<aside>`)
  - Oikea sarake: pääsisältö (`<main>`)

4. Flexbox navigaatiossa
- Ylänavigaatio on rakennettu Flexboxilla linkkien vaakasuuntaista tasausta ja välejä varten.

5. WS03:n edistyneet CSS-ominaisuudet säilytetty ja laajennettu
- `@keyframes`-animaatio bannerissa
- Hover-siirtymät kuvissa
- Tyylitellyt listat pseudoluokilla (`:nth-child`, `:first-child`, `:last-child`)
- Pseudoelementit (`::before`, `::after`, `::first-letter`)
- Tyylitelty lomake focus- ja hover-tiloilla

6. Sivupalkin sisältö päivitetty
- Sivuasettelun peruskäsitteiden selitys
- Semanttisten elementtien yhteenveto
- Linkit ulkoisiin oppimislähteisiin:
  - W3Schools CSS Flexbox
  - W3Schools CSS Grid

## Kansiorakenne

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

## Oppimistavoitteet

Tämän harjoituksen jälkeen opiskelija osaa:
- Rakentaa moniosaisen sivuston yhteisellä asettelulla
- Käyttää semanttista HTML-rakennetta selkeästi
- Soveltaa CSS Gridiä sivun ylätason asetteluun
- Soveltaa Flexboxia komponenttitason asetteluun
- Pitää tyylit uudelleenkäytettävinä yhdellä ulkoisella tyylitiedostolla
