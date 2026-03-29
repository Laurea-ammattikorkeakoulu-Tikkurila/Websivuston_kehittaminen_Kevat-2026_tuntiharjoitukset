# WS02: CSS perusteet - tuntiharjoitus

Tässä tuntiharjoituksessa tutustutaan CSS:n perusteisiin ja siihen, miten sivun ulkoasu muuttuu selkeammaksi ja visuaalisesti miellyttavammaksi pelkan HTML-rakenteen päälle lisatyn tyylin avulla.

## Mikä on CSS?

CSS (Cascading Style Sheets) on tyylikieli, jolla maaritellaan verkkosivun ulkoasu.
HTML kertoo mita sivulla on (esim. otsikko, kappale, kuva, linkki), ja CSS kertoo milta ne nayttavat (esim. vari, koko, fontti, valit, sijoittelu).

Lyhyesti:
- HTML = sisalto ja rakenne
- CSS = ulkoasu ja tyyli

## Miten CSS:aa kaytetaan?

CSS kirjoitetaan sääntöinä, joissa valitaan haluttu elementti (selector) ja annetaan sille tyyliominaisuuksia.

Esimerkki:

```css
h1 {
	color: #1f4e79;
	font-size: 2rem;
}
```

Ylla oleva sääntö muotoilee kaikki h1-otsikot sinertaviksi ja suuremmiksi.

## Missa CSS voidaan maaritella?

1. Ulkoisessa tyylitiedostossa (suositeltu tapa), esim. `styles/style.css`
2. HTML-tiedoston `<style>`-osion sisalla. TÄmä on kaytannollista, jos halutaan maaritella vain muutama tyyli yhdelle sivulle. <stye> elementti sijoitetaan HTML-tiedoston `<head>`-osion sisalle.
3. Suoraan elementin `style`-attribuutissa

Yleensä käytetään ulkoista tyylitiedostoa, koska se pitaa koodin selkeana ja helpottaa yllapitoa.

## Mita tässä harjoituksessa opitaan?

Tavoitteena on harjoitella yleisimpiä CSS-muotoiluja, kuten:
- tekstin vari ja fontti
- taustavarit
- marginaalit ja sisamarginaalit
- reunukset
- elementtien leveydet ja sijoittelu

Kun samoille HTML-elementeille lisataan CSS-saantoja, sivun ulkoasu muuttuu nopeasti huomattavasti selkeammaksi ja ammattimaisemmaksi.

## Yhteenveto

CSS on verkkosivun ulkoasun perusta. Sen avulla voit erottaa sisallon (HTML) ja ulkoasun (CSS), jolloin sivujen rakentaminen, muokkaaminen ja yllapito on helpompaa.
