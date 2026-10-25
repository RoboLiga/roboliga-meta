# BrickLink Studio 2 – kocka z ArUco oznako in paleta Robo liga

V tej mapi so datoteke za [BrickLink Studio 2](https://www.bricklink.com/v3/studio/download.page), s katerimi lahko robota za Robo ligo FRI 2026 sestavite in preizkusite virtualno:

| Datoteka | Opis |
| --- | --- |
| `parts/ArucoTag.dat` | Model kocke z ArUco oznako (dodatni del, `aruco_tag_part`) |
| `connectivity/ArucoTag.conn` | Priključne točke dela (kako se pripne na ostale kocke) |
| `collider/ArucoTag.col` | Kolizijski model dela |
| `Palette_RoboLiga.xml` | Paleta s kockami, ki so na voljo za gradnjo robota |

> **Pomembno:** najprej namestite dodatni del (custom part), šele nato uvozite paleto. Paleta vsebuje del `aruco_tag_part`; če ta ob uvozu še ni nameščen, ga Studio ne prepozna in ga v paleti ne bo.

## 1. Namestitev dodatnega dela (ArUco oznaka)

1. Zaprite BrickLink Studio, če je odprt.
2. Odprite mapo za dodatne dele (`CustomParts`):
   - **Windows:** `%LOCALAPPDATA%\Stud.io\CustomParts`
     (pot vpišite v naslovno vrstico Raziskovalca, npr. `C:\Users\<uporabnik>\AppData\Local\Stud.io\CustomParts`)
   - **macOS:** `~/Library/Application Support/Stud.io/CustomParts`

   Če mapa `CustomParts` ali katera od spodnjih podmap ne obstaja, jo ustvarite.
3. Datoteke iz te mape skopirajte v istoimenske podmape:

   | Iz te mape | V mapo |
   | --- | --- |
   | `parts/ArucoTag.dat` | `CustomParts/parts/` |
   | `connectivity/ArucoTag.conn` | `CustomParts/connectivity/` |
   | `collider/ArucoTag.col` | `CustomParts/collider/` |

4. Zaženite BrickLink Studio.
5. Preverite namestitev: v paleti izberite **Custom Parts** (ali v iskalno polje vpišite `ArUco`). Del **ArUco Tag** se mora prikazati.

## 2. Uvoz palete Robo liga

1. V Studiu odprite ploščo **Palette** (levo).
2. Kliknite spustni seznam za izbiro palete in izberite **Config...**.
3. Spodaj kliknite **Choose a way to add new palette...**.
4. V seznamu izberite **Import a wanted list xml w/ quantity**.
5. Izberite datoteko `Palette_RoboLiga.xml` iz te mape.
6. Paleta se prikaže v seznamu palet; izberite jo in med kockami preverite, ali je prisotna tudi kocka z ArUco oznako.

## Odpravljanje težav

- **ArUco oznake ni v paleti:** paleta je bila najverjetneje uvožena, preden je bil del nameščen. Preverite korak 1, ponovno zaženite Studio, izbrišite paleto in jo uvozite znova.
- **Del se prikaže, a se ne pripne na druge kocke:** datoteka `ArucoTag.conn` ni v mapi `CustomParts/connectivity/`.
- **Del se prikaže brez slike oznake:** preverite, da je bila datoteka `ArucoTag.dat` skopirana v celoti (oznaka je vgrajena v datoteko kot tekstura).
