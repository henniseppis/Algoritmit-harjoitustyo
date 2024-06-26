# Määrittelydokumentti 

#### Opinto-ohjelma:
- Tietojenkäsittelytieteen kandidaatti

#### Projektin ohjelmointikieli ja muiden kielien osaaminen
- Teen projektini Pythonilla
- Dokumentointi on suomeksi, mutta koodi englanniksi
- Pystyn vertaisarvioimaan tarvittaessa myös JavaScriptillä tehtyjä töitä, mieluiten python.

#### Projektin aihe

Päädyin aiheessani klassiseen ristinolla peliin. Mielenkiintoinen aihe, jossa pääsee haastaamaan itseään ja oppimaan uutta.

Ristinolla tulee olemaan 20x20 lauta. Algoritmina käytössä minimax aplha-beta karsinnalla. 

Tarkoituksena algoritmin avulla löytää viimeisimmän siirron perusteella, siihen tilanteeseen parhain siirto. Löytääksemme parhaimman siirron nopeiten, tutkitaan vain aikaisempien siirtojen lähialueet.

Voitto selvitetään tarkastelemalla vain viimeiseen siirtoon liittyviä ruutuja, viimesimmän siirron tehnyt julistetaan voittajaksi jos voiton ehdot täyttyvät.

Aikavaativuus on O(b^m), jossa b on mahdollisten siirtojen määrä ja m puun syvyys.

Ydin on saada algoritmi tuottamaan mahdollisimman nopeasti paras mahdollinen siirto, mitä silloisessa pelitilanteessa voidaan tehdä. 

#### Pelin kulku
- Peliä voi pelata komentoriviltä
- Käyttäjä pelaa tietokonetta vastaan. Toisella nappuloina ristit, toisella nollat.
- Nappuloita laitetaan laudalle vuorotellen, yksi kerrallaan
- Se kumpi saa ensiksi 5 omaa nappulaa peräkkäin pelilaudalle, voittaa. (Pysty, vaaka tai diagonaali)
- Pelissä tehdään siirtoja syöttämällä paikan koordinaatti johon oman nappulan haluaa (esim. B3, jolloin oma nappula laitetaan toisen rivin kolmannelle sarakkeelle)
- Teen (ehkä) niin, että käyttäjä on aina risti ja tietokone nolla. Toki saatan myös tehdä niin että käyttäjä voi valita kumpi haluaa olla.

#### Minimax-algoritmi alpha-beta-karsinnalla

Minimax on päätöspuualgoritmi, jota käytetään esimerkiksi pelien luonnissa Minimax-algoritmi pyrkii minimoimaan häviön joko itse voittamalla, tai tekemällä siiroon joka ei johda toisen pelaajan voittoon seuraavalla kierroksella. Algoritmi arvioi pelin tilaa ja seuraavaa siirtoa pelin edetessä verraten sitä edellisiin siirtoihin.  Alpha-beta-karsinta tuodaan rinnalle tehostamaan minmax-algoritmia, jotta saadaan luotua paras siirto mahdollisimman vähällä työllä. Alpha ja beta saavat kuvaavat parhainta ja huonointa arvoa. Puuta läpikäytäessä min saa arvoksi alphan ja max betan.

  
#### Lähteet
https://en.wikipedia.org/wiki/Minimax#Minimax_algorithm_with_alternate_moves
https://jyx.jyu.fi/bitstream/handle/123456789/58204/1/URN%3ANBN%3Afi%3Ajyu-201805292875.pdf
https://www.neverstopbuilding.com/blog/minimax
https://www.geeksforgeeks.org/finding-optimal-move-in-tic-tac-toe-using-minimax-algorithm-in-game-theory/
