Pravila
================================

## Roboliga 2026 – gradbeno dovoljenje

## Zgodba

Pisalo se je leto 2026, začela se je gradnja kampusa Brdo, ki vključuje novo fakulteto za farmacijo in fakulteto za strojništvo. Gradbena dela so potekala lepo v miru brez problemov, ampak česar gradbeniki niso vedeli, je, da naravovarstveniki za kulisami pripravljajo svoj načrt.
Naravovarstveniki sklepajo, da je gradbeno dovoljenje za novi fakulteti neveljavno pridobljeno, zato so začeli načrtovati, kako ustaviti gradbenike. Po več dolgih sestankih in tednih planiranja so se končno strinjali. Končna ideja je, da bodo poskusili ustaviti promet do gradbišča tako, da posadijo drevesa na pot, po kateri vozijo material.
Zdaj, ko je načrt pripravljen, je naslednji korak pripraviti drevesa in določiti dan, na katerega bodo izvedli akcijo. Odločili so se, da bodo napadli 3. decembra 2026. Ali bo gradbenikom kljub temu uspelo dostaviti potreben material na gradbišče ali jih bodo naravovarstveniki uspešno ustavili? Vabljeni, da na ta dan pridete na FRI spremljat, kdo bo zmagal to tekmovanje.

## Opis izziva

Vsaka ekipa sestavi svojega avtonomnega robota, ki bo igral vlogo gradbenika/naravovarstvenika. Roboti tekmujejo na poligonu, ki predstavlja gradbišče. Razpršeno po gradbišču se nahaja gradbeni material, in sicer opeka ter železo. Naravovarstvenik ima svoja drevesa (smreka ter japonska češnja) ob začetku v svoji bazi.

Naenkrat tekmujeta dva avtonomna robota. Gradbenik poskuša gradbeni material pripeljati v svojo bazo, medtem ko naravovarstvenik poskuša posaditi drevesa, da mu blokira pot.

Robota se po poligonu navigirata s pomočjo podatkov, ki jih preko brezžičnega omrežja pridobita s strežnika. Slednji budno spremlja dogajanje na poligonu s pomočjo kamere, nameščene nad njim.

## Potrebna znanja in veščine

Ekipe potrebujejo osnovno znanje programiranja in veselje do sestavljanja lego kock. Zelo pomemben je občutek za delo v skupini in zagnanost za reševanje novih izzivov.

Tekmovalci izdelajo program, ki se izvaja na robotu Lego Mindstorms EV3. Izbirajo lahko med množico programskih jezikov, med katerimi je najbolj priljubljen Python. Program mora poskrbeti za naslednje naloge:

1. Vzpostaviti mora brezžično (Wi-Fi) povezavo s strežnikom, ki bo robota oskrboval s podatki o dogajanju na poligonu.
2. Robot mora avtonomno voziti po poligonu, na podlagi podatkov, ki jih bo prejemal s strežnika. Tekmovalci bodo imeli na razpolago [primer programske kode](https://github.com/RoboLiga/ev3-nabiralec) v jeziku Python.

## Časovnica

| **Kdaj?** | **Kaj?** |
| --- | --- |
| 20. 10. 2024 | konec zbiranja prijav |
| 25. 10. 2024, 14:30 v R2.38 | prvo srečanje s prijavljenimi ekipami (predstavitev izziva, razdelitev kompletov) |
| XX. 11. 2024, 16:30 | uvodna delavnica (testni poligon) |
| XX. 11. 2024, 11:00 | 1. uradni trening (testni poligon) |
| XX. 11. 2024, 11:00 | 2. uradni trening (testni poligon) |
| 5. 12. 2024, 10:00 | zaključno tekmovanje (avla FRI) |

## Sestavni deli izziva

### Poligon

Poligon je ravno območje, po katerem se lahko gibljejo roboti – čistilci. Sestavljen je iz penastih plošč, ki jih obdaja ograja, znotraj poligona pa je na eni strani baza gradbenika (rdeča) ter baza naravovarstvenika (zelena).

Velikost: 2 m x 3,5 m 
Obdaja ga ograja iz pleksi stekla – ograja ni trdna in ni namenjena zaletavanju. 
Baze:
- postavljeni na nasprotnih straneh poligona,
- rdeče ter zelene barve,
- velikost vsakega koša: približno 1 m x 0,5 m,
- štirikotnik, ki definira koš za smeti, je določen v nastavitvah sledilnika.

### Gradbeni material

Na površini poligona se nahajajo kosi gradbenega materiala, ki so predstavljeni s plastičnimi kvadri:

- velikost (D x Š x V): 10 cm x 10 cm x 8 cm,
- na vrhu je značka za kamero,
- strežnik vsakemu kosu materiala določi naključno identifikacijsko številko (id),
- ko se ustvari nova tekma (Create a new game) in
- ko se tekma prične (Start the game).

### Drevesa

Na površini poligona se nahajajo tudi drevesa, ki so predstavljena s plastičnimi kvadri:
- velikost (D x Š x V): 10 cm x 10 cm x 8 cm,
- na vrhu je značka za kamero,
- strežnik vsakemu drevesu določi naključno identifikacijsko številko (id),
- ko se ustvari nova tekma (Create a new game) in
- ko se tekma prične (Start the game).

![Poligon-plaža](https://github.com/OnlyHans/roboliga-meta/blob/master/poligon.png)

### Robot

Robota sestavite iz kock Lego, ki so prisotne v kompletu, in napišete program, ki se bo izvajal na njem. Pri oblikovanju morate biti iznajdljivi, da konstrukcijo robota čim bolj prilagodite izzivu. Ob tem morate upoštevati naslednje omejitve:

- Robot je lahko izdelan iz kompletov Lego Mindstorms EV3, druge različice niso dovoljene.
- Izdelan robot lahko vsebuje eno programirljivo kocko, največ tri motorje in največ štiri tipala. Dovoljene vrste tipal so: barvno/svetlobno, ultrazvočno, žiroskop in tipalo za dotik.
- Največja dovoljena velikost gum je 56 mm x 26 mm.
- Robot lahko na začetku tekme meri največ 50 cm x 50 cm x 50 cm.
- Robot mora imeti na vrhu prostor za namestitev značke, ki bo vidna kameri.
- Programirate lahko v poljubnem programskem jeziku. Organizatorji nudimo [podporo za Python](https://github.com/RoboLiga/ev3-nabiralec).

Med tekmo lahko robota prime samo sodnik. 
Hkrati bosta v eni tekmi tekmovala dva robota. 
Na začetku tekme bodo sodniki postavili robota tako, da bo njegov skrajni sprednji del poravnan s tistim robom njegove baze, ki gleda proti sredini poligona. Robot bo tako v celoti v svoji bazi. 
V času tekme je robotu dovoljena povezava izključno na strežnik, ki nudi podatke o tekmi, in ne na druge naprave. 
Program na robotu lahko zaženete preko tipk na kocki ali oddaljeno preko SSH.

## Tekma

Tekma je dvoboj med dvema robotoma. Njun cilj je v omejenem času zbrati čim več točk. Gradbenik pridobiva točke s tem, da pripelje gradbeni material do svoje baze, medtem ko naravovarstvenik dobiva točke s tem, da sadi drevesa. Če gradbenik zapelje čez polje z drevesom, se mu odbijajo točke. 
Trajanje tekme: do 3 minute

Točkovanje:
- Vsaka opeka v košu gradbenika pomeni +2 točki za ekipo gradbenika.
- Vsako igro je eden izmed kosov gradbenega materiala železo, ki prinese +4 točke za ekipo gradbenika.
- Vsaka posajena smreka prinese eno točko za ekipo naravovarstvenika.
- Vsako igro je eno izmed dreves japonska češnja, ki prinese dve točki za ekipo naravovarstvenika.
- Če gradbenik zapelje čez smreko, se mu odšteje ena točka, če pa zapelje čez japonsko češnjo, pa 2 točki.
- Da je drevo posajeno, štejemo, ko je na določenem polju vsaj 10 sekund in je središče značke znotraj polja. Drevesa ne moremo posaditi znotraj baze gradbenika/naravovarstvenika.
- Da je gradbenik zapeljal čez drevo, štejemo takrat, ko je središče značke znotraj polja.
- Da je gradbeni material prispel v bazo, upoštevamo takrat, ko je središče značke znotraj baze. Nato se material odstrani iz poligona.
- V primeru, da sledilnik ne prepozna značke, o točkovanju odloča sodnik (primeri: gradbeni material je prevrnjen in njegova oznaka ni več vidna, značka materiala je prekrita z drugim objektom).

Protokol tekme:
- Priprava na tekmo: tekmovalni ekipi sta povabljeni, da postavita svojega robota na začetni položaj. Robota morata biti prižgana in povezana na strežnik.
- Začetek tekme: strežnik oznani začetek tekme z zastavico v podatkih o tekmi.
- Konec tekme: strežnik oznani konec tekme z zastavico v podatkih o tekmi. Možni načini konca tekme:
  - pretek časa,
  - obema robotoma zmanjka energije,
  - diskvalifikacija obeh robotov,
  - po presoji sodnika.

Če se robot začne premikati pred začetkom tekme, se tekma razveljavi in se vrnemo v pripravo na tekmo. Če robot to stori dvakrat v sklopu iste tekme, je diskvalificiran in tekma se ponovi samo za preostalega robota. 
Predvidoma bo tekmovanje sestavljeno iz dveh delov. V prvem bodo ekipe razdeljene v skupine, dvoboji pa bodo potekali po načelu vsak z vsakim. Najvišje uvrščene ekipe glede na število točk se potem pomerijo še v izločilnih bojih. Začetni tekmovalni pari izločilnih bojev se določijo glede na izkupiček točk skupinskega dela.

## Sodnik

- Sodnik ima absolutno diskrecijsko pravico.
- Sodnik lahko prekine tekmo, če presodi, da se stanje točk ne bo spremenilo (npr. oba robota obtičita, se sploh ne odzivata, tekmovalci vdrejo na poligon ipd.).

## Testni poligon

Za lažje priprave na tekmovanje smo pripravili testni poligon. Nahaja se na Fakulteti za računalništvo in informatiko v 2. nadstropju. Prostor ima oznako R2.38 in je v bližini Laboratorija za adaptivne sisteme in paralelno procesiranje (R2.41), kjer smo organizatorji Robo lige FRI. Za boljšo orientacijo si oglejte [načrt prostorov](https://github.com/RoboLiga/roboliga-meta/raw/master/Na%C4%8Drt_FRI_2nadstropje.pdf).

V prostor s poligonom lahko pridete le s posebnim elektronskim ključem. Ključ prevzamete pri vratarju in ga po končanem delu tja tudi vrnete. Vrata odklenete tako, da elektronski ključ približate črni ploščici na levi strani vrat. Ko so vrata odklenjena, zasveti zelena lučka. V sobi je postavljen poligon iz penastih plošč, na stropu je širokokotna spletna kamera.

**Pravila obnašanja**
- Prepovedano je stopiti na penasto ploščo, saj se takoj umaže in deformira.
- V prostoru skrbite za red in čistočo.
- Ko zapuščate prostor, ugasnite vse luči in zaprite okna.
- Zaklepajte vrata za seboj. To storite tako, da elektronski ključ približate črni ploščici na levi strani vrat; zasveti oranžna lučka.
- V primeru težav se obrnite na organizatorje.

--------------------------
> Organizatorji si pridržujemo pravico do spremembe in dopolnitve nalog ter tekmovalnih pravil.