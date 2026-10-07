## Roboliga 2026 – Gradbišče
================================

## Zgodba

Pisalo se je leto 2026. Začela se je gradnja kampusa Brdo, ki vključuje novo Fakulteto za farmacijo in Fakulteto za strojništvo. Gradbena dela so potekala mirno in brez težav, česar pa gradbeniki niso vedeli, je bilo, da naravovarstveniki za kulisami pripravljajo svoj načrt.
Naravovarstvenike je izredno zbodlo, koliko travnatih površin se uniči za »betonski gozd«, zato so začeli načrtovati, kako bi ustavili gradbenike. Po številnih dolgih sestankih in tednih načrtovanja je prišlo do prelomnice. Vohun, ki so ga poslali med gradbenike, je poročal, da gradbeniki razvijajo avtonomne robote, ki bodo dostavljali gradbeni material na gradbišče.
Naravovarstveniki so se takoj lotili načrtovanja lastnih robotov. Kako jih ustaviti, je bilo očitno: njihovi roboti bodo na pot, po kateri vozijo roboti gradbenikov, posadili drevesa in jih tako dokončno ustavili.
Za napad so izbrali 3. december 2026. Bo gradbenikom kljub temu uspelo dostaviti potrebni material na gradbišče ali jih bodo naravovarstveniki ustavili? Vabljeni, da ta dan pridete na FRI in si ogledate, kdo bo zmagal.

## Opis izziva

Vsaka ekipa sestavi svojega avtonomnega robota, ki bo igral vlogo gradbenika ali naravovarstvenika. Roboti tekmujejo na poligonu, ki predstavlja gradbišče. Po gradbišču je razpršen gradbeni material, in sicer opeke in železo. Naenkrat tekmujeta dva avtonomna robota gradbenik in naravovarstvenik. Slednji ima na začetku tekme v svojem izhodišču drevesa. Na drugi strani poligona se nahaja gradbena baza, kamor poskuša Gradbenik pripeljati razpršeni gradbeni material, medtem ko naravovarstvenik po poligonu sadi drevesa, s katerimi mu zapira pot.

Robota se po poligonu orientirata na podlagi podatkov, ki jih prek brezžičnega omrežja prejemata s strežnika. Strežnik dogajanje na poligonu budno spremlja s kamero, nameščeno nad njim.

## Potrebna znanja in veščine

Ekipe potrebujejo osnovno znanje programiranja in veselje do sestavljanja kock Lego. Zelo pomemben je občutek za delo v skupini in zagnanost za reševanje novih izzivov.

