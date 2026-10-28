# Vaatimusmäärittely

Tila: ns luonnos. Päivitetään tarkentuessa.

## Tausta

Asiakas haluaa sovelluksen/sivuston, jossa voi selata elokuvia, muodostaa ryhmiä, arvostella ja keskustella elokuvista. 

Tällä hetkellä on käytössä Whatssapp, jossa keskustelevat mielenkiintoisista elokuvista ja ehdottelevat kavereilleen tietoa. Heillä ei ole yhteistä sovellusta, mikä sopii heidän tarpeisiinsa.

(Tähän ongelmankuvaus ja projektin tavoite. Miksi tehdään ja mitä ratkaistaan.)

## Sidosryhmät ja käyttäjät

| Rooli | Tarve | Oikeudet |
|----|----------|----------------------------------|------|
| Käyttäjä | Luo tunnukset ja voi tehdä arvosteluja | Oikeus nähdä elokuvien tiedot ja arvostelut sekä tehdä arvosteluja ja ryhmiä |
| Ryhmän ylläpitäjä | Voi perustaa ja hallinnoida ryhmää | Muokata ryhmän tietoja ja jäseniä |
| Admin | Pystyy hallinnoimaan verkkosivuja ja käyttäjiä | Oikeus tehdä muutoksia |

## Toiminnalliset vaatimukset

| ID | Vaatimus | Prioriteetti (must/should/could) | Tila |
|----|----------|----------------------------------|------|
| F1 | Kirjautuminen (käyttäjätunnus/salasana) | must | ehdotettu |
| F2 | Arvostelu sanallisesti | must | ehdotettu |
| F3 | Arvostelu tähdillä | should | ehdotettu |
| F4 | Ryhmien muodostaminen ja nimeäminen | must |  ehdotettu |
| F5 | Elokuvien perustiedot (kuvaus, julisteet yms.) haetaan ulkoisesta elokuvatietokanta-rajapinnasta | must | ehdotettu |
| F6 | Käyttäjä voi tehdä listan | must | ehdotettu |
| F7 | Ryhmät voi tehdä omia listoja | should | ehdotettu |
| F8 | Julkisia ryhmiä | should | ehdotettu |
| F9 | Selata ryhmiä | could | ehdotettu |
| F10 | Rekisteröity käyttäjä voi kirjoittaa arvostelun | must | ehdotettu |
| F11 | Keskusteluominaisuus | should | ehdotettu |
| F12 | Mahdollisuus hakea elokuvia | must | ehdotettu |
| F13 | Haun voi tehdä eriperusteille esim. näyttelijä, genre | must | ehdotettu |
| F14 | Elokuvaehdotuksia | could | ehdotettu |
| F15 | Elokuvista näkyy leffateatteri ja näytösajat | should | ehdotettu |
| F16 | Sopii mobiiliversiolle | must | ehdotettu |
| F17 | Kuka tahansa ei voi liittyä ryhmään/hyväksyntä liittymiselle | should | ehdotettu |
| F18 | Käyttäjä voi liittyä ryhmiin | must | ehdotettu |
| F19 | Ryhmällä on oma sivu ja siinä näkyy ryhmän suosikit| must | ehdotettu |
| F20 | Ryhmästä voi poistua ja ryhmän ylläpitäjä voi poistaa jäseniä | must | ehdotettu |
| F21 | Elokuavlistan voi jakaa linkillä, ei tarvitse käyttäjätunnusta | must | ehdotettu |
| F22 | Ryhmän sisäiset arvostelut ryhmässä | could | ehdotettu |
| F23 | Näkyvyys asvostelun ajankohdasta ja tekijästä | could | ehdotettu |
| F24 | Arvostelun tekijä voi itse päättää, kuka näkee julkaisun | should | ehdotettu |
| F25 | Käyttäjän tiedot ei saa näkyä muille | must | ehdotettu |
| F26 | Käyttäjä valitsee itse käyttäjänimen | must | ehdotettu |
| F27 | Tilastotietoa elokuvista | could | ehdotettu |
| F28 | Älykkäitä toimintoja | could | ehdotettu |
| F29 | Maksullisuus | could | ehdotettu |
| F30 | Käyttäjän profiilissa näkyy suositukset, listat ja arvostelut | could | ehdotettu |
| F31 | Ryhmän sisällä useammalle voi antaa oikeudet muuttaa ryhmän tietoja | could | ehdotettu |
| F32 | Salaisuudet (tietokanta-URL, API-avaimet) ympäristömuuttujina, ei GitHubissa | must | ehdotettu |


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

- Mikä on "kaveri"? Erillinen kaverisuhde vai riittääkö, että ollaan samassa ryhmässä? Riittää omassa ryhmässä
- Mitä elokuvatietokantaa käytetään ensisijaisesti (esim. TMDB), ja onko muita lähteitä? tutkitaan
- Mistä näytösajat haetaan (esim. Finnkinon rajapinta), ja riittääkö Finnkino? tutkitaan
- Onko ryhmächat pakollinen vai toive, koska se on iso toteutus? Tämä on toive
- Tarvitaanko 2FA ensimmäiseen versioon? mietitään myöhemmin
- Vahvistaako asiakas must/should/could-jaon? mietitään myöhemmin
- Halutaanko käyttäjänsähköposti käyttäjätunnuksien palautukseen.
