# WS03: CSS edistyneet ominaisuudet - tuntiharjoitus

Tässä tuntiharjoituksessa tutustutaan CSS:n edistyneisiin ominaisuuksiin: animaatioihin, siirtymiin, pseudo-luokkiin, pseudo-elementteihin ja suodattimiin.

## Harjoituksen tiedostot

- `index.html` — HTML-sivu, joka sisältää otsikon, animoidun bannerin, kappaleen, kuvan, järjestetyn ja järjestämättömän listan sekä lomakkeen
- `styles/style.css` — ulkoinen tyylitiedosto, joka hyödyntää edistyneitä CSS-ominaisuuksia
- `images/` — harjoituksessa käytetty kuva

## Mitä tässä harjoituksessa opitaan?

Harjoituksessa käytännössä sovelletaan seuraavia CSS:n edistyneitä ominaisuuksia:

### CSS Animation (animaatio)

CSS-animaatio koostuu kahdesta osasta: `@keyframes`-säännöstä ja `animation`-ominaisuudesta.

```css
@keyframes slideInDown {
    from { transform: translateY(-40px); opacity: 0; }
    to   { transform: translateY(0);     opacity: 1; }
}

.animated-banner {
    animation: slideInDown 0.8s ease-out forwards;
}
```

- `@keyframes` määrittelee animaation alku- ja lopputilan
- `animation-name` viittaa `@keyframes`-säännön nimeen
- `animation-duration` asettaa keston
- `animation-fill-mode: forwards` pitää elementin loppuasennossa animaation jälkeen

**Ero `transition`-ominaisuuteen:** `transition` käynnistyy vain tilamuutoksesta (esim. `:hover`), `animation` käynnistyy automaattisesti.

### CSS Transition (siirtymäanimaatio)

`transition`-ominaisuuden avulla elementtien tilamuutoksista tulee sileitä animaatioita sen sijaan, että ne tapahtuisivat välittömästi.

```css
img {
    transition: all 0.5s ease-in-out;
}
```

- `all` — animaatio koskee kaikkia muuttuvia ominaisuuksia (mukaan lukien `filter`)
- `0.5s` — siirtymän kesto on 0,5 sekuntia
- `ease-in-out` — animaatio alkaa hitaasti, nopeutuu keskellä ja hidastuu lopussa

### CSS Filter (suodattimet)

`filter`-ominaisuudella voidaan soveltaa visuaalisia efektejä elementtiin suoraan CSS:ssä.

```css
img {
    filter: grayscale(100%) brightness(80%);
}

img:hover {
    filter: none;
}
```

- `grayscale(100%)` — muuttaa kuvan täysin harmaasävyiseksi
- `brightness(80%)` — himmentää kuvan kirkkautta 80 %:iin
- `filter: none` — poistaa kaikki suodattimet (käytetään hover-tilassa)
- Muita suodattimia: `blur()`, `contrast()`, `sepia()`, `hue-rotate()`, `opacity()`

Useita suodattimia voi ketjuttaa välilyönnillä erotettuna: `filter: grayscale(50%) blur(2px);`

### CSS Pseudo-luokat (pseudo-classes)

Pseudo-luokka valitsee elementin tietyssä tilassa tai rakenteellisen asemansa perusteella. Kirjoitetaan yhdellä kaksoispisteellä: `elementti:pseudo-luokka`.

| Pseudo-luokka | Käyttö tässä harjoituksessa |
|---|---|
| `:hover` | Kuvan suurentaminen ja värin palautus, napin tummentaminen |
| `:focus` | Lomakekentän reunuksen korostus, kun kenttä on aktiivisena |
| `:nth-child(odd/even)` | Järjestetyn listan raidoitus |
| `:first-child` | Järjestämättömän listan ensimmäinen kohta kultaisena |
| `:last-child` | Järjestämättömän listan viimeinen kohta kursivoituna |

### CSS Pseudo-elementit (pseudo-elements)

Pseudo-elementti viittaa elementin tiettyyn osaan tai lisää uutta sisältöä HTML-koodia muuttamatta. Kirjoitetaan kahdella kaksoispisteellä: `elementti::pseudo-elementti`.

| Pseudo-elementti | Käyttö tässä harjoituksessa |
|---|---|
| `::before` | `▸`-symboli h2-otsikoiden eteen automaattisesti |
| `::after` | Sininen korostusviiva h2-otsikoiden alle |
| `::first-letter` | Kappaleen ensimmäinen kirjain suurena drop cap -tyyliin |

`::before` ja `::after` vaativat aina `content`-ominaisuuden (voi olla myös tyhjä `""`).

### CSS Transform

`transform`-ominaisuudella voidaan siirtää, skaalata tai kiertää elementtiä muuttamatta sivun muuta rakennetta.

- `scale(1.1)` — suurentaa elementin 110 %:iin alkuperäisestä koosta (käytetään `img:hover`-tilassa)
- `translateY(-40px)` — siirtää elementtiä 40 px ylöspäin (käytetään `@keyframes`-animaatiossa)

### Box Shadow (varjostus)

`box-shadow` lisää elementille varjon, joka tekee siitä visuaalisesti erottuvamman.

```css
box-shadow: 4px 4px 12px rgba(0, 0, 0, 0.2);
```

- Ensimmäiset kaksi arvoa määrittävät varjon sijainnin vaakasuunnassa ja pystysuunnassa
- Kolmas arvo on varjon pehmeysalue (blur)
- `rgba()` määrittää värin ja läpinäkyvyyden

### Lomakkeen muotoilu

Lomakkeelle ja sen kentille on määritelty tyylit, jotka tekevät siitä siistimmän ja käyttäjäystävällisemmän:

- Valkoinen kortti-ulkoasu reunuksella ja varjolla
- Kenttien otsikot (`label`) näytetään omalla rivillään
- Teksti- ja sähköpostikentät täyttävät koko leveyden
- `:focus`-pseudo-luokka korostaa aktiivisen kentän
- Submit-napille oma tyyli ja `:hover`-tila

### CSS:n kolme kirjoituspaikkaa

Tässä harjoituksessa CSS on kirjoitettu kaikkiin kolmeen paikkaan:

1. **Ulkoinen tyylitiedosto** `styles/style.css` — pääasiallinen paikka
2. **`<style>`-elementti** HTML-tiedoston `<head>`-osiossa — listaelementtien (`li`) tyyli
3. **`style`-attribuutti** suoraan elementissä — h1-otsikon väri

## Yhteenveto

Edistyneiden CSS-ominaisuuksien avulla verkkosivuille voidaan lisätä interaktiivisuutta ja visuaalista kiinnostavuutta ilman JavaScript-koodia. Animaatiot, suodattimet, pseudo-luokat ja pseudo-elementit tekevät sivusta dynaamisemman ja miellyttävämmän käyttää.

---

*Tämän tiedoston sisältö on luotu GitHub Copilot -tekoälyavustajan avulla.*
