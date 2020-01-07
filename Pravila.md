Pravila
================================

## Zgodba

(Pretekle dogodivščine Janeza in Franca lahko najdete v [lanskih pravilih](https://github.com/RoboLiga/roboliga-meta/blob/20182019/Pravila.md).)

Prišlo je poletje 2019 in sadovnjaki so samevali. Le redko-katera veja se je šibila pod težo sadja. Roboti so hitro pobrali ubogi pridelek in še  preden bi lahko oče sadovnjak predal enemu od sinov, je k njemu prišla multinacionalka, ki je tam hotela postaviti tovarno. Za kmetijsko zemljišče mu je ponudila trikratnik vrednosti v registru nepremičnin na portalu E-prostor Geodetske uprave Republike Slovenije.

Rešitev je bila sedaj preprosta: vsak od sinov je lahko dobil polovico denarja. Vendar sta kmalu ugotovila, da denar ni vse in da bogastvo s seboj prinese dolžnosti do družbe in socialnega okolja.

Da bi poskrbela, da se podobna katastrofa ne bi pripetila še drugim in bi hkrati očistila svojo vest, ker sta v svojo vas pripeljala velikega onesnaževalca, sta se sinova Janez in Franc odločila, da bosta postala čebelarja. Tako bosta lahko svoje čebele vozila v sadovnjake na pašo, kjer bodo oprašile drevesa, v zameno pa bosta dobila med.

Med je seveda boljši, če ga čebele naberejo na bolj eksotičnih rastlinah, zato sta Janez in Franc naročnike začela iskati čim dlje stran od doma. Ker pa stari oče potrebuje skrb svojih sinov, ne moreta biti dolgo zdoma, zato sta se odločila, da bosta svoje panje naredila samo-vozeče. In tako pomoč spet iščeta pri najboljših izdelovalcih samostojnih robotov - pri vas.

## Opis izziva

Vsaka ekipa sestavi svojega avtonomnega robota – nabiralca. Roboti tekmujejo na poligonu, ki predstavlja sadovnjak. Na njem se nahajajo jabolka, ki so lahko zdrava ali gnila, in dve shrambi. Naenkrat tekmujeta dva avtonomna robota, ki imata nalogo, da v omejenem času v svojo shrambo prineseta čim več zdravih jabolk in poskrbita, da je v njej čim manj gnilih. Robota navigirata po sadovnjaku s pomočjo podatkov, ki jim jih preko brezžičnega omrežja pridobita s strežnika. Slednji budno spremlja dogajanje v sadovnjaku s pomočjo kamere nameščene nad njim.

## Potrebna znanja in veščine

Ekipe potrebujejo osnovno znanje programiranja in veselje do sestavljanja lego kock. Zelo pomemben je občutek za delo v skupini in zagnanost za reševanje novih izzivov.

Tekmovalci izdelajo program, ki se izvaja na robotu Lego Mindstorms EV3. Izbirajo lahko med množico programskih jezikov, med katerimi je najbolj priljubljen Python. Program mora poskrbeti za naslednje naloge:

1. Vzpostaviti mora Brezžično (Wi-Fi) povezavo z strežnikom, ki bo robota oskrboval s podatki o dogajanju na poligonu. Tekmovalci bodo imeli na razpolago podrobno tehnično dokumentacijo in primere programske kode v jeziku Python.
2. Robot mora avtonomno voziti po poligonu, na podlagi podatkov, ki jih bo prejemal iz strežnika.

## Časovnica

| **Kdaj?** | **Kaj?** |
| --- | --- |
| 18. 1. 2019 | konec zbiranja prijav |
| 30. 1. 2019 ob 12:30 v P04 | prvo srečanje s prijavljenimi ekipami (predstavitev izziva, razdelitev kompletov) |
| 21. 2. 2019 ob 14:00 v R2.38 | 1. uradni trening (testni poligon) |
| 7. 3. 2019 ob 14:15 v R2.38 | 2. uradni trening (testni poligon) |
| 13. 3. 2019 ob 14:00 v avli FRI | zaključno tekmovanje |

## Sestavni deli izziva

### Sadovnjak

Sadovnjak je ravno območje, po katerem se lahko gibljejo roboti - nabiralci. Sestavljen je iz penastih plošč, ki jih obdaja ograja, znotraj pa sta označeni barvni območji, ki predstavljata nabiralni košari.

- Velikost:  2 m x 3,5 m
- Obdaja ga ograja iz pleksi stekla – ograja ni trdna in ni namenjena zaletavanju.
- Košari za nabiranje jabolk:
  - postavljeni na robovih poligona
  - modre oziroma rdeče barve
  - velikost košare: približno 1 m x 0,5 m,
  - štirikotnik, ki definira območje košare, je določen v nastavitvah sledilnika.

![Poligon-sadovnjak](https://github.com/RoboLiga/roboliga-meta/raw/master/poligon.jpg)

      
### Jabolka

Na površini sadovnjaka se nahajajo jabolka, ki so predstavljena z lesenimi kvadri:

- velikost (D x Š x V): 10 cm x 10 cm x 8 cm,
- na vrhu je oznaka za kamero,
- barva zdravih jabolk je zelena, gnilih pa rjava.

### Robot nabiralec

Nabiralnega robota sestavite iz kock Lego, ki so prisotne v kompletu, in napišete program, ki se bo izvajal na njem. Pri oblikovanju morate biti iznajdljivi, da konstrukcijo robota čim bolj prilagodite izzivu. Ob tem morate upoštevati naslednje omejitve:

- Robot je lahko izdelan iz kompletov Lego Mindstorms EV3, druge različice niso dovoljene.
- Izdelan robot lahko vsebuje eno programirljivo kocko, največ tri motorje in največ štiri tipala. Dovoljene vrste tipal so: barvno/svetlobno, ultrazvočno, žiroskop in tipalo za dotik.
- Največja dovoljena velikost gum je 56 mm x 26 mm.
- Robot lahko na začetku tekme meri največ 30 cm x 30 cm x 30 cm.
- Robot mora imeti na vrhu prostor za namestitev označbe, ki bo vidna kameri.
- Programirate lahko v poljubnem programskem jeziku. Organizatorji nudimo podporo za Python.
- Med tekmo lahko robota prime samo sodnik.
- Predvidoma bosta hkrati v eni tekmi tekmovala dva robota.
- Na začetku tekme bodo sodniki postavili nabiralca tako, da bo njegov skrajni sprednji del poravnan s tistim robom njegove košare, ki gleda proti sredini poligona. Nabiralec bo tako sceloma v svoji košari in približno usredinjen glede na daljši rob košare.
- V času tekme je dovoljena povezava izključno na strežnik, ki nudi podatke o tekmi, in ne na druge naprave.
- Program na robotu lahko zaženete preko tipk na kocki ali oddaljeno preko SSH.

## Tekma

Tekma je dvoboj med dvema nabiralcema. Njun cilj je v omejenem času zbrati čim več točk. Točke pridobiva z nabiranjem zdravih jabolk v svojo košaro, gnila jabolka v košari pa pomenijo negativne točke.

- Trajanje tekme: do 3 minute
- Pridobivanje točk:
  - vsako zdravo jabolko, ki se pojavi v košari, nabiralcu prinese 1 točko,
  - vsako gnilo jabolko v košari nabiralcu odšteje 2 točki,
  - da je jabolko v košari, štejemo takrat, ko je središče njegove oznake znotraj košare,
  - v primeru, da sledilnik ne prepozna oznake jabolka, o točkovanju odloča sodnik. Primeri:
    - jabolko je prevrnjeno in njegova oznaka ni več vidna,
    - oznaka jabolka je prekrita z drugim objektom.
- Zmagovalec je tisti nabiralec, ki ima po izteku časa več točk. V primeru izenačenega števila točk, zmaga tisti, ki ima več zdravih jabolk. V primeru, da je tudi število zdravih jabolkov izenačeno, zmaga tisti, ki je prej v svojo košaro prinesel zadnje zdravo jabolko.
- Sodnik sproti odstranjuje zdrava jabolka iz košare, pri čemer gnilih ne in jih lahko robot premika po sadovnjaku do konca tekme.
- Robotu se je dovoljeno premikati po vsej površini sadovnjaka, vključno s košarama.
- Protokol tekme:
  - priprava na tekmo: tekmovalni ekipi sta povabljeni, da postavita svojega robota na začetni položaj. Robota morata biti prižgana in povezana na strežnik.
  - začetek tekme: strežnik oznani začetek tekme z zastavico v podatkih o tekmi.
  - konec tekme: strežnik oznani konec tekme z zastavico v podatkih o tekmi. Možni načini konca tekme:
    - pretek časa,
    - diskvalifikacija obeh robotov,
    - po presoji sodnika.
- Če se robot začne premikati pred začetkom tekme, tekma razveljavi in se vrnemo v pripravo na tekmo. Če robot to stori dvakrat v sklopu iste tekme, je diskvalificiran in tekma se ponovi samo za preostalega robota.

Predvidoma bo tekmovanje sestavljeno iz dveh delov. V prvem bodo ekipe razdeljene v skupine, dvoboji pa bodo potekali po načelu vsak z vsakim. Najvišje uvrščene ekipe glede na število točk se potem pomerijo še v izločilnih bojih. Začetni tekmovalni pari izločilnih bojev se določijo glede na izkupiček točk skupinskega dela.

## Sodnik

- Sodnik ima absolutno diskrecijsko pravico.
- Sodnik lahko prekine tekmo, če presodi, da se stanje točk ne bo spremenilo (npr. oba robota obtičita, se sploh ne odzivata, tekmovalci vdrejo na poligon ipd.).
- Sodnik lahko na prošnjo člana ekipe premakne njenega robota v začetni položaj (ponastavitev). Vsaka ekipa lahko zaprosi za ponastavitev robota največ 2-krat na tekmo. To stori tako, da član ekipe sodniku zavpije "Reset!". Če sta nabiralca obeh tekmujočih ekip zapletena, je prošnja po ponastavitvi ugodena samo ob strinjanju obeh ekip. Izjema: če je ena od obeh ekip že porabila vse možnosti za ponastavitev nabiralca, se v primeru medsebojnega zapleta druga ekipa sama odloča glede ponastavitve svojega robota. Ponastavita se oba nabiralca. 

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

