# WS02: CSS perusteet - tuntiharjoitus

Tässä tuntiharjoituksessa tutustutaan CSS:n perusteisiin ja siihen, miten sivun ulkoasu muuttuu selkeämmäksi ja visuaalisesti miellyttävämmäksi, kun pelkän HTML-rakenteen päälle lisätään tyyliä.

## Harjoituksen tiedostot

Kansiossa on kaksi HTML-tiedostoa:
- index1.html = sivun perusversio ilman CSS-muotoiluja
- index2.html = sama sivu CSS:n avulla muotoiltuna

Lisäksi käytössä on erillinen tyylitiedosto:
- styles/style.css = ulkoiset CSS-säännöt, joita index2 hyödyntää

Vertaa index1- ja index2-tiedostoja keskenään. Näet konkreettisesti, miten samat HTML-elementit näyttävät hyvin erilaisilta, kun niihin lisätään CSS-muotoilua.

## Mikä on CSS?

CSS (Cascading Style Sheets) on tyylikieli, jolla maaritellaan verkkosivun ulkoasu.
HTML kertoo mita sivulla on (esim. otsikko, kappale, kuva, linkki), ja CSS kertoo milta ne nayttavat (esim. vari, koko, fontti, valit, sijoittelu).

Lyhyesti:
- HTML = sisalto ja rakenne
- CSS = ulkoasu ja tyyli

## Miten CSS:ää käytetään?

CSS kirjoitetaan sääntöinä, joissa valitaan haluttu elementti (selector) ja annetaan sille tyyliominaisuuksia.

Esimerkki:

```css
h1 {
	color: #1f4e79;
	font-size: 2rem;
}
```

Yllä oleva sääntö muotoilee kaikki h1-otsikot sinertäviksi ja suuremmiksi.

## Missä CSS voidaan määritellä?

1. Ulkoisessa tyylitiedostossa (suositeltu tapa), esim. `styles/style.css`
2. HTML-tiedoston `<style>`-osion sisällä. Tämä on käytännöllistä, jos halutaan määritellä vain muutama tyyli yhdelle sivulle. `<style>`-elementti sijoitetaan HTML-tiedoston `<head>`-osion sisälle.
3. Suoraan elementin `style`-attribuutissa

Yleensä käytetään ulkoista tyylitiedostoa, koska se pitää koodin selkeänä ja helpottaa ylläpitoa.

## Mitä tässä harjoituksessa opitaan?

Tavoitteena on harjoitella yleisimpiä CSS-muotoiluja, kuten:
- tekstin vari ja fontti
- taustavarit
- marginaalit ja sisamarginaalit
- reunukset
- elementtien leveydet ja sijoittelu

Kun samoille HTML-elementeille lisätään CSS-sääntöjä, sivun ulkoasu muuttuu nopeasti huomattavasti selkeämmäksi ja ammattimaisemmaksi.

## Yhteenveto

CSS on verkkosivun ulkoasun perusta. Sen avulla voit erottaa sisällön (HTML) ja ulkoasun (CSS), jolloin sivujen rakentaminen, muokkaaminen ja ylläpito on helpompaa.

## Huomio

Tämän README-tiedoston sisällön luomisessa on käytetty GitHub Copilotia.
