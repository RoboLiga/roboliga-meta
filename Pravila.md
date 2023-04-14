Pravila
================================

## Opis izziva

Letošnji izziv postavi robota v vlogo rudarja, ki mora v omejenem času nabrati čim več dragocenega unobtanija in ga pripeljati domov in s tem prinesti zmago svoji ekipi.

Vsaka ekipa sestavi svojega avtonomnega robota – rudarja. Roboti tekmujejo na poligonu, ki predstavlja rudnik unobtainija. V rudniku se nahajajo kosi rude, ki lahko vsebujejo unobtainij ali pa tudi ne.

Naenkrat tekmujeta dva avtonomna robota, ki imata nalogo, da na svoje odlagališče prineseta čim več unobtainija in poskrbita, da je v njem čim manj jalovine – torej rude brez dragocenega elementa. Robot ugotovi prisotnost elementa v rudi šele, ko naredi podrobno kemično analizo.

Za svoje rudarske aktivnosti ima robot omejeno količino goriva. Svojo zalogo lahko napolni na posebnih površinah polnilne postaje.

Robota navigirata po poligonu s pomočjo podatkov, ki jih preko brezžičnega omrežja pridobita s strežnika. Slednji budno spremlja dogajanje na poligonu s pomočjo kamere nameščene nad njim.

## Potrebna znanja in veščine

Ekipe potrebujejo osnovno znanje programiranja in veselje do sestavljanja lego kock. Zelo pomemben je občutek za delo v skupini in zagnanost za reševanje novih izzivov.

Tekmovalci izdelajo program, ki se izvaja na robotu Lego Mindstorms EV3. Izbirajo lahko med množico programskih jezikov, med katerimi je najbolj priljubljen Python. Program mora poskrbeti za naslednje naloge:

