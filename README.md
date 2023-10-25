# Maven Analyticsin Queen's Gambit -haaste

Tein Maven Analyticsin [Queen's Gambit -haasteen](https://mavenanalytics.io/challenges/queen's-gambit-challenge/20), jossa oli tarkoitus tehdä yli 20 000 pelatun shakkipelin tietokannasta (määrittelemättömiä) analyyseja, mutta itse keskityin lähinnä tehtävän bonuskysymykseen.

Tehtävän ja bonuskysymyksen innoittajana oli vuoden 2020 Netflixin hittisarja "The Queen's Gambit", joka sai nimensä sarjassa pelatun viimeisen jakson päätösottelun mukaan, jossa päähenkilö, Elizabeth Harmon, aloitti pelin kuningatargambiitti-avauksella.

Kuningatargambiitti on kolmen siirron shakkiavaus (d4 d5 c4). Tehtävänä oli selvittää tietokannasta pelattujen pelien perusteella, mikä olisi paras vastasiirto, eli mustan toinen siirto tätä shakkiavausta vastaan.

Tehtävän lopullinen vastaus oli tarkoitus esittää esim. Power BI:n tai Tableaun yhden sivun "dashboardina", mutta tämän näytön vuoksi päädyin tekemään tehtävän Jupyter Notebookilla.

Asensin Jupyter Notebookin ensin macOS-käyttöjärjestelmään, mutta siinä oleva oletus-Python (v. 2.7) aiheutti ongelmia polkujen kanssa alusta lähtien. Sain nuo myöhemmin kyllä korjattua, mutta siinä välissä olin asentanut Anaconda Navigator -ympäristön jo puhtaalle Windows-virtuaalikoneelle, jolla tein tehtävän loppuun.

## Työvaiheet

Työvaiheet on kommentoitu myös itse muistikirjaan, mutta ohessa työvaiheista vähän laveammin.

1. Vaadittavien ohjelmakirjastojen asentaminen conda-ympäristöön ja tuonti Jupyteriin: **Pandas** tietojenkäsittelyä ja analysointia sekä **Matplotlib** grafiikkaa varten.
2. CSV-tiedoston lukeminen muistikirjaan. Konvertoin CSV-tiedoston SQL-muotoon, koska ajattelin käyttää sitä ensin, mutta lopetin sen aika äkkiä siitä johtuvien ongelmien takia. Tuo SQLite-tietokanta löytyy kyllä repositoriosta myös.
3. DataFramen luominen ja tietotyyppien tarkistus.
4. Tietokannan yhtenäisyyden tarkistus. Toisin kuin joissain muissa Maven Analyticsin haasteissa, tässä tietokannassa ei ollut käytännössä mitään korjattavaa. Siellä oli joitain puuttuvia tietoja esim. avausvariaatioista, mutta ei mitään sellaista, mikä olisi vaikuttanut varsinaiseen analyysiin. Myös tietotyypit olivat kunnossa. Varmistin vielä asiaa etsimällä kaksoiskappaleita ja tyhjiä tietueita tietokannasta, mutta se oli kunnossa myös niiltä osin.
5. Ympyräkaavion luominen voittojen jakautumasta (valkoinen/musta/tasapeli). En ollut ennen käyttänyt Matplotlibia ja kyllä kaikenlaiset grafiikan muokkaamiset ovat äärimmäisen kankeita verrattuna em. BI-ohjelmiin. Myös yritykseni muuttaa desimaalierotin pilkuksi kaatoi koko Jupyter Notebookin (ja hävitti samalla kaikki siihen asti tallentamattomat työt), joten jätin sen suosiolla pisteeksi.
6. Ympyräkaavion luominen voitetuista peleistä pelaajan Elo-luvun mukaan, eli kuinka usein pelin on voittanut se, jolla on parempi tai huonompi Elo-luku.
7. Pylväskaavion luominen eniten voittoon johtaneista shakkiavauksista. Paremman analyysin kannalta, olisi varmaan ollut aiheellista suhteuttaa myös nuo voitokkaat shakkiavaukset siihen, paljonko niitä on käytetty, mutta jätin sen nyt tuolleensa.
   
## Queen's Gambit -haaste

Viimeisen vastauksen tein vähän osissa, josta tietenkin näkee tuon prosessin ja kyllähän tuo sen vastauksenkin antaa, mutta tein vielä viimeisen kohdan, jossa yhdistin nuo kaikki yhteen vastaukseen. Eli jos valkoinen aloittaa kuningatargambiitilla, tarkastellaan ensin kaikkia pelejä, joissa valkoinen on hävinnyt (näitä oli 58 kpl 168 kpl:sta). Näistä 58 pelistä katsotaan, mikä on ollut yleisin mustan 4. siirto ja se on ollut Nf6.
