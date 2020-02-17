Opis Game JSON datoteke
=====================

V tem dokumentu so opisani objekti v datoteki JSON, ki opisuje trenutno stanje igre. Primer celotne datoteke je v `game.json`. Vrednosti posameznih atributov so zgolj informativne narave.

Igra
----
```
{
  "timeLeft": 100.0,
  "gameOn": true,
  "teams": [<Ekipa>, ...]
  "fields": [<Igrišče>, <Skladišča>, <Cone>]
  "objects": [<Panji>, <Roboti>]
}
```

Igra je glavni objekt v datoteki JSON. Vsebuje preostali čas tekme `timeLeft` v sekundah, zastavico, ki opisuje ali je tekma v teku, `gameOn`, opise ekip `teams`, opis igrišča `fields` ter seznam panjev in robotov na igrišču `objects`.

Ekipa
-----
```
"teamX": {
  "id": 13,
  "name": "Ekipa-da-te-skipa",
  "score": 2
}
```

Ekipa je objekt sestavljen iz identifikatorja ArUco značke njenega robota `id`, imena ekipe `name` in trenutnega števila točk ekipe `score`.

Igrišče
-------------
```
"field": {
      "bottomLeft": {
        "x": 514,
        "y": 342
      },
      "bottomRight": {
        "x": 4,
        "y": 343
      },
      "topLeft": {
        "x": 4,
        "y": 4
      },
      "topRight": {
        "x": 519,
        "y": 5
      }
    }
```

Igrišče je objekt sestavljen iz koordinat vogalov (v milimetrih): `topLeft`, `topRight`, `bottomLeft` in `bottomRight`. Preko koordinat vogalov je določeno izhodišče koordinatnega sistema ter orientacija igrišča v njem.

Skladišča
------
```
"baskets": {
      "team1": {
        "bottomLeft": {
          "x": 109,
          "y": 239
        },
        "bottomRight": {
          "x": 3,
          "y": 250
        },
        "topLeft": {
          "x": 4,
          "y": 104
        },
        "topRight": {
          "x": 113,
          "y": 105
        }
      },
      "team2": {
        "bottomLeft": {
          "x": 515,
          "y": 260
        },
        "bottomRight": {
          "x": 383,
          "y": 262
        },
        "topLeft": {
          "x": 383,
          "y": 108
        },
        "topRight": {
          "x": 517,
          "y": 99
        }
      }
    },
```
Skladišče je definirano za vsako ekipo in vsebuje štiri točke, ki predstavljajo koordinate njenih vogalov (v milimetrih).

Robot
-----
```
"robots": {
    "0": {
        "dir": -0.12435499454676144,
        "x": 767,
        "y": 623
    }
}
```

Robot je objekt sestavljen iz identifikatorja [ArUco](https://www.uco.es/investiga/grupos/ava/node/26) (zgornji primer za id=0), pozicije na igralnem polju `x` in `y` (v milimetrih) in azimutne orientacije `dir` (v stopinjah) na območju [-180, 180].

Panji
-------
```
"hives": {
      "24": {
        "dir": -1.4940244355251187,
        "type": "HIVE_DISEASED",
        "x": 895,
        "y": 658
      },
      "36": {
        "dir": 0.43240777557053783,
        "type": "HIVE_HEALTHY",
        "x": 918,
        "y": 600
      }
    }
```

Panj je objekt sestavljen iz identifikatorja ArUco, opisa tipa `type`, ki je lahko `HIVE_HEALTHY` za zdrav panj ali `HIVE_DISEASED` za panj z bolnimi čebelami, in pozicije na igralnem polju `x` in `y` (v milimetrih) ter azimutne orientacije `dir` (v stopinjah) na območju [-180, 180].
