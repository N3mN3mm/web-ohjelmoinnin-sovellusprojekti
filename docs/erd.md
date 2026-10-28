# Tietokannan ERD (Entity-Relationship Diagram)

Tila: Luonnos

## Ydin: Käyttäjät, elokuvat, arvostelut

```mermaid
erDiagram
    USERS ||--o{ REVIEWS : kirjoittaa
    MOVIES ||--o{ REVIEWS : saa

    USERS {
        int id PK
        string username UK
        string email UK
        string password_hash
        string role "user, moderator, admin"
        timestamp created_at
    }
    MOVIES {
        int id PK
        int tmdb_id UK
    }
    REVIEWS {
        int id PK
        int user_id FK
        int movie_id FK
        int rating "1-5"
        text body
        string visibility "public, group"
        timestamp created_at
    }
```

## Suunnittelupäätökset (ryhmän ehdotus, ei vahvistettu)

- Elokuvan tiedot haetaan ulkoisesta rajapinnasta (F5), joten MOVIES tallentaa vain rajapinnan tunnisteen. Tällä paikallinen rivi toimii arvostelujen viiteavaimena.
- Globaali rooli on USERS-taulussa (user, moderator, admin). Ryhmäkohtaiset roolit tulevat ryhmien jäsentauluun myöhemmin.
- Yksi käyttäjä voi arvostella saman elokuvan vain kerran: lisätään UNIQUE (user_id, movie_id).

## Avoimet kysymykset

- Sähköposti (salasanan palautus): ryhmä päätti lisätä, koska salasanan palautus vaatii sen. Asiakkaalle ilmoitetaan katselmoinnissa. Samalla vaatimusmäärittelyyn kannattaa lisätä rivi, esim. F31 "Salasanan palautus sähköpostilla", jotta ERD:n email-kenttä vastaa vaatimusta.
- Jos arvostelu näkyy vain ryhmälle (F16), mille ryhmälle tarkalleen? Ratkaistaan, kun ryhmätaulut on piirretty.
