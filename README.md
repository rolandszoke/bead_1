# bead_1
##Követelményanalízis

- legalább két modellt, egy-sok kapcsolatban
- legalább 1 űrlapot
- legalább 1 listázó oldalt
- legyen lehetőség új felvételére
- legyen lehetőség meglévő szerkesztésére
- legyen lehetőség meglévő törlésére
- legyenek benne csak hitelesítés után elérhető funkciók
- perzisztálás fájlba történjen
- közzététel Herokun

###Családi TODO
####Funkcionális
+ Családtagként szeretnék kitűzni egy feladatot a család valamely vagy bármely tagjának. --> Hozzáadás
+ Családtagként szeretnénk visszajelzést kapni, hogy a kitűzött feladat milyen stádtuszban van. --> Listázása
+ Családtagként szeretnénk egy feladat státuszát megváltoztatni.
+ Bejelentkezés után használhatják a funkciókat.
+ főoldalon az alkalmazás ismertetése, használatához szükséges feltételek jelennek meg.
####Nem funkcionális
+ Felhasználóbarát, ergonomikus elrendezés és kinézet.
+ Gyors működés.
+ Biztonságos működés: jelszavak tárolása, funkciókhoz való hozzáférés.

##Tervezés
###Oldaltérkép:
Publikus:

- Főoldal
- Login
- Regisztráció

Családtag

- Főoldal
- Login/Logout
- TODO lista
    + TODO megtekintése
    + TODO szerkesztése
    + TODO Törlése
- Hozzáadás
    + új TODO 

###Végpontok
  + GET /: főoldal
  + GET /help: leírás a használatról
  + GET /login/login: bejelentkező oldal
  + POST /login/login: bejelentkezési adatok felküldése
  + GET /login/signup: regisztrációs oldal
  + POST /login/signup: regisztrációs adatok felküldése
  + GET /list: todo lista
  + GET /add: új tod felvitele
  + POST /add: új todo felvitele, adatok küldése
  + GET /delete/:id todo törlése
  + GET /ready/:id todo módosítása
  + GET /inform/:id todo részletezése

###Drótváz
  
  ![Drótváz](docs/images/1.png)
  
###Adatmodell

![Adatmodell](docs/images/2.png)

##Implementáció

###Fejlesztői környezet: 
Cloud9

###Mappa szerkezet:
+ models    ---felhasználó és feladat Waterline Collection
    - todo.js
    - user.js
+ node_modules  --- node package
    - ....
+ test  ---teszt fájl
    - create.test.js
+ views ---nézetek
    - login
        * index.hbs
        * signup.hbs
    - partials
        * menu.hbs
        * messages.hbs
    - add.hbs
    - info.hbs
    - layout.hbs
    - list.hbs
    - todo.hbs
+ index.js
+ package.json
+ router.js


##Felhasználó dokumentáció

Futtatáshoz ajánlott konfiguráció: Bármely naprakész böngésző felület
A program használatához szükséges regisztrálni.
Minden egyéb instrukciót megtalál az adott felületen.