Tekmovalci napišejo program, ki teče na robotu. Robota sami oblikujejo in sestavijo iz kompleta [Lego Mindstorms Education EV3 Core Set (45544)](https://assets.education.lego.com/v3/assets/blt293eea581807678a/bltd9e811d9ff83b385/5f8801d5887a311d8fa19812/45544_element_survey.pdf?locale=en-us). Na robotu je namesto Legovega operacijskega sistema naložen operacijski sistem [ev3dev](https://www.ev3dev.org/). Tekmovalci lahko izbirajo med številnimi programskimi jeziki, najbolj priljubljen med njimi je Python.

## Časovnica

| **Kdaj?** | **Kaj?** |
| --- | --- |
| 20. 10. 2026 | konec zbiranja prijav |
| 25. 10. 2026, 14:30 v R2.38 | prvo srečanje s prijavljenimi ekipami (predstavitev izziva, razdelitev kompletov) |
| XX. 11. 2026, 16:30 | uvodna delavnica (testni poligon) |
| XX. 11. 2026, 11:00 | 1. uradni trening (testni poligon) |
| XX. 11. 2026, 11:00 | 2. uradni trening (testni poligon) |
| 5. 12. 2026, 10:00 | zaključno tekmovanje (avla FRI) |

## Sestavni deli izziva

### Poligon

Poligon je ravna površina, po kateri se gibljejo roboti -- gradbeniki in naravovarstveniki. Sestavljen je iz penastih plošč in obdan z ograjo. Na nasprotnih straneh poligona sta bazi gradbenika (rdeča) in naravovarstvenika (zelena). Poligon je razdeljen na polja (posamezne penaste plošče, velikosti približno 0,5 m x 0,5 m).

Velikost: 2 m x 3,5 m 
Obdaja ga ograja iz pleksi stekla – ograja ni trdna in ni namenjena zaletavanju. 
Bazi:
- postavljeni na nasprotnih straneh poligona,
- rdeče in zelene barve,
- velikost izhodišč: približno 1 m x 0,5 m,

### Gradbeni material

Na poligonu so kosi gradbenega materiala, ki jih predstavljajo plastični kvadri:

- velikost (D x Š x V): 10 cm x 10 cm x 8 cm,
- na vrhu je značka za kamero,
- strežnik vsakemu kosu materiala določi naključno identifikacijsko številko (id),
- ko se ustvari nova tekma (Create a new game) in
- ko se tekma prične (Start the game).

### Drevesa

Na poligonu so tudi drevesa, ki jih prav tako predstavljajo plastični kvadri:
- velikost (D x Š x V): 10 cm x 10 cm x 8 cm,
- na vrhu je značka za kamero,
- strežnik vsakemu drevesu določi naključno identifikacijsko številko (id),
- ko se ustvari nova tekma (Create a new game) in
- ko se tekma prične (Start the game).

![Poligon-gradbišče](https://github.com/RoboLiga/roboliga-meta/blob/dev/26/poligon.png)

### Robot

Robot sme biti sestavljen samo iz kock enega kompleta [Lego Mindstorms Education EV3 Core Set (45544)](https://assets.education.lego.com/v3/assets/blt293eea581807678a/bltd9e811d9ff83b385/5f8801d5887a311d8fa19812/45544_element_survey.pdf?locale=en-us), ki si ga tekmovalci po prijavi izposodijo. Komplet in robota lahko vzamejo domov.

Za oblikovanje svetujemo uporabo programa, kot je [BrickLink Studio](https://www.bricklink.com/v3/studio/main.page), ki ga priporoča tudi Lego.

Pri oblikovanju bodite iznajdljivi in konstrukcijo robota čim bolje prilagodite izzivu. Upoštevati morate naslednji omejitvi:
- Robot sme na začetku tekme meriti največ 50 cm × 50 cm × 50 cm.
- Robot mora imeti na vrhu prostor za namestitev značke, ki bo vidna kameri.

#### Pravila za robote
- Med tekmo sme robota prijeti samo sodnik.
- V eni tekmi hkrati tekmujeta dva robota.
- Med tekmo se sme robot povezati izključno s strežnikom, ki posreduje podatke o tekmi.

### Program
Program je lahko napisan v [podprtih jezikih](https://www.ev3dev.org/docs/programming-languages/), **vendar** organizatorji podpiramo samo Python.

Organizatorji vzdržujemo [predlogo za Python](https://github.com/RoboLiga/ev3-nabiralec), ki vsebuje program za povezovanje s strežnikom in pobiranje kock.

Če uporabljate drug programski jezik, za povezavo s strežnikom in branje prejetih podatkov potrebujete odjemalca HTTP.

#### Pravila za program

- Tekmovalci med tekmovanjem ne smejo posegati v delovanje programa; robot mora delovati samostojno.
- Če se program sesuje, ga do naslednjega kroga ni dovoljeno ponovno zagnati. Program je dovoljeno ustaviti.
- Program lahko med tekmovanjem zaženete s tipkami na kocki ali na daljavo prek SSH.

## Tekma
**Trajanje tekme: največ 3 minute**

Tekma je dvoboj med dvema robotoma. Njun cilj je v omejenem času zbrati čim več točk. Gradbenik dobi točke, ko pripelje gradbeni material v svojo bazo, naravovarstvenik pa, ko posadi drevo. Če gradbenik zapelje čez polje z drevesom, izgubi točke.

Točkovanje:
- Vsaka opeka v bazi gradbenika prinese ekipi gradbenika 2 točki.
- V vsaki igri je en kos gradbenega materiala železo, ki gradbeniku prinese 4 točke.
- Vsaka posajena smreka prinese naravovarstveniku 1 točko.
- Eno izmed dreves je japonska češnja, ki ekipi naravovarstvenika prinese 2 točki.
- Če gradbenik zapelje čez smreko, se mu odšteje 1 točka, če zapelje čez japonsko češnjo, pa 2 točki.
- Drevo velja za posajeno, ko je vsaj 5 sekund na istem polju in je središče njegove značke znotraj polja. Drevesa ni mogoče posaditi v bazi gradbenika ali naravovarstvenika.
- Že posajeno drevo se lahko presadi na drugo polje, vendar presajanje ne prinese dodatnih točk naravovarstveniku.
- Šteje se, da je gradbenik zapeljal čez drevo, ko je središče njegove značke znotraj polja z drevesom.
- Gradbeni material velja za dostavljen v bazo, ko je središče njegove značke znotraj baze. Točke se prištejejo takoj in ostanejo, tudi če je material pozneje izrinjen iz baze. Ponovno dostavljen material ne prinese dodatnih točk.
- Če sledilnik značke ne prepozna, o točkah odloči sodnik (npr. če se gradbeni material prevrne in njegova značka ni več vidna ali če značko materiala prekrije drug predmet).

Protokol tekme:
- Znotraj tekme se izvedeta dva teka: najprej ena ekipa prevzame vlogo gradbenika, druga pa naravovarstvenika, nato se vlogi ekip zamenjata.
- Priprava na tekmo: tekmovalni ekipi postavita svoja robota na začetna položaja. Robota morata biti prižgana in povezana s strežnikom.
- Začetek tekme: strežnik začetek tekme sporoči z zastavico v podatkih o tekmi.
- Konec tekme: strežnik konec tekme sporoči z zastavico v podatkih o tekmi. Tekma se lahko konča:
  - ko poteče čas,
  - z diskvalifikacijo obeh robotov,
  - po presoji sodnika.

Če se robot začne premikati pred začetkom tekme, se začetek razveljavi in tekma se vrne v fazo priprave. Če robot to stori dvakrat v isti tekmi, je diskvalificiran, tekma pa se ponovi samo s preostalim robotom.
Tekmovanje bo predvidoma potekalo v dveh delih. V skupinskem delu bodo ekipe razdeljene v skupine, v katerih se bo pomerila vsaka z vsako. Ekipe z največ točkami se nato pomerijo še v izločilnih dvobojih. Pari za prvi krog izločilnih dvobojev se določijo glede na izkupiček točk iz skupinskega dela.

## Sodnik

- Sodnik ima popolno diskrecijsko pravico.
- Sodnik lahko tekmo prekine, če presodi, da se stanje točk ne bo več spremenilo (npr. če oba robota obtičita ali se ne odzivata, če tekmovalci posežejo na poligon ipd.).

## Testni poligon

Za lažjo pripravo na tekmovanje smo postavili testni poligon. Je v 2. nadstropju Fakultete za računalništvo in informatiko, v prostoru R2.38, v bližini Laboratorija za adaptivne sisteme in paralelno procesiranje (R2.41), kjer delujemo organizatorji Robolige FRI. Za lažjo orientacijo si oglejte [načrt prostorov](https://github.com/RoboLiga/roboliga-meta/raw/master/Na%C4%8Drt_FRI_2nadstropje.pdf).

V prostor s poligonom lahko vstopite le s posebnim elektronskim ključem. Ključ prevzamete pri vratarju in mu ga po koncu dela tudi vrnete. Vrata odklenete tako, da elektronski ključ približate črni ploščici na levi strani vrat. Ko so vrata odklenjena, zasveti zelena lučka. V sobi je postavljen poligon iz penastih plošč, na stropu pa je nameščena širokokotna spletna kamera.

**Pravila obnašanja**
- Na penaste plošče je prepovedano stopati, saj se hitro umažejo in deformirajo.
- Skrbite za red in čistočo v prostoru.
- Ko zapuščate prostor, ugasnite vse luči in zaprite okna.
- Za seboj zaklenite vrata: elektronski ključ približajte črni ploščici na levi strani vrat, da zasveti oranžna lučka.
- Če naletite na težave, se obrnite na organizatorje.

--------------------------
> Organizatorji si pridržujemo pravico do spremembe in dopolnitve nalog ter tekmovalnih pravil.
