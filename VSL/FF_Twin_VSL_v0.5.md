# FF Twin — VSL Draft
**Salgspitch til grundlæggere og beslutningstagere i drone-startups**
*Version 0.5 — juni 2026*

---

## Målgruppe og salgsproces

**Hvem VSL'en taler til:**
Grundlæggeren, CEO'en eller den forretningsansvarlige i en drone-virksomhed. Den person der kontrollerer budgettet, taler med investorer og er ansvarlig for at dronen når marked til tiden — og med den rette performance.

**Hvad VSL'en skal opnå:**
Skabe tilstrækkelig interesse til at grundlæggeren inviterer til et møde, hvor Finn deltager og besvarer de tekniske spørgsmål fra deres CTO, lead engineer og drone-ingeniører. VSL'en åbner døren — mødet lukker tilliden.

**Teknisk dybde hører til mødet, ikke til VSL'en.**

---

## ICP (Ideal Customer Profile)

**Primær ICP:**
Grundlæggeren af en drone-virksomhed der bygger eller har bygget en prototype. Dronen flyver og udfører sin mission. Men de mangler et beregnet grundlag for at vide om designet er optimalt — og hvad de præcist skal prioritere for at forbedre det.

Det gælder hvad enten de skal beslutte hvad version 2 indeholder, eller stadig er ved at iterere version 1 frem. Processen er den samme. FF Twin er relevant på begge stadier.

*(To-VSL-spørgsmål: En sekundær VSL målrettet dem der starter helt fra scratch — anden hook, andet argument om tidsbesparing og sprunget iterationer — afventer særskilt behandling.)*

**Deres forretningsmæssige situation:**
De har rejst kapital eller er ved at gøre det. De er under pres for at nå markedet. De vil gerne kunne fortælle investorer at deres design er verificeret og optimalt. Men de har hidtil udviklet på mavefornemmelse, inspiration fra andre og trial-and-error — ikke på præcise beregninger. De ved ikke hvad de ikke ved.

**Primære forretningsmæssige smerter:**
1. De ved at dronen kan forbedres — men ikke præcist hvilke dele der skal prioriteres.
2. Designbeslutningerne til næste version tages med den samme ufuldstændige information de startede med.
3. Hver ekstra prototype-iteration koster tid og kapital de ikke har råd til at spilde.

---

## Trin 1 — HOOK

**Primær hook:**
> **"Du har bygget en drone der flyver. Men ved du præcist hvad du skal ændre for at gøre den bedre?"**

**Alternativ hook (investor-vinkel):**
> **"Dine investorer spørger snart om dit drone-design er verificeret og optimalt. Hvad svarer du?"**

**Alternativ hook (energi-vinkel — mest relevant for teknisk publikum):**
> **"Din drone producerer ét samlet energiforbrug. Men du kan ikke se hvad der udgør det. Det er problemet."**

*(Note: Den tidligere 60%-hook er bevidst fjernet herfra som primær hook. Den er velkendt inden for helikopterteori — Johnsons "Helicopter Theory" — men ikke sikkert kendt af alle drone-grundlæggere. Den kan bruges i mødet med teknisk modpart, men er ikke stærk nok som åbner til en bred ICP.)*

---

## Trin 2 — PROBLEM

Du har bygget noget der virker. Men "det virker" er ikke det samme som "det er optimalt" — og i en industri der bevæger sig hurtigt, er forskellen afgørende.

De beslutninger der definerede dit design blev taget med ufuldstændige data. Komponenterne blev valgt enkeltvis frem for som et sammenhængende system. Designet blev itereret frem gennem fysiske prototyper — dyrt og langsomt — fordi der ikke fandtes et bedre alternativ.

Her er kerneproblemet: Du kan måle dronens samlede energiforbrug. Men du kan ikke se hvad der udgør det. Hvilken del af systemet der er veloptimeret. Hvilken der trækker mest. Hvad der rent faktisk holder dig tilbage. Så beslutningen om hvad du skal ændre næste gang er i bedste fald delvist kvalificeret — i værste fald et gæt.

