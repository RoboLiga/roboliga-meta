Pravila
================================

## Opis izziva

Letošnji izziv postavlja robota pred izziv čiščenja plaže. Robot mora v omejenem času pravilno reciklirati čim več odpadkov, ki jih najde na plaži, ob tem pa paziti, da ne zagrabi školjk.

Vsaka ekipa sestavi svojega avtonomnega robota – čistilca. Roboti tekmujejo na poligonu, ki predstavlja slovensko plažo. Na plaži se nahajajo odpadki (plastika ali steklo) in školjke.

Naenkrat tekmujeta dva avtonomna robota, ki imata nalogo, da v svoja koša pravilno reciklirata plastiko ter steklo ob tem pazita, da ne zagrabita školjke. Robot ugotovi, ali je odpadek steklo ali plastika, šele ob podrobni analizi.

Kot vsakdo se tudi robot med delom utrudi, posledično se mora odpočiti na posebnih poljih, namenjenih počitku.

Robota navigirata po poligonu s pomočjo podatkov, ki jih preko brezžičnega omrežja pridobita s strežnika. Slednji budno spremlja dogajanje na poligonu s pomočjo kamere nameščene nad njim.

## Potrebna znanja in veščine

Ekipe potrebujejo osnovno znanje programiranja in veselje do sestavljanja lego kock. Zelo pomemben je občutek za delo v skupini in zagnanost za reševanje novih izzivov.

Tekmovalci izdelajo program, ki se izvaja na robotu Lego Mindstorms EV3. Izbirajo lahko med množico programskih jezikov, med katerimi je najbolj priljubljen Python. Program mora poskrbeti za naslednje naloge:

1. Vzpostaviti mora Brezžično (Wi-Fi) povezavo z strežnikom, ki bo robota oskrboval s podatki o dogajanju na poligonu.
2. Robot mora avtonomno voziti po poligonu, na podlagi podatkov, ki jih bo prejemal s strežnika. Tekmovalci bodo imeli na razpolago [primer programske kode](https://github.com/RoboLiga/ev3-nabiralec) v jeziku Python.

## Časovnica

| **Kdaj?** | **Kaj?** |
| --- | --- |
| 20. 10. 2024 | konec zbiranja prijav |
| 25. 10. 2024, 14:30 v R2.38 | prvo srečanje s prijavljenimi ekipami (predstavitev izziva, razdelitev kompletov) |
| XX. 11. 2024, 16:30 | uvodna delavnica (testni poligon)|
| XX. 11. 2024, 11:00 | 1. uradni trening (testni poligon) |
| XX. 11. 2024, 11:00 | 2. uradni trening (testni poligon) |
| 5. 12. 2024, 10:00 | zaključno tekmovanje (avla FRI) |

## Sestavni deli izziva

### Poligon

Poligon je ravno območje, po katerem se lahko gibljejo roboti - čistilci. Sestavljen je iz penastih plošč, ki jih obdaja ograja,znotraj poligona sta na eni strani rdeč in črn koš ter na drugi moder in zelen, ki služita tudi, kot bar.

Velikost: 2 m x 3,5 m
Obdaja ga ograja iz pleksi stekla – ograja ni trdna in ni namenjena zaletavanju.
koši za smeti:
postavljeni na nasprotnih straneh poligona
modre, zelene, rdeče ter črne barve
velikost vsakega koša: približno 1 m x 0,5 m
štirikotnik, ki definira koš za smeti, je določen v nastavitvah sledilnika.

### Smeti
Na površini poligona se nahajajo kosi smeti, ki so predstavljeni z lesenimi kvadri:

velikost (D x Š x V): 10 cm x 10 cm x 8 cm,
na vrhu je značka za kamero,
Steklenica je zelene barve, Plastika pa rdeče barve,
strežnik vsakemu kosu smeti določi naključno identifikacijsko številko (id),
ko se ustvari nova tekma (Create a new game) in
ko se tekma prične (Start the game).

### Školjke
na površini poligona se nahajajo tudi školjke, ki so predstavljene z lesenimi kvadri.
velikost (D x Š x V): 10 cm x 10 cm x 8 cm
Školjke so modre barve
na vrhu je značka za kamero
strežnik vsaki školjki določi naključno identifikacijsko številko (id),
ko se ustvari nova tekma (Create a new game) in
ko se tekma prične (Start the game).



![Poligon-sadovnjak](https://github.com/RoboLiga/roboliga-meta/raw/master/poligon.jpg)

      
### Ruda

Na površini poligona se nahajajo kosi rude, ki so predstavljeni z lesenimi kvadri:

- velikost (D x Š x V): 10 cm x 10 cm x 8 cm,
- na vrhu je značka aruco za kamero,
- kos rude, ki vsebuje unobtainij, je zelene barve, jalovina je rjave barve,
- strežnik vsakemu kosu rude določi naključno identifikacijsko številko (`id`),
  - ko se ustvari nova tekma (*Create a new game*) in
  - ko se tekma prične (*Start the game*).

### Robot čistilec
Robota čistilca sestavite iz kock Lego, ki so prisotne v kompletu, in napišete program, ki se bo izvajal na njem. Pri oblikovanju morate biti iznajdljivi, da konstrukcijo robota čim bolj prilagodite izzivu. Ob tem morate upoštevati naslednje omejitve:

Robot je lahko izdelan iz kompletov Lego Mindstorms EV3, druge različice niso dovoljene.
Izdelan robot lahko vsebuje eno programirljivo kocko, največ tri motorje in največ štiri tipala. Dovoljene vrste tipal so: barvno/svetlobno, ultrazvočno, žiroskop in tipalo za dotik.
Največja dovoljena velikost gum je 56 mm x 26 mm.
Robot lahko na začetku tekme meri največ 50 cm x 50 cm x 50 cm.
Robot mora imeti na vrhu prostor za namestitev značke, ki bo vidna kameri.
- Programirate lahko v poljubnem programskem jeziku. Organizatorji nudimo [podporo za Python](https://github.com/RoboLiga/ev3-nabiralec).
Med tekmo lahko robota prime samo sodnik.
Hkrati bosta v eni tekmi tekmovala dva robota.
Na začetku tekme bodo sodniki postavili robota tako, da bo njegov skrajni sprednji del poravnan s tistim robom njegovega koša za plastiko, ki gleda proti sredini poligona. Robot bo tako sceloma v svojem odlagališču.
V času tekme je robotu dovoljena povezava izključno na strežnik, ki nudi podatke o tekmi, in ne na druge naprave.
Program na robotu lahko zaženete preko tipk na kocki ali oddaljeno preko SSH.

## Tekma

Tekma je dvoboj med dvema robotoma. Njun cilj je v omejenem času zbrati čim več točk. Točke pridobiva s pravilnem recikliranjem, školjke pa pomenijo negativne točke.

Trajanje tekme: do 3 minute
Pridobivanje točk:
  -vsaka smet v pravilnem košu, ekipi prinese točko, če je smet v napačnem košu ne pridobiš     točke,
  -vsaka školjka na odlagališču odšteje 2 točki.
  -podatka o vrsti smeti robot ne dobi iz strežnika in ga mora pridobiti sam (uporaba barvnega   tipala, s poskušanjem)
  da je smet v košu, štejemo takrat, ko je središče značke znotraj odlagališča,
  v primeru, da sledilnik ne prepozna značke, o točkovanju odloča sodnik. 
  Primeri:
    -smet je prevrnjena in njegova oznaka ni več vidna,
    -značka smeti je prekrita z drugim objektom.
    -vrsta koša za smeti bo definirana na strežniku.
Vloga Bara:
  -robot ima na začetku tekme na voljo dovolj energije in volje za 25 sekund delovanja,
  -spočije se v enemu od Barov, ki se nahajajo v koših .
  -Počitek, ki mora trajati vsaj 5 sekund, mu prinese dodatnih 25 sekund,
  -preostanek energije, ki jo ima robot na voljo, pridobi iz strežnika,
  -če robotu zmanjka energije (časa), se do konca tekme ne sme več premikati,
  -ko je robot na polnilni postaji, se količina njegove energije ne prazni.
  -Robotu se je dovoljeno premikati po vsej površini poligona, vključno z odlagališčema.
Protokol tekme:
  -priprava na tekmo: tekmovalni ekipi sta povabljeni, da postavita svojega robota na začetni     položaj. Robota morata biti prižgana in povezana na strežnik.
začetek tekme: 
  -strežnik oznani začetek tekme z zastavico v podatkih o tekmi.
konec tekme: 
  -strežnik oznani konec tekme z zastavico v podatkih o tekmi. Možni načini 
    konca tekme:
      -pretek časa,
      -obema robotoma zmanjka energije,
      -diskvalifikacija obeh robotov, 
      -po presoji sodnika.
Če se robot začne premikati pred začetkom tekme, se tekma razveljavi in se vrnemo v pripravo na tekmo. Če robot to stori dvakrat v sklopu iste tekme, je diskvalificiran in tekma se ponovi samo za preostalega robota.
Predvidoma bo tekmovanje sestavljeno iz dveh delov. V prvem bodo ekipe razdeljene v skupine, dvoboji pa bodo potekali po načelu vsak z vsakim. Najvišje uvrščene ekipe glede na število točk se potem pomerijo še v izločilnih bojih. Začetni tekmovalni pari izločilnih bojev se določijo glede na izkupiček točk skupinskega dela.

## Sodnik

- Sodnik ima absolutno diskrecijsko pravico.
- Sodnik lahko prekine tekmo, če presodi, da se stanje točk ne bo spremenilo (npr. oba robota obtičita, se sploh ne odzivata, tekmovalci vdrejo na poligon ipd.).

## Testni poligon

Za lažje priprave na tekmovanje, smo pripravili testni poligon. Nahaja se na Fakulteti za računalništvo in informatiko v 2. nadstropju. Prostor ima oznako R2.38 in je v bližini Laboratorija za adaptivne sisteme in paralelno procesiranje (R2.41), kjer smo organizatorji Robo lige FRI. Za boljšo orientacijo si oglejte [načrt prostorov](https://github.com/RoboLiga/roboliga-meta/raw/master/Na%C4%8Drt_FRI_2nadstropje.pdf).

V prostor s poligonom lahko pridete le s posebnim elektronskim ključem. Ključ prevzamete pri vratarju in ga po končanem delu tja tudi vrnete. Vrata odklenete tako, da elektronski ključ približate črni ploščici na levi strani vrat. Ko so vrata odklenjena, zasveti zelena lučka. V sobi je postavljen poligon iz penastih plošč, na stropu je širokokotna spletna kamera.

**Pravila obnašanja**
- Prepovedano je stopiti na penasto ploščo, saj se takoj umaže in deformira.
- V prostoru skrbite za red in čistočo.
- Ko zapuščate prostor, ugasnite vse luči in zaprite okna.
- Zaklepajte vrata za seboj. To storite tako, da elektronski ključ približate črni ploščici na levi strani vrat; zasveti oranžna lučka.
- V primeru težav se obrnite na organizatorje.


--------------------------
> Organizatorji si pridržujemo pravico do spremembe in dopolnitve nalog ter tekmovalnih pravil.

