- [Leírás](https://github.com/laszlokelemen/alkfejl-bead#leírás)
- [Követelmények](https://github.com/laszlokelemen/alkfejl-bead#követelmények)
- [Szakterületi fogalomjegyzék](https://github.com/laszlokelemen/alkfejl-bead#fogalomjegyzék)
- [Szerepkörök](https://github.com/laszlokelemen/alkfejl-bead#szerepkörök)
- [Használati eset diagram](https://github.com/laszlokelemen/alkfejl-bead#használati eset diagram)
- [Folyamatok](https://github.com/laszlokelemen/alkfejl-bead#folyamatok)
- [Oldaltérkép](https://github.com/laszlokelemen/alkfejl-bead#oldaltérkép)
- [Végpontok](https://github.com/laszlokelemen/alkfejl-bead#végpontok)
- [Oldalvázlat](https://github.com/laszlokelemen/alkfejl-bead#oldalvázlat)
- [Adatbázis modell](https://github.com/laszlokelemen/alkfejl-bead#modell)





##Leírás
Egy tárgyfelvétel nyilvántartó programot készítek, ahol meglehet fel lehet venni,nézni az 
aktuális tárgyainkat, illetve profilunkat.

##Követelmények
Funkcionális elvárások

    Felhasználóként szeretnék tudni bejelentkezni az oldalra.
    Felhasználóként szeretnék tudni bejelentkezni az adott félévre.
    Felhasználóként szeretnék felvenni egy kuruzst.
    Felhasználóként szeretnék megtekinteni a kurzus típusokat, egy adot kurzuson belül.
    Felhasználóként szeretnék kurzust keresni.
    Felhasználóként szeretnék megtekinteni, szerkeszteni törölni a saját profilomat.
    Felhasználóként szeretnék megtekinteni, szerkeszteni, törölni a saját tárgyaimat.
    
    Vendégként szeretnék tudni beregisztrálni az oldalra. 
    Vendégként szeretnék kurzusokat megtekinteni.

Nem funkcionális követelmények

    Felhasználóbarát, ergonomikus elrendezés és kinézet.
    Gyors működés.
    Funkciókhoz való hozzáférés.
    Biztonságos működés: jelszavak tárolása, funkciókhoz való hozzáférés.


##Fogalomjegyzék
Szakteröketi fogalomjegyzék

    Kurzus:Az a keret, amelyben a hallgatók meghatározott rend (előadás, gyakorlat, házi feladat, stb.) szerint                   gyarapítják tudásukat, és arról számot is adnak.

##Szerepkörök
Szerepkörök

    Vendég:a tárgyfelvételhez szükséges regisztrálást végezheti, valamint megtekintenheti a kurzusok listáját.
    Felhasználó:a vendég szerepkörén túl saját profilja és kurzusai kezelésére képes. 
##Használati eset diagram
![Használati eset](https://github.com/laszlokelemen/alkfejl-bead/blob/master/usecase.png)

##Folyamatok
Felhasználó:


 * bejelentkezés:![bejelentkezésfoly](https://github.com/laszlokelemen/alkfejl-bead/blob/master/bejelentkezés.png)
 * új kurzus felvétel:![kurzusfoly](https://github.com/laszlokelemen/alkfejl-bead/blob/master/kurzusfelvesz.png)
 
Vendég:
 
  * regisztrálás:![regisztrálás](https://github.com/laszlokelemen/alkfejl-bead/blob/master/vendeg.png)
  * kurzusok megtekintése:![kurzusok](https://github.com/laszlokelemen/alkfejl-bead/blob/master/kurzuskeres.png)

##Oldaltérkép
Oldaltérkép: 

    Publikus:    -Főoldal
                 -Belépés
                 -Regisztrálás
                 -Kurzusok keresés
                    +kurzus megtekintése
    Felhasználó:-Kilépés
                -Profiladatok
                    +Profiladatok szerkesztése
                 -Bejelentkezés a félévre
                 -Felvett kurzusok megtekintése
                 -Kurzusok megtekintése
                    +kurzus felvétele
                    +felvett kurzus módosítása
                 -Hibalista
                    +hibák jelzése
                 
                

##Végpontok
Végpontok:

    -GET  /:főoldal
    -GET  /search : kurzusok keresés
    -GET  /login : bejelentkező oldal
    -POST /login :bejelentkező adatok felküldése
    -GET  /profile: profiladatok megtekintése
    -POST /profile/modify : profiladatok módosításának elküldése
    -GET  /courses: kurzusok listája
    -GET  /courses/id: kurzus megtekintése
    -GET  /courses/id/take : kurzus felvétele
    -POST /courses/id/take : kurzus felvétele/adatok küldése
    -GET  /mycourses : felvett kurzusok listája 
    -GET  /mycourses/id : felvett kurzus megtekintése
    -POST /mycourses/id/modify : felvett kurzus módosításának elküldése
    
##Oldalvázlat
Oldalvázlat:
![bejelentkezésfoly](https://github.com/laszlokelemen/alkfejl-bead/blob/master/miniNeptun.jpg)
![bejelentkezésfoly](https://github.com/laszlokelemen/alkfejl-bead/blob/master/miniNeptunlogedin.jpg)

##modell
Adatbázis modell:
![bejelentkezésfoly](https://github.com/laszlokelemen/alkfejl-bead/blob/master/datamodel.png)
    
