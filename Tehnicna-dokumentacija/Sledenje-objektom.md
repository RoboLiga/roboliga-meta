Uporaba programa za sledenje
================================

## Nastavitve
Delovanje sledilnika objektov nastavljate z urejanjem konfiguracijskih datotek, ki se nahajajo v mapi ``Tracker``.
* Nastavitev tekme urejate preko datoteke ``gameData.json``:
  * V polju ``teams`` se nahajajo imena vseh sodelujočih ekip in pripadajoči identifikatorji ArUco.
  * V polju ``currentGameTeams`` se nahajata identifikatorja ArUco dveh ekip, ki bosta tekmovali v naslednji tekmi.
  * S poljem ``gameTime`` lahko nastavimo trajanje tekme v sekundah.
  * Polje ``goodApple`` določa število točk, ki jih prinese ekipi pobrano zdravo jabolko.
  * Polje ``badApple`` določa število točk, ki jih prinese ekipi pobrano gnilo jabolko.
```json
{
    "teams": {
        "-1": "",
         "0": "Super Glavce",
         "5": "GAYA",
        "12": "Distopija",
        "18": "Noteblock gang",
        "19": "Hugs for Bugs",
        "25": "KROBOD",
        "32": "BetterBot",
        "33": "Bionic Farmers",
        "35": "TrijeMaliKlinci",
        "39": "Pršut in teran",
        "41": "Deep Thought",
        "44": "( ͡° ͜ʖ ͡°)"
		
    },
    "currentGameTeams": {
        "Team1": -1,
        "Team2": -1
    },
    "gameTime": 100,
    "goodApple": 1,
    "badApple": -2
}
```

* Nastavitve sledilnika urejate preko datoteke ``Resources.py``:  
  Večina nastavitev v tej datoteki je fiksna. Za uporabnike je smiselno le nastavljanje poti do datotek in video izvora.
  Te nastavitve se nahajajo v razredu ``ResFileNames``:
  * Spremenljivka ``gameDataFile`` vsebuje ime datoteke, kjer s nahajajo nastavitve tekme.
  * Spremenljivka ``gameLiveDataFileName`` vsebuje ime datoteke, kjer se shranjuje trenutno stanje na poligonu.
  * Spremenljivka ``gameLiveDataTempFileName`` vsebuje ime začasne datoteke, kjer se shranjuje trenutno stanje na poligonu.
  * Spremenljivka ``mapConfigFileName`` vsebuje ime datoteke, v kateri se hranijo meje poligona.
  * Spremenljivka ``videoSource`` vsebuje naslov kamere/posnetka, od kjer se bere video.
```python
class ResFileNames:
    """Stores file names for json data"""
    gameDataFileName = "gameData.json"
    gameLiveDataFileName = "../nginx/html/game.json"
    gameLiveDataTempFileName = "gameLiveTemp.json"
    mapConfigFileName = "mapConfig"
    #videoSource = "rtsp://193.2.72.149/axis-media/media.amp"
    videoSource="http://193.2.72.149/mjpg/video.mjpg"
```
  
Ob spremembi konfiguracijskih datotek je potrebno sledilnik objektov ponovno zagnati, da se spremembe uveljavijo.


## Zagon

Sledenje zaženete preko ukazne vrstice Anaconda. Prestavite se v mapo ``Tracker`` in zaženete ukaz ``Tracker.py``. 
Nato je potrebno zagnati še spletni strežnik, ki podatke servira robotom. Tega zaženete tako, da v mapi ``nginx`` poženete skripto ``server_start.bat``. Spletni strežnik lahko ugasnete z zagonom skripte ``server_stop.bat``.

## Uporabniški vmesnik sledilnika objektov

Sledilnik objektov nadzorujemo s pomočjo tipk. Na voljo so sledeči ukazi:
* ``l`` - Naloži nastavitve tekme in poligon iz datotek ``gameData.json`` in ``mapConfig`` v kolikor le-te obstajajo.
* ``e`` - Odpre vmesnik za risanje mej poligona. Ponovni pritisk ``e`` pobriše trenutno naloženi poligon in zapre vmesnik. Poligon rišemo s klikanjem na želene vogale poligona in košar, pri tem pazimo na pravilen vrstni red. Po tem, ko narišemo vseh 12 vogalov se poligon samodejno shrani v datoteko ``configMap``.
* ``s`` - Začne tekmo in odštevanje časa. Tekma se ne more začeti, če ni bila najprej naložena nastavitev tekme s pomočjo tipke ``l``. Tekmo lahko predčasno zaključimo, če ponovno pritisnemo ``s``.
* ``c`` - Vklopi možnost urejanja točk ekip, ki tekmujejo. Levi klik na košaro ekipe poveča število točk za ena, desni klik na košaro ekipe pa število točk zmanjša za ena. Urejanje izklopimo s ponovnim pritiskom na tipko ``c``.
* ``q`` - Zapre sledilnik objektov.

![image](https://github.com/RoboLiga/roboliga-meta/blob/master/Tehnicna-dokumentacija/Tracker.PNG)

## Komunikacija z robotom

Robot sprejema podatke o stanju na poligonu preko enostavnega spletnega strežnika, ki servira datoteko ``game.json``, ki jo neprestano osvežuje sledilnik objektov. Ta datoteka vsebuje opis poligona in objektov na njemu v formatu JSON. Opis datoteke se nahaja na [link](https://github.com/RoboLiga/roboliga-meta/blob/master/Tehnicna-dokumentacija/game.md).



