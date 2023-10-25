# Maven Analyticsin Queen's Gambit -haaste

Tein Maven Analyticsin [Queen's Gambit -haasteen](https://mavenanalytics.io/challenges/queen's-gambit-challenge/20), jossa oli tarkoitus tehdä yli 20 000 pelatun shakkipelin tietokannasta (määrittelemättömiä) analyyseja, mutta itse keskityin lähinnä tehtävän bonuskysymykseen.

Tehtävän ja bonuskysymyksen innoittajana oli vuoden 2020 Netflixin hittisarja "The Queen's Gambit", joka sai nimensä sarjassa pelatun viimeisen jakson päätösottelun mukaan, jossa päähenkilö, Elizabeth Harmon, aloitti pelin kuningatargambiitti-avauksella.

Kuningatargambiitti on kolmen siirron shakkiavaus (d4 d5 c4). Tehtävänä oli selvittää tietokannasta pelattujen pelien perusteella, mikä olisi paras vastasiirto, eli mustan toinen siirto tätä shakkiavausta vastaan.

Tehtävän lopullinen vastaus oli tarkoitus esittää esim. Power BI:n tai Tableaun yhden sivun "dashboardina", mutta tämän näytön vuoksi päädyin tekemään tehtävän Jupyter Notebookilla.

## Työvaiheet

Työvaiheet on kommentoitu myös itse muistikirjaan, mutta ohessa työvaiheista vähän laveammin.

1. Vaadittavien ohjelmakirjastojen tuonti Jupyteriin: **Pandas** tietojenkäsittelyä ja analysointia sekä **Matplotlib** grafiikkaa varten.
2. CSV-tiedoston lukeminen muistikirjaan. Jossain vaiheessa sain ajatusken konvertoida CSV-tiedoston SQL-muotoon, mutta lopetin sen käytön aika äkkiä siitä johtuvien ongelmien takia. Tuo SQLite-tietokanta löytyy kyllä repositoriosta myös.
3. DataFramen luominen ja tietotyyppien tarkistus.
4. Tietokannan yhtenäisyyden tarkistus. Toisin kuin muissa Maven Analyticsin haasteissa, tässä tietokannassa ei ollut käytännössä mitään korjattavaa. Siellä oli joitain puuttuvia tietoja esim. avausvariaatioista, mutta ei mitään sellaista, mikä olisi vaikuttanut varsinaiseen analyysiin. Myös tietotyypit olivat kunnossa. Varmistin vielä asian etsimällä kaksoiskappaleita ja tyhjiä tietueita tietokannasta, mutta se oli kunnossa myös siltä osin.
5. 
