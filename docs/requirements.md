# Vaatimusmäärittely

Tila: luonnos. Perustuu asiakashaastattelu pohjaan.

## Tausta

Asiakas haluaa IMDb-tyylisen elokuvapalvelun, jonka erottava tekijä on yhteisöllisyys: käyttäjät arvostelevat elokuvia, tekevät listoja ja toimivat ryhmissä yhdessä kavereiden kanssa. Asiakas ei tunne teknistä toteutusta, joten asiat selitetään katselmoinnissa selkeästi.

## Käyttäjäroolit

- Vierailija: selaa elokuvia, lukee arvosteluja, katsoo jaettuja listoja
- Käyttäjä: kirjautunut, arvostelee, tekee listoja, liittyy ryhmiin
- Kaveri: käyttäjä, joka on liittynyt samaan ryhmään
- Ryhmän ylläpitäjä: hallinnoi omaa ryhmäänsä
- Moderaattori: poistaa sopimatonta sisältöä
- Ylläpitäjä (admin): hallinoi käyttäjiä, elokuvia ja moderaattoreita

## Prioriteetit

Priot on ryhmän ehdotus (must/should/could).

## Toiminnalliset vaatimukset

### Käyttäjänhallinta

| ID | Vaatimus | Prioriteetti | Tila |
|----|----------|--------------|------|
| F1 | Rekisteröityminen ja kirjautuminen käyttäjätunnuksella ja salasanalla | must | ehdotettu |
| F2 | Käyttäjä valitsee itse käyttäjänimen | must | ehdotettu |
| F3 | Oma käyttäjäsivu: omat arvostelut ja milloin on katsonut mitäkin | must | ehdotettu |
| F4 | Kaksivaiheinen tunnistautuminen, helppokäyttöinen | should | ehdotettu |

### Elokuvat ja haku

| ID | Vaatimus | Prioriteetti | Tila |
|----|----------|--------------|------|
| F5 | Elokuvien perustiedot (kuvaus, julisteet yms.) haetaan ulkoisesta elokuvatietokanta-rajapinnasta | must | ehdotettu |
| F6 | Haku ja hakuehdot: nimi, näyttelijät, ohjaaja yms. | must | ehdotettu |
| F7 | Etusivulla ajankohtaisia elokuvia | should | ehdotettu |
| F8 | Admin voi lisätä elokuvia tarvittaessa | should | ehdotettu |
| F9 | Suositukset, jotka eivät ole aina samanlaisia | could | ehdotettu |
| F10 | Suositukset aiempien valintojen perusteella | could | ehdotettu |
| F11 | Elokuvateatterit ja näytösajat (esim. viikonlopun tarjonta), kuten Finnkinossa | could | ehdotettu |

### Arvostelut

| ID | Vaatimus | Prioriteetti | Tila |
|----|----------|--------------|------|
| F12 | Tähtiarvostelu asteikolla 1-5 | must | ehdotettu |
| F13 | Tekstiarvostelu, pituutta ei rajata | must | ehdotettu |
| F14 | Arvostelun voi tehdä vain kirjautunut käyttäjä | must | ehdotettu |
| F15 | Arvostelut ovat kaikkien luettavissa | must | ehdotettu |
| F16 | Kirjoittaja päättää, onko arvostelu julkinen vai näkyykö se vain ryhmälle | should | ehdotettu |
| F17 | Kavereiden arvostelut nostetaan esiin tuntemattomien edelle | should | ehdotettu |

### Listat

| ID | Vaatimus | Prioriteetti | Tila |
|----|----------|--------------|------|
| F18 | Toivelista: elokuvat, jotka haluaa nähdä mutta ei ole katsonut | must | ehdotettu |
| F19 | Vakiolista: vanhat suosikit | must | ehdotettu |
| F20 | Listan jakaminen linkillä, katselu ei vaadi käyttäjätunnusta | must | ehdotettu |
| F21 | Listoilla on nimi, ja listoja voi hakea | should | ehdotettu |
| F22 | Listan jakaminen ryhmän sisällä ilman linkkiä | should | ehdotettu |
| F23 | Ryhmän yhteinen lista, jota vain ryhmän ylläpitäjä voi muokata | should | ehdotettu |

### Ryhmät

| ID | Vaatimus | Prioriteetti | Tila |
|----|----------|--------------|------|
| F24 | Ryhmän luonti, ryhmällä oma sivu ja näkyvä jäsenmäärä | must | ehdotettu |
| F25 | Ryhmät-osio näkyvillä, julkinen ja yksityinen ryhmä, liittymismahdollisuus | must | ehdotettu |
| F26 | Ryhmän ylläpitäjä ja moderaattori-rooli | must | ehdotettu |
| F27 | Jos ryhmän ainoa ylläpitäjä poistuu, ylläpito siirtyy automaattisesti toiselle jäsenelle | should | ehdotettu |
| F28 | Kaverin ryhmät näkyvät muille kavereille, eivät kaikille | should | ehdotettu |
| F29 | Ryhmän chat | could | ehdotettu |

### Moderointi

| ID | Vaatimus | Prioriteetti | Tila |
|----|----------|--------------|------|
| F30 | Moderaattori ja admin voivat poistaa sopimattomia arvosteluja | must | ehdotettu |

## Ei-toiminnalliset vaatimukset

| ID | Vaatimus | Prioriteetti | Tila |
|----|----------|--------------|------|
| N1 | Sovellus julkaistaan Azureen | must | ehdotettu |
| N2 | Tietoturva best practice -tasolla: rate limiting, XSS-suojaus, CSP | must | ehdotettu |
| N3 | Hyvä käytettävyys, ei ponnahdusikkunoita | must | ehdotettu |
| N4 | Asiallinen ulkoasu, värimaailmaa ei ole määritelty | must | ehdotettu |
| N5 | Mobiilinavigaatio ja responsiivinen CSS | must | ehdotettu |
| N6 | Kieli aluksi suomi | must | ehdotettu |
| N7 | Englanti tarvittaessa | could | ehdotettu |
| N8 | Ruotsi (asiakas mainitsi, tarve epäselvä) | could | ehdotettu |

## Rajaukset

- Maksulliset lisäominaisuudet: ei vaatimus tässä projektissa
- Kaikkea ei ehditä toteuttamaan 8 viikossa, tarkennetaan tätä vielä

## Avoimet kysymykset asiakkaalle

- Mikä on "kaveri"? Erillinen kaverisuhde vai riittääkö, että ollaan samassa ryhmässä?
  - Riittää omassa ryhmässä
- Mitä elokuvatietokantaa käytetään ensisijaisesti (esim. TMDB), ja onko muita lähteitä?
  - tutkitaan
- Mistä näytösajat haetaan (esim. Finnkinon rajapinta), ja riittääkö Finnkino?
  - tutkitaan
- Onko ryhmächat pakollinen vai toive, koska se on iso toteutus?
  - Tämä on toive
- Tarvitaanko 2FA ensimmäiseen versioon?
  - mietitään myöhemmin
- Vahvistaako asiakas must/should/could-jaon?
  - mietitään myöhemmin