Kontrolsystemet kompenserer løbende for inefficienserne og gør dem usynlige. Du ved aldrig at du har et designproblem — du ved bare at det fungerer.

Og det er ikke fordi du har gjort noget forkert. Det er fordi der hidtil ikke har eksisteret et tilgængeligt værktøj der kobler dine forretningsmål direkte til et præcist drone-design.

---

## Trin 3 — AGITATION

Det reelle valg du står over for er ikke om du vil optimere eller ej. Det er om du vil gøre det manuelt og håndholdt — som du har gjort hidtil — eller om du vil have et system der giver dig den indsigt direkte.

Virksomheder der allerede arbejder med præcis aerodynamisk modellering bruger færre fysiske iterationer for at nå det samme sted. De ankommer til markedet på et mere dokumenteret grundlag.

Og der er et argument der bliver vigtigere for hvert kvartal: din investorcase. Virksomheder der kan dokumentere at deres drone-design er verificeret af specialiseret ekspertise — ikke blot "vi har testet det og det virker" — har et stærkere fundament i fundraising-samtaler. Det er ikke et hypotetisk argument. Det er noget vores nuværende kunder bruger aktivt.

Hvert trin i produktudviklingen der kan understøttes af præcis simulering i stedet for fysisk iteration, er tid du vinder og kapital du anvender mere effektivt.

---

## Trin 4 — LØSNING

FF Twin er en simulerings- og optimeringsplatform for UAV'er — fra droner og multirotorer til fixed-wing, VTOL og raketkøretøjer. Den er bygget til at operere på forretningsmål: du beskriver hvad du vil opnå, platformen beregner hvordan du kommer derhen.

Det der normalt kræver uger af konfigurationsarbejde i tunge simuleringsværktøjer — boundary conditions, mesh-strukturer, kalibreringsprocedurer for netop din drone — er kodet direkte ind i FF Twins workflow. Vi har brugt år på at vide præcis hvordan de aerodynamiske modeller skal sættes op, justeres og fortolkes for UAV-systemer. Den viden er tilgængelig for dig via platformen, fra dag ét.

Platformen følger dig fra den første idé til fuld operation:

*1. Design og optimering → 2. Komponent- og produktionsrådgivning → 3. Styring og kontrol → 4. Digital twin og vedligehold*

Du starter ikke forfra ved hvert trin. I de fleste virksomheder er design én gruppe mennesker, kontrol en anden og vedligehold en tredje — og de starter alle forfra. Med FF Twin er det den samme model der driver alle fire faser. Du bygger videre på et fundament der vokser med dig.

---

## Trin 5 — AUTORITET & TROVÆRDIGHED

FF Twin er bygget på PhD-niveau forskning inden for drone-aerodynamik og gjort tilgængeligt som en brugervenlig platform.

Finn Matras, PhD fra NTNU (Norges teknisk-naturvitenskapelige Universitet), er en award-winning forsker og specialist inden for dynamisk inflow-modellering for multirotor-systemer. Hans forskning er publiceret og peer-reviewed i *The Aeronautical Journal* (Cambridge University Press, 2025) og *Wind Energy Science* (Copernicus, 2025).

Platformens modeller er baseret på velkendte og accepterede fysiske ligninger. Det vi har gjort er at sætte dem præcist sammen til UAV-systemer, kalibreret dem til at fungere korrekt for de flyveregimer og geometrier der gælder for droner og VTOL-køretøjer, og pakket det ind i et system du kan bruge fra dag ét. Det er det arbejde vi har gjort — og som du ikke behøver at gøre selv.

*Troværdighed i praksis bygges løbende på kundereferencer. Se trin 7.*

---

## Trin 6 — FEATURES → FORDELE

**Du finder ud af præcis hvad der koster dig energi**

