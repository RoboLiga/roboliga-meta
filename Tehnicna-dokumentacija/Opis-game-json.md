Opis Game JSON datoteke
=====================

V tem dokumentu so opisani objekti v datoteki JSON, ki opisuje trenutno stanje igre. Primer celotne datoteke je v `game.json`. Vrednosti posameznih atributov so zgolj informativne narave.

Igra
----
```
{
  "timeLeft": 100.0,
  "gameOn": true,
  "team1": <Ekipa>,
  "team2": <Ekipa>,
  "field": <Igrišče>,
  "apples": [ <Jabolko>, ... ],
  "robots": [ <Robot>, ...]
}
```

Igra je glavni objekt v datoteki JSON. Vsebuje preostali čas tekme `timeLeft` v sekundah, zastavico, ki opisuje ali je tekma v teku, `gameOn`, opisa ekip `team1` in `team2`, opis igrišča `field`, seznam jabolk na igrišču `apples` in seznam robotov na igrišču `robots`.

Ekipa
-----
```
{
  "id": 13,
  "name": "Ekipa-da-te-skipa",
  "score": 2
}
```

Ekipa je objekt sestavljen iz identifikatorja ArUco značke njenega robota `id`, imena ekipe `name` in trenutnega števila točk ekipe `score`.

Igrišče
-------------
```
{
  "topLeft": [0, 2055],
  "topRight": [3555, 2055],
  "bottomLeft": [0, 0],
  "bottomRight": [3555, 0],
  "baskets": {
    "team1": <Košara>, 
    "team2": <Košara>
  }
}
```

Igrišče je objekt sestavljen iz koordinat vogalov (v milimetrih): `topLeft`, `topRight`, `bottomLeft` in `bottomRight`, ter objekta `baskets`, ki vsebuje opisa košar obeh ekip `team1` in `team2`. Preko koordinat vogalov je določeno izhodišče koordinatnega sistema ter orientacija igrišča v njem.

Košara
------
```
{
  "topLeft": [0, 1520],
  "topRight": [510, 1520],
  "bottomLeft": [0, 530],
  "bottomRight": [510, 530]
}
```

Košara je objekt, ki vsebuje štiri točke, ki predstavljajo koordinate njenih vogalov (v milimetrih).

Robot
-----
```
{
  "id": 13,
  "position": [150, 80],
  "direction": 10
}
```

Robot je objekt sestavljen iz identifikatorja ArUco `id`, pozicije na igralnem polju `position` (v milimetrih) in azimutne orientacije `direction` (v stopinjah) na območju [-180, 180].

Jabolko
-------
```
{
  "id": 40,
  "type": "appleGood",
  "position": [1000, 500]
  "direction": 10
}
```

Jabolko je objekt sestavljen iz identifikatorja ArUco `id`, opisa tipa `type`, ki je lahko `appleGood` za zdravo jabolko in `appleBad` za gnilo, in pozicije na igralnem polju `position` (v milimetrih) ter azimutne orientacije `direction` (v stopinjah) na območju [-180, 180].
