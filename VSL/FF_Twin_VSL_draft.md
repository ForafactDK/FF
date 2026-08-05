# FF Twin — VSL Draft
**Salgspitch til grundlæggere og beslutningstagere i drone-startups**
*Version 0.4 — juni 2026*

---

## Målgruppe og salgsproces

**Hvem VSL'en taler til:**
Grundlæggeren, CEO'en eller den forretningsansvarlige i en drone-virksomhed. Den person der kontrollerer budgettet, taler med investorer og er ansvarlig for at dronen når marked til tiden — og med den rette performance.

**Hvad VSL'en skal opnå:**
Skabe tilstrækkelig interesse til at grundlæggeren inviterer til et møde, hvor Finn deltager og besvarer de tekniske spørgsmål fra deres CTO, lead engineer og drone-ingeniører. VSL'en åbner døren — mødet lukker tilliden.

**Teknisk dybde hører til mødet, ikke til VSL'en.**

---

## ICP (Ideal Customer Profile)

**Primær ICP — version 1 til version 2:**
Grundlæggeren af en drone-startup der har investeret 2–3 år og betydelig kapital i en første prototype. Dronen flyver og udfører sin mission. Nu skal de beslutte hvad version 2 skal indeholde — og de har stadig ikke et solidt beregningsgrundlag at bygge de beslutninger på.

**Sekundær ICP — starter fra scratch:**
*(Kræver separat VSL — anden hook, andre argumenter)*
Grundlæggeren der er ved at starte udviklingen af sin første drone. Her er det primære argument tidsbesparelse og at springe 5–6 prototype-iterationer over. Dette adresseres i en fremtidig version.

**Deres forretningsmæssige situation:**
De har rejst kapital eller er ved at gøre det. De er under pres for at nå markedet. De vil gerne kunne fortælle investorer at deres design er verificeret og optimalt. Men de har hidtil udviklet på mavefornemmelse, inspiration fra andre og trial-and-error — ikke på præcise beregninger. De ved ikke hvad de ikke ved.

**Primære forretningsmæssige smerter:**
1. De ved ikke om deres drone performer optimalt — og har intet at sammenligne med.
2. De skal tage de største designbeslutninger til v2 med den samme ufuldstændige information de startede med.
3. Hver ekstra prototype-iteration koster tid og kapital de ikke har råd til at spilde.

---

## Trin 1 — HOOK

**Primær hook:**
> **"Du har investeret år og millioner i at bygge en drone der flyver. Men ved du om den er konkurrencedygtig — eller om du bare er tilfreds fordi den virker?"**

**Alternativ hook (investor-vinkel):**
> **"Dine investorer spørger snart om dit drone-design er verificeret og optimalt. Hvad svarer du?"**

**Alternativ hook (60%-varianten — mere teknisk, god i miljøer med teknisk baggrund):**
> **"60% af din drones energiforbrug går til én ting. Hvornår sidst optimerede du den?"**

---

## Trin 2 — PROBLEM

Du har bygget noget der virker. Det er i sig selv en bedrift. Men "det virker" er ikke det samme som "det er optimalt" — og i en industri der bevæger sig hurtigt, er forskellen afgørende.

De beslutninger der definerede din version 1 blev taget med ufuldstændige data. Komponenterne blev valgt enkeltvis frem for som et sammenhængende system. Designet blev itereret frem gennem fysiske prototyper — dyrt, langsomt og uden fuld indsigt i hvad der faktisk skabte problemerne.

Her er hvad den iterative loop faktisk koster:

3 måneder at bygge en prototype. 3–6 måneder at debugge og flyve tests. Dertil analyse — og den analyse er aldrig fuldstændig, fordi du kun kan måle dronens samlede energiforbrug. Du kan ikke se hvad der udgør det. Så beslutningen om hvad du skal ændre næste gang er i bedste fald delvist kvalificeret — i værste fald et gæt.

En ny prototype bygges. Loopen starter forfra. 5–6 iterationer = 2–3 år.

Kontrolsystemet kompenserer løbende for inefficienserne og gør dem usynlige. Du ved aldrig at du har et designproblem — du ved bare at det fungerer.

Og det er ikke fordi du har gjort noget forkert. Det er fordi der hidtil ikke har eksisteret et tilgængeligt værktøj der kobler dine forretningsmål direkte til et præcist drone-design.

---

## Trin 3 — AGITATION

Dine konkurrenter der har adgang til præcis aerodynamisk modellering itererer hurtigere. De undgår de prototype-runder du betaler for. De ankommer til markedet på et fundamentalt andet grundlag.

Og der er et argument der bliver vigtigere for hvert kvartal: din investorcase. Virksomheder der kan dokumentere at deres drone-design er verificeret af specialiseret ekspertise — ikke bare "vi har testet det og det virker" — har et stærkere fundament i fundraising-samtaler. Det er ikke et hypotetisk argument. Det er noget vores eksisterende kunder bruger aktivt.

