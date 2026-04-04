# WS03: CSS edistyneet ominaisuudet - tuntiharjoitus

Tässä tuntiharjoituksessa tutustutaan CSS:n edistyneisiin ominaisuuksiin, kuten siirtymäanimaatioihin, hover-tiloihin, varjostuksiin ja lomakkeiden muotoiluun.

## Harjoituksen tiedostot

- `index.html` — HTML-sivu, joka sisältää otsikon, kappaleen, kuvan, järjestetyn ja järjestämättömän listan sekä lomakkeen
- `styles/style.css` — ulkoinen tyylitiedosto, joka hyödyntää edistyneitä CSS-ominaisuuksia
- `images/` — harjoituksessa käytetty kuva

## Mitä tässä harjoituksessa opitaan?

Harjoituksessa käytännössä sovelletaan seuraavia CSS:n edistyneitä ominaisuuksia:

### CSS Transition (siirtymäanimaatio)

`transition`-ominaisuuden avulla elementtien tilamuutoksista tulee sileitä animaatioita sen sijaan, että ne tapahtuisivat välittömästi.

Esimerkki tässä harjoituksessa:

```css
img {
    transition: all 0.3s ease-in-out;
}
```

- `all` — animaatio koskee kaikkia muuttuvia ominaisuuksia
- `0.3s` — siirtymän kesto on 0,3 sekuntia
- `ease-in-out` — animaatio alkaa hitaasti, nopeutuu keskellä ja hidastuu lopussa

### Pseudo-luokka :hover

`:hover`-pseudo-luokan avulla voidaan määrittää elementille tyyli, joka aktivoituu, kun käyttäjä vie hiiren sen päälle.

Esimerkki tässä harjoituksessa:

```css
img:hover {
    transform: scale(1.1);
    box-shadow: 8px 8px 20px rgba(0, 0, 0, 0.4);
}
```

Kuva suurenee 10 % ja sen varjo kasvaa, kun hiiri viedään kuvan päälle.

### CSS Transform

`transform`-ominaisuudella voidaan siirtää, skaalata tai kiertää elementtiä muuttamatta sivun muuta rakennetta.

- `scale(1.1)` — suurentaa elementin 110 %:iin alkuperäisestä koosta

### Box Shadow (varjostus)

`box-shadow` lisää elementille varjon, joka tekee siitä visuaalisesti erottuvamman.

```css
box-shadow: 4px 4px 12px rgba(0, 0, 0, 0.2);
```

- Ensimmäiset kaksi arvoa määrittävät varjon sijainnin vaakasuunnassa ja pystysuunnassa
- Kolmas arvo on varjon pehmeysalue (blur)
- `rgba()` määrittää värin ja läpinäkyvyyden

### Lomakkeen muotoilu

Lomakkeelle ja sen kentille on määritelty omat tyylit, jotka tekevät siitä siistimmän ja käyttäjäystävällisemmän:

- Valkoinen kortti-ulkoasu reunuksella ja varjolla
- Kenttien otsikot (`label`) näytetään omalla rivillään
- Teksti- ja sähköpostikentät täyttävät koko leveyden, niissä on pehmuste ja pyöristetyt kulmat

### CSS:n kolme kirjoituspaikkaa

Tässä harjoituksessa CSS on kirjoitettu kaikkiin kolmeen paikkaan:

1. **Ulkoinen tyylitiedosto** `styles/style.css` — pääasiallinen paikka
2. **`<style>`-elementti** HTML-tiedoston `<head>`-osiossa — listaelementtien (`li`) tyyli
3. **`style`-attribuutti** suoraan elementissä — h1-otsikon väri

## Yhteenveto

Edistyneiden CSS-ominaisuuksien avulla verkkosivuille voidaan lisätä interaktiivisuutta ja visuaalista kiinnostavuutta ilman JavaScript-koodia. Transitiot ja hover-tilat tekevät sivusta dynaamisemman ja miellyttävämmän käyttää.

## Huomio

Tämän README-tiedoston sisällön luomisessa on käytetty GitHub Copilotia.