1. Vzpostaviti mora Brezžično (Wi-Fi) povezavo z strežnikom, ki bo robota oskrboval s podatki o dogajanju na poligonu.
2. Robot mora avtonomno voziti po poligonu, na podlagi podatkov, ki jih bo prejemal s strežnika. Tekmovalci bodo imeli na razpolago [primer programske kode](https://github.com/RoboLiga/ev3-nabiralec) v jeziku Python.

## Časovnica

| **Kdaj?** | **Kaj?** |
| --- | --- |
| 26. 2. 2023 | konec zbiranja prijav |
| 3. 3. 2023, 11:00 v P03 | prvo srečanje s prijavljenimi ekipami (predstavitev izziva, razdelitev kompletov) |
| 9. 3. 2023, 16:30 | uvodna delavnica (testni poligon)|
| 31. 3. 2023, 11:00 | 1. uradni trening (testni poligon) |
| 14. 4. 2023, 11:00 | 2. uradni trening (testni poligon) |
| 19. 4. 2023, 10:00 | zaključno tekmovanje (avla FRI) |

## Sestavni deli izziva

### Poligon

Poligon je ravno območje, po katerem se lahko gibljejo roboti - rudarji. Sestavljen je iz penastih plošč, ki jih obdaja ograja, znotraj pa sta z modro oziroma rdečo barvo označeni območji, ki predstavljata odlagališči, in z zeleno barvo polnilne postaje.

- Velikost:  2 m x 3,5 m
- Obdaja ga ograja iz pleksi stekla – ograja ni trdna in ni namenjena zaletavanju.
- Odlagališči rude:
  - postavljeni na robovih poligona
  - modre oziroma rdeče barve
  - velikost skladišča: približno 1 m x 0,5 m
  - štirikotnik, ki definira območje skladišča, je določen v nastavitvah sledilnika.
- Polnilne postaje:
  - dve polnilni postaji
  - vsaka velikosti 0,5 m x 0,5 m
  - zelene barve.

![Poligon-sadovnjak](https://github.com/RoboLiga/roboliga-meta/raw/master/poligon.jpg)

      
### Ruda

Na površini poligona se nahajajo kosi rude, ki so predstavljeni z lesenimi kvadri:

- velikost (D x Š x V): 10 cm x 10 cm x 8 cm,
- na vrhu je značka aruco za kamero,
- kos rude, ki vsebuje unobtainij, je zelene barve, jalovina je rjave barve,
- strežnik vsakemu kosu rude določi naključno identifikacijsko številko (`id`),
  - ko se ustvari nova tekma (*Create a new game*) in
  - ko se tekma prične (*Start the game*).

### Robot rudar

Robota rudarja sestavite iz kock Lego, ki so prisotne v kompletu, in napišete program, ki se bo izvajal na njem. Pri oblikovanju morate biti iznajdljivi, da konstrukcijo robota čim bolj prilagodite izzivu. Ob tem morate upoštevati naslednje omejitve:

- Robot je lahko izdelan iz kompletov Lego Mindstorms EV3, druge različice niso dovoljene.
- Izdelan robot lahko vsebuje eno programirljivo kocko, največ tri motorje in največ štiri tipala. Dovoljene vrste tipal so: barvno/svetlobno, ultrazvočno, žiroskop in tipalo za dotik.
- Največja dovoljena velikost gum je 56 mm x 26 mm.
- Robot lahko na začetku tekme meri največ 50 cm x 50 cm x 50 cm.
- Robot mora imeti na vrhu prostor za namestitev značke, ki bo vidna kameri.
- Programirate lahko v poljubnem programskem jeziku. Organizatorji nudimo [podporo za Python](https://github.com/RoboLiga/ev3-nabiralec).
- Med tekmo lahko robota prime samo sodnik.
- Hkrati bosta v eni tekmi tekmovala dva robota.
- Na začetku tekme bodo sodniki postavili robota tako, da bo njegov skrajni sprednji del poravnan s tistim robom njegovega odlagališča, ki gleda proti sredini poligona. Robot bo tako sceloma v svojem odlagališču in približno usredinjen glede na daljši rob.
- V času tekme je robotu dovoljena povezava izključno na strežnik, ki nudi podatke o tekmi, in ne na druge naprave.
- Program na robotu lahko zaženete preko tipk na kocki ali oddaljeno preko SSH.

## Tekma

Tekma je dvoboj med dvema robotoma. Njun cilj je v omejenem času zbrati čim več točk. Točke pridobiva z zbiranjem unobtainija na svojem odlagališču, jalovina pa pomeni negativne točke.

- Trajanje tekme: do 3 minute
- Pridobivanje točk:
  - vsak kos rude na odlagališču, ki vsebuje unobtainij, ekipi prinese točko,
  - vsak kos jalove rude na odlagališču odšteje 2 točki,
  - podatka o kvaliteti kosa rude robot ne dobi iz strežnika in ga mora pridobiti sam (uporaba barvnega tipala, s poskušanjem)
  - da je kos rude na odlagališču, štejemo takrat, ko je središče značke znotraj odlagališča,
  - v primeru, da sledilnik ne prepozna značke rude, o točkovanju odloča sodnik. Primeri:
    - kos rude je prevrnjen in njegova oznaka ni več vidna,
    - značka rude je prekrita z drugim objektom.
- Vloga polnilnih postaj:
  - robot ima na začetku tekme na voljo dovolj goriva za 25 sekund delovanja,
  - gorivo si napolni na polnilni postaji,
  - polnjenje, ki mora trajati vsaj 5 sekund, mu prinese dodatnih 25 sekund,
  - preostanek goriva, ki ga ima robot na voljo, pridobi iz strežnika,
  - če robotu zmanjka goriva (časa), se do konca tekme ne sme več premikati,
  - na polnilni postaji se lahko polni največ en robot naenkrat (prvi pride, prvi polni),
  - ko je robot na polnilni postaji, se količina njegovega goriva ne zmanjšuje (v primeru, da pride prvi na postajo).
- Robotu se je dovoljeno premikati po vsej površini poligona, vključno z odlagališčema.
- Protokol tekme:
  - priprava na tekmo: tekmovalni ekipi sta povabljeni, da postavita svojega robota na začetni položaj. Robota morata biti prižgana in povezana na strežnik.
  - začetek tekme: strežnik oznani začetek tekme z zastavico v podatkih o tekmi.
  - konec tekme: strežnik oznani konec tekme z zastavico v podatkih o tekmi. Možni načini konca tekme:
    - pretek časa,
    - obema robotoma zmanjka goriva,
    - diskvalifikacija obeh robotov,
    - po presoji sodnika.
- Če se robot začne premikati pred začetkom tekme, se tekma razveljavi in se vrnemo v pripravo na tekmo. Če robot to stori dvakrat v sklopu iste tekme, je diskvalificiran in tekma se ponovi samo za preostalega robota.

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

