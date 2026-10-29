# Vaatimusmäärittely

Tila: ns luonnos. Päivitetään tarkentuessa.

## Tausta

Asiakas haluaa sovelluksen/sivuston, jossa voi selata elokuvia, muodostaa ryhmiä, arvostella ja keskustella elokuvista. 

Tällä hetkellä on käytössä Whatssapp, jossa keskustelevat mielenkiintoisista elokuvista ja ehdottelevat kavereilleen tietoa. Heillä ei ole yhteistä sovellusta, mikä sopii heidän tarpeisiinsa.

(Tähän ongelmankuvaus ja projektin tavoite. Miksi tehdään ja mitä ratkaistaan.)

## Sidosryhmät ja käyttäjät

| Rooli | Tarve | Oikeudet |
|-------|-------|----------|
| Käyttäjä | Luo tunnukset ja voi tehdä arvosteluja | Oikeus nähdä elokuvien tiedot ja arvostelut sekä tehdä arvosteluja ja ryhmiä |
| Ryhmän ylläpitäjä | Voi perustaa ja hallinnoida ryhmää | Muokata ryhmän tietoja ja jäseniä |
| Admin | Pystyy hallinnoimaan verkkosivuja ja käyttäjiä | Oikeus tehdä muutoksia |

## Toiminnalliset vaatimukset

| ID | Vaatimus | Prioriteetti (must/should/could) | Tila |
|----|----------|----------------------------------|------|
| F1 | Henkilö voi rekisteröityä | must | ehdotettu |
| F2 | Kirjautuminen (käyttäjätunnus/salasana) | must | ehdotettu |
| F3 | Käyttäjän tiedot ei saa näkyä muille | must | ehdotettu |
| F4 | Käyttäjä valitsee itse käyttäjänimen | must | ehdotettu |
| F5 | Käyttäjän profiilissa näkyy suositukset, listat ja arvostelut | could | ehdotettu |
| F6 | Rekisteröity käyttäjä voi tehdä arvostelun | must | ehdotettu |
| F7 | Arvostelun tekijä voi itse päättää, kuka näkee julkaisun | should | ehdotettu |
| F8 | Arvostelu sanallisesti | must | ehdotettu |
| F9 | Arvostelu tähdillä | should | ehdotettu |
| F10 | Käyttäjätunnuksen voi poistaa | must | ehdotettu |
| F11 | Käyttäjä voi liittyä ryhmiin | must | ehdotettu |
| F12 | Näkyvyys arvostelun ajankohdasta ja tekijästä | could | ehdotettu |

| F13 | Elokuvien perustiedot (kuvaus, julisteet yms.) haetaan ulkoisesta elokuvatietokanta-rajapinnasta | must | ehdotettu |
| F14 | Mahdollisuus hakea elokuvia | must | ehdotettu |
| F15 | Haun voi tehdä eriperusteille esim. näyttelijä, genre | must | ehdotettu |
| F16 | Elokuvista näkyy leffateatteri ja näytösajat muutamalta paikkakunnalta | could | ehdotettu |
| F17 | Käyttäjä voi tehdä listan | must | ehdotettu |
| F18 | Elokuvalistan voi jakaa linkillä, ei tarvitse käyttäjätunnusta | must | ehdotettu |

| F19 | Ryhmien muodostaminen ja nimeäminen | must |  ehdotettu |
| F20 | Ryhmän sisällä useammalle voi antaa oikeudet muuttaa ryhmän tietoja | could | ehdotettu |
| F21 | Ryhmät voi tehdä omia listoja | should | ehdotettu |
| F22 | Julkisia ryhmiä | should | ehdotettu |
| F23 | Selata ryhmiä | could | ehdotettu |
| F24 | Kuka tahansa ei voi liittyä ryhmään/hyväksyntä liittymiselle | should | ehdotettu |
| F25 | Ryhmällä on oma sivu ja siinä näkyy ryhmän suosikit| must | ehdotettu |
| F26 | Ryhmästä voi poistua ja ryhmän ylläpitäjä voi poistaa jäseniä | must | ehdotettu |
| F27 | Ryhmän sisäiset arvostelut ryhmässä | could | ehdotettu |
| F28 | Keskusteluominaisuus | should | ehdotettu |
| F29 | Elokuvaehdotuksia | could | ehdotettu |

| F30 | Sopii mobiiliversiolle | must | ehdotettu |
| F31 | Elokuvalistan voi jakaa linkillä, ei tarvitse käyttäjätunnusta | must | ehdotettu |
| F32 | Tilastotietoa elokuvista | could | ehdotettu |
| F33 | Älykkäitä toimintoja | could | ehdotettu |
| F34 | Maksullisuus | could | ehdotettu |


## Ei-toiminnalliset vaatimukset

| ID | Vaatimus | Tila |
|----|----------|------|
| N1 | Sovellus on julkaistu Azureen | ehdotettu |
| N2 | Elokuvat on listattu lyhyellä infolla | ehdotettu |
| N3 | Ryhmän sisäiset arvostelut näkyy kavereille | ehdotettu |
| N4 | Ulkoasu asiallinen ja selkeä | ehdotettu |
| N5 | Hyvä käytännöllisyys ilman kirjautumista ja ponnahdusikkunaa | ehdotettu |
| N6 | Kielet | ehdotettu |

## Tietoturva vaatimukset

| ID | Vaatimus | Prioriteetti (must/should/could) | Tila |
|----|----------|----------------------------------|------|
| S1 | Salaisuudet (tietokanta-URL, API-avaimet) ympäristömuuttujina, ei GitHubissa | must | ehdotettu |
| S2 | Rate limiting kirjautumiseen ja rekisteröitymiseen | must | ehdotettu |
| S3 | Oikeudet tarkistetaan palvelimella: roolit (käyttäjä, ryhmän ylläpitäjä, moderaattori, admin) ja yksityisen ryhmän sisältö vain jäsenille | must | ehdotettu |
| S4 | Kaksivaiheinen tunnistautuminen, helppokäyttöinen | must | ehdotettu |
| S5 | XSS-suojaus: Käyttäjän syöttämä sisältö (arvostelut, listojen nimet, chat) käsitellään turvallisesti | must | ehdotettu |

## Rajaukset

Ei toteuteta maksullisuus ominaisuutta. Työskennellään korkeimman priotiteetin mukaan. Prioriteetit määritellään asiakkaan toiveisen mukaan.

## Avoimet kysymykset asiakkaalle

- Mitä elokuvatietokantaa käytetään ensisijaisesti (esim. TMDB), ja onko muita lähteitä? tutkitaan
- Mistä näytösajat haetaan (esim. Finnkinon rajapinta), ja riittääkö Finnkino. Halutaan useammpi elokuvateatteri ja muutamalta paikkakunnalta esim. Oulu, Tampere, Helsinki
- Onko ryhmächat pakollinen vai toive, koska se on iso toteutus? Tämä on toive
- Tarvitaanko 2FA ensimmäiseen versioon? mietitään myöhemmin
- Vahvistaako asiakas must/should/could-jaon? mietitään myöhemmin
- Halutaanko käyttäjänsähköposti käyttäjätunnuksien palautukseen. Kyllä