Din drone producerer ét samlet tal for energiforbrug. FF Twin dekomponerer det: vi beregner hvad de forskellige dele af dit system faktisk bidrager med, hvad der er veloptimeret og hvad der ikke er. Når vi kan se at ét område er langt fra optimalt, ved du præcist hvad du skal fokusere din næste investering på — og hvad der ikke er problemet. Den indsigt har du ikke i dag.

**Du erstatter fysiske prototype-iterationer med hurtige simuleringer**

En iteration i FF Twin tager sekunder til minutter. Optimeringsalgoritmen kører loopen selv og finder den bedste løsning automatisk. Virksomheder der udvikler uden præcis modellering bruger typisk mange fysiske iterationer på at nå et modent design. Med FF Twin kan mange af dem erstattes af simulation — og de der stadig skal bygges fysisk, bliver sat i gang på et langt bedre beregnet grundlag.

**Dine designbeslutninger understøttes af præcis beregning**

Det der tager uger at konfigurere i tunge simuleringsværktøjer, tager minutter i FF Twin. Systemet er specificeret til UAV-systemer — ikke til en generisk ingeniørworkflow.

**Du kan tilpasse dit drone-design per kundeordre**

Når dit grunddesign er modelleret, kan vi på minutter beregne en variant optimeret til en specifik kundes behov — anden cargo-vægt, anden mission, andet flyveregime. I stedet for én standarddrone du sælger til alle, har du en basisplatform du kan tilpasse per ordre til en brøkdel af hvad det ellers ville kræve. Det er en ny serviceydelse og et nyt konkurrencefortrin.

**Din investorcase bliver stærkere**

"Vores design er verificeret af specialiseret ekspertise" er et håndgribeligt argument i fundraising-samtaler. Det er ikke et argument du kan bruge, hvis du har itereret dig frem på mavefornemmelse. *(Dette argument modnes med konkrete kundecases — se trin 7.)*

**Træn kundens piloter inden dronen er leveret**

Fordi FF Twins model beskriver præcis hvordan din drone flyver, kan din slutkundes pilot begynde at træne i en simulator måneder før dronen er leveret. Dag 1 med den rigtige drone er allerede dag 300 i simulatoren. Det er en serviceydelse du kan tilbyde — og sælge — til dine kunder. *(Roadmap-feature: specificeres nærmere i kommende version.)*

**Du ved hvornår en komponent fejler — inden det sker**

Når din drone flyver i drift, sammenligner FF Twin løbende faktiske flyvedata med modellens forudsigelse. Afvigelser detekteres og diagnosticeres automatisk: hvilken komponent, hvad er forkert, og hvornår estimeres fejlen at blive kritisk. For en flåde er det forskellen på planlagt vedligehold og uventede nedbrud.

**Du har en AI-assistent der kender din drone**

Platformen inkluderer en specialiseret AI-agent med adgang til FF Twins modeller og metodikker. Du kan spare med den undervejs i dit design og optimeringsforløb — stille spørgsmål, afprøve hypoteser, forstå resultater — uden at det nødvendigvis kræver en konsulenttime. Det er som at have adgang til specialiseret fagviden løbende, ikke kun når du betaler for det.

**Fra idé til operation — ét system**

Design, simulering, optimering, komponentrådgivning, digital twin, pilottræning og vedligehold. Du skifter ikke platform efterhånden som du vokser. Et system, én model, ét datasæt der følger dig hele vejen.

---

## Trin 7 — SOCIAL PROOF

*[Under aktiv opbygning — udbygges løbende med dokumenterede resultater]*

**Nuværende proxy:**
FF Twin arbejder allerede med drone-virksomheder i Danmark og Norge. Én af dem bruger aktivt Finn Matras' involvering i deres investordialog som dokumentation for at deres design er verificeret og optimeret af specialiseret ekspertise. Forskningen bag platformen er peer-reviewed og anerkendt med priser.

*→ Glasvæg-modellen (vis konkrete resultater fra navngivne kunder) implementeres når 3–5 cases er dokumenterede. Ambition: efterår 2026.*