Hvert udviklingsår der kan komprimeres, er kapital der ikke spildes. Hver prototype-iteration der kan erstattes af en simulering, er måneder du vinder og penge du beholder.

---

## Trin 4 — LØSNING

FF Twin er en simulerings- og optimeringsplatform for UAV'er — fra droner og multirotorer til fixed-wing og VTOL-systemer. Den er bygget til at operere på forretningsmål: du beskriver hvad du vil opnå, platformen beregner hvordan du kommer derhen.

**Du behøver ikke ansætte en aerospace PhD for at få adgang til den ekspertise.**

Det der normalt kræver uger af konfigurationsarbejde i tunge simuleringsværktøjer som Ansys — boundary conditions, mesh-strukturer, kalibreringsprocedurer for netop din drone — er kodet direkte ind i FF Twins workflow. Finn Matras har brugt år på at vide præcis hvordan de aerodynamiske modeller skal sættes op, justeres og fortolkes for UAV-systemer. Den viden er tilgængelig for dig via platformen, fra dag ét.

Platformen følger dig fra den første idé til fuld operation:

*1. Design og optimering → 2. Styring og kontrol → 3. Digital twin og vedligehold*

Du starter ikke forfra hver gang. Modellen du bygger i fase 1 er den samme der driver fase 2 og 3. Du bygger videre på et fundament der vokser med dig.

---

## Trin 5 — AUTORITET & TROVÆRDIGHED

FF Twin er skabt på baggrund af årelangt, specialiseret PhD-niveau forsknings- og konsulentarbejde inden for drone-aerodynamik — og gjort tilgængeligt som en brugervenlig platform.

Finn Matras, PhD fra NTNU (Norges teknisk-naturvitenskapelige Universitet), er en award-winning forsker og en af de meget få specialister i verden der har formaliseret dynamisk inflow-modellering for multirotor-systemer. Hans forskning er publiceret og peer-reviewed i *The Aeronautical Journal* (Cambridge University Press, 2025) og *Wind Energy Science* (Copernicus, 2025).

Den reelle defensibility er ikke hemmelig matematik — de underliggende fysikligninger er velkendte og accepterede. Det der er svært at kopiere er *orchestreringen*: at vide præcis hvordan modellerne kombineres, hvilke aerodynamiske forenklinger der er sikre at lave for UAV'er uden at miste nøjagtighed, og hvordan output skal fortolkes i en konkret designkontekst. En konkurrent der forsøger at bygge det samme står over for årelangt trial-and-error. Vi har allerede gjort det arbejde — og pakket det ind i et system du kan bruge fra dag ét.

*Troværdighed i praksis bygges løbende på kundereferencer. Se trin 7.*

---

## Trin 6 — FEATURES → FORDELE

**Du finder ud af præcis hvad der koster dig energi — og hvad der ikke gør**

Din drone producerer ét samlet energiforbrug. Vi opdeler det i de tre komponenter der rent faktisk driver dit energibudget: induced power (propellernes inflow-interaktioner), profile power (aerodynamik på krop, arme og vinger) og parasitic power (mekanisk modstand og strukturel ineffektivitet). Kun FF Twin kan give dig den opdeling — fordi det kræver præcis modellering af alle tre. Når vi kan se at én parameter er langt uden for hvad den bør være, ved vi præcist hvad du skal fokusere din næste investering på — og hvad der *ikke* er problemet. Den indsigt har du ikke i dag.

**Du undgår prototype-runder — ikke bare én, men flere**

Én iteration i FF Twin tager sekunder til minutter. Optimeringsalgoritmen kører loopen selv og finder den bedste løsning automatisk. Det der ellers ville koste dig 3 måneder at bygge og 3–6 måneder at teste, kan du se resultatet af på dage. Virksomheder der starter udvikling uden præcis modellering bruger typisk 5–6 fysiske prototype-iterationer på at nå et modent design. Med FF Twin kan mange af de iterationer erstattes af simulering.

**Dine designbeslutninger tager minutter, ikke måneder**

Det der tager en aerodynamikekspert uger at konfigurere i Ansys, tager minutter i FF Twin. Systemet er bygget til din profil — ikke til en generisk ingeniørworkflow.

**Du kan custom-tilpasse din drone per kundeordre**

Når dit grunddesign er modelleret, kan vi på minutter beregne en variant optimeret til en specifik kundes behov — anden cargo-vægt, anden mission, anden flyveregime. I stedet for én standarddrone du sælger til alle, har du en basisplatform du tilpasser per ordre med de rette aerodynamiske specifikationer til kundens specifikke situation. Det er et nyt konkurrencefortrin du ikke kan tilbyde uden et system som FF Twin.

**Din investorcase bliver stærkere**

"Vores design er verificeret af specialiseret PhD-ekspertise" er et håndgribeligt argument i fundraising-samtaler. Det er ikke et argument du kan bruge, hvis du har itereret dig frem på mavefornemmelse.

**Træn din pilots kunder inden dronen er bygget**