---

## Trin 8 — TILBUD

**Start her: En uforpligtende vurdering af dit drone-designs forbedringspotentiale**

Lav en simpel flyvetest — dronen flyver frem og tilbage ved 4–6 forskellige hastigheder. Det tager under en time. Send os logdataene.

Vi kigger på det og vender tilbage med vores vurdering: baseret på vores erfaring med tilsvarende designs tror vi dit forbedringspotentiale ligger i størrelsesordenen X%. Hvilke dele af systemet det drejer sig om, og præcis hvad der skal til — det kræver en fuld analyse.

Vil du vide det præcise svar, tager vi en snak om hvad en analyse indeholder, og hvad det koster.

**Byttehandlen:** Vi bruger jeres testdata til at validere og udbygge vores modeller. I får en kvalificeret vurdering baseret på specialiseret ekspertise. Ingen forpligtelse.

*Prissætning af fuld analyse: 5–10.000 DKK, svarende til hvad Finn allerede leverer manuelt i dag. Tilpasses i takt med at platformen og produktet modnes.*

---

## Trin 9 — CALL TO ACTION

> **"Lav en simpel flyvetest. Send os loggen. Vi sender dig en vurdering af hvad vi tror dit drone-design kan forbedres med — og på hvilke områder. Er du interesseret i det præcise svar, tager vi en snak."**

---

## Dokumentstatus

**Implementeret i v0.5 (fra gennemgang af v0.4):**
- [x] Hook omskrevet: 60%-hook fjernet som primær (for ukendt for bred ICP), ny hook fokuserer på "ved du hvad du skal ændre"
- [x] ICP konsolideret til én primær (v1→v2 og scratch er samme proces), to-VSL-noter bevaret
- [x] Problem: fjernet specifikke tidstall og iterationstal — "flere fysiske iterationer" er tilstrækkeligt
- [x] Problem: "det er i sig selv en bedrift"-sætning fjernet
- [x] Agitation: "penge du beholder"-sætning omskrevet til "kapital du anvender mere effektivt"
- [x] Agitation: konkurrenceframing ændret — kampen er in-house vs. FF Twin, ikke konkurrenter mod konkurrenter
- [x] Løsning: fjernet "du behøver ikke ansætte en aerospace PhD" (risiko for at støde ingeniører i målgruppen)
- [x] Løsning: Finn Matras' navn erstattet af "vi" i workflow-beskrivelsen
- [x] Løsning: 4 faser (tilføjet fase 2: Komponent- og produktionsrådgivning)
- [x] Autoritet: fjernet "real defensibility / svær at kopiere"-afsnittet — det er ikke et tillidsargument, det er et konkurrenceargument, og hører ikke her
- [x] Features: 3P-terminologi fjernet (Pi/Pr/Pa) — for teknisk til CEO/CTO-niveau; erstattet med lettilgængeligt sprog
- [x] Features: "kan ikke tilbyde uden FF Twin" → "til en brøkdel af hvad det ellers ville kræve"
- [x] Features: AI-assistent tilføjet som ny feature
- [x] Features: pilottræning markeret som roadmap-feature
- [x] Tilbud: sukkermodellen opdateret — giver nu forbedringsestimat, ikke 3P-analyse gratis

**Mangler stadig:**
- [ ] Konkrete kundehistorier til social proof (målsætning: efterår 2026)
- [ ] Glasvæg-variant ved 3–5 dokumenterede cases
- [ ] Separat VSL til ICP 2 (starter fra scratch)
- [ ] Tilpasning til kanal: video-script / landingsside / pitch-dokument
- [ ] Pilottræning-feature: bekræft scope og tidspunkt (fase 2 roadmap?)
- [ ] AI-assistent: bekræft hvad der faktisk er/er planlagt i platformen
- [ ] Bekræft om investorargumentet er korrekt formuleret i forhold til nuværende kunder