Fordi FF Twin's model beskriver præcis hvordan din drone flyver, kan slutkunden begynde at træne sin pilot i en simulator måneder før dronen er leveret. Dag 1 med den rigtige drone er allerede dag 300 i simulatoren. Det er en serviceydelse du kan tilbyde — og sælge — til dine kunder.

**Du ved hvornår en komponent fejler — inden det sker**

I driftsfasen sammenligner FF Twin løbende faktiske flyvedata med modellens forudsigelse. Afvigelser detekteres og diagnosticeres automatisk: hvilken komponent, hvad er forkert, og hvornår estimeres fejlen at blive kritisk. For en flåde på 500 droner er det forskellen på planlagt vedligehold og uventede nedbrud.

**Fra idé til operation — ét system**

Design, simulering, optimering, digital twin, pilot training og vedligehold. Du skifter ikke platform efterhånden som du vokser. Det hele hænger sammen og bygger på det samme fundament.

---

## Trin 7 — SOCIAL PROOF

*[Under aktiv opbygning — udbygges løbende med dokumenterede resultater]*

**Nuværende proxy:**
Finn Matras arbejder allerede med drone-virksomheder i Danmark og Norge. Én af dem bruger aktivt hans involvering i deres investordialog som dokumentation for at deres design er verificeret og optimeret. Forskningen bag platformen er peer-reviewed og anerkendt med priser.

*→ Glasvæg-modellen (vis konkrete resultater fra navngivne kunder) implementeres når 3–5 cases er dokumenterede.*

---

## Trin 8 — TILBUD (Sukker-modellen)

**Start her: Gratis energianalyse af din drone**

Lav en simpel flyvetest — dronen flyver frem og tilbage ved 4–6 forskellige hastigheder. Det tager under en time. Send os logdataene.

Vi analyserer og sender dig en rapport der viser:
- Præcis hvor din drone bruger sin energi — opdelt på de tre nøgleparametre (induced, profile, parasitic)
- Hvad der er veloptimeret og hvad der ikke er
- Et konkret estimat på forbedringspotentialet — og på hvilke parametre

Rapporten afslører hvad der faktisk sker i dit system. Den løser det ikke selv — men den giver dig et beregnet grundlag du ikke har i dag, og et konkret udgangspunkt for en samtale om hvad næste skridt er.

**Byttehandlen:** Vi bruger jeres testdata til at validere og udbygge vores modeller. I får en analyse baseret på specialiseret ekspertise. Ingen forpligtelse.

*Denne model gælder for de første kunder i opstartsfasen. Herefter evalueres overgang til betalt analyse som standard entry-punkt (5–10.000 DKK), svarende til hvad Finn allerede leverer manuelt i dag.*

---

## Trin 9 — CALL TO ACTION

> **"Lav en simpel flyvetest. Send os loggen. Vi sender dig en rapport inden for 24 timer der viser præcist hvad din drone bruger energi på — opdelt på de tre nøgleparametre — og hvad der kan forbedres. Er du interesseret i hvad rapporten viser, tager vi en snak."**

---

## Dokumentstatus

**Implementeret i v0.4:**
- [x] Konkret workflow-tidslinje tilføjet til Problem: 3 mdr bygge + 3-6 mdr debug + analyse = iterationsomkostning
- [x] "Kun total P" som kerneproblem: de kan ikke se Pi/Pr/Pa — derfor er alle ændringer gæt
- [x] Tre faser tydeliggjort: Design (1x) → Styring/kontrol (løbende) → Digital twin/O&M (løbende)
- [x] Pilottræning tilføjet som feature (træn inden dronen eksisterer)
- [x] Predictive maintenance / digital twin feature tilføjet
- [x] Fasernes sammenhæng: én model driver alle tre faser
- [x] Optimeringsalgoritmen nævnt: systemet itererer selv, ikke bare manuelt
- [x] Fra v0.3: målgruppe grundlægger/CEO, UAV som kategori, workflow moat, custom-drone per ordre, investor-argument

**Mangler stadig:**
- [ ] Konkret tal på hvad én undgået prototype-iteration koster i DKK og måneder (Finn kan give bud)
- [ ] Konkrete kundehistorier til social proof
- [ ] Glasvæg-variant (bygges ved 3–5 cases)
- [ ] Separat VSL til ICP 2 (starter fra scratch)
- [ ] Tilpasning til kanal: video-script / landingsside / pitch-dokument
- [ ] Deep-dive på styringssystemer og kontrolhierarki (fase 2) — Finn skal bekræfte detaljeniveau for VSL
- [ ] Pilottræning-feature: bekræft om det er i scope for v1 eller fremtidig feature

**Næste session med Finn:**
- Bekræft tal: hvad koster én prototype-iteration typisk (DKK + måneder) for en drone-startup?
- Bekræft scope for fase 2 (styring/kontrol) og fase 3 (digital twin) — hvad er tilgængeligt nu vs. roadmap?
- Review: er pilottræning-feature korrekt beskrevet og i scope?
