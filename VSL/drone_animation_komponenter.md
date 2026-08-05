# FF Twin — Drone Komponentindhold til Animation
**Indhold til eksplosionsvisning af drone — udfordringer og FF Twin-løsninger per komponent**
*Version 1.0 — juni 2026*

---

## Koncept

En drone vises samlet. Animation opdeler den i alle enkeltdele. Klik på en del → se udfordring og FF Twin-løsning. Klik på samlet drone → se det samlede billede.

Dronen er bygget op af disse synlige komponenter:
1. Propeller (blade)
2. Motor
3. Arm / boom
4. Dronekrop / frame
5. Batteri
6. ESC (Electronic Speed Controller)
7. Flight Controller (hjerne)
8. Payload / cargo

Plus ét usynligt "system-lag":
- Aerodynamiske interaktioner (propel-til-propel inflow)

---

## KOMPONENT 1 — Propeller

**Hvad den gør:**
Omdanner motorens rotation til løftekraft ved at accelerere luft nedad. ~60% af dronens samlede energiforbrug sker her.

---

**Udfordringen uden FF Twin:**

De fleste vælger propeller ud fra standard specifikationer — størrelse og stigning — og antager at en større propel giver mere kraft. Det passer, men det er kun halvdelen af historien.

Det, der ikke fremgår af databladet: propellens geometri (angle of attack langs hele bladet) er designet til ét specifikt luftindstrømningsmønster. Hvis den faktiske inflow er anderledes — fordi en nærliggende propel ændrer luften, fordi dronen flyver fremad i stedet for at stå stille — arbejder propellen med en forkert angle of attack. Den laver stadig kraft, men ineffektivt.

Kontrolsystemet kompenserer automatisk. Dronen flyver. Designfejlen forbliver usynlig.

Herudover: en propel der sidder direkte over eller under en anden (coaxial design) vil se en fundamentalt anderledes inflow end en, der sidder alene. De to propeller har brug for forskellig geometri — men de fleste bruger identiske blade på begge.

**Størrelse og rotationshastighed:**
Langsomt roterende, stor propel er mest effektivt. Men hvis dronen er for stor, blokerer kroppen for luftindstrømningen under propellen — så fungerer den centrale del af bladet ikke. Optimal størrelse er ikke "størst mulig" men "størst mulig uden at oversætte dronekroppen."

---

**FF Twin løsning:**

FF Twin beregner den faktiske inflow-hastighed og retning som propellen vil opleve — i hover, ved fremadflyvning, med nabopropellers indflydelse. Ud fra det beregnes den optimale blade-geometri specifikt for den drone og den mission.

For coaxial designs beregnes to separate geometrier — én til den øverste propel, én til den nedre — så begge arbejder optimalt i det indstrømningsmønster, de faktisk ser.

Resultatet: du vælger ikke propel ud fra katalog. Du beregner den rigtige propel til netop din drone.

---

## KOMPONENT 2 — Motor

**Hvad den gør:**
Omdanner elektrisk energi til mekanisk rotation. Skal matche propellens krav til drejemoment og RPM nøjagtigt — ellers arbejder den udenfor sin effektivitetskurve.

---

**Udfordringen uden FF Twin:**

En motor har en effektivitetskurve: den er effektiv ved visse kombinationer af drejemoment og rotationshastighed — og ineffektiv ved andre. Forskel kan være 20-30% i effektivitet.

Typisk vælger man en motor man tror passer, og finder så den bedste propel til den motor. Men fordi motoren var det forkerte valg fra starten, ender man med en propel der passer til den kraft man vil have — men ikke til den specifikke motor man valgte. Man mister energi i koblingen.

Motorer til droner produceres næsten udelukkende i Kina. Der er ingen europæisk producent der matcher kvaliteten endnu. De fleste vælger standard hyldevarer og håber på det bedste.

---

**FF Twin løsning:**

FF Twin beregner de nødvendige drejemoment- og RPM-krav som motoren skal levere, givet den valgte propel og det forventede flyveregime. Det giver et præcist kravspecifikation til motorvalget — og gør det muligt at evaluere om en given motor faktisk arbejder inden for sin effektive zone for netop det design.

---

## KOMPONENT 3 — Arm / Boom

**Hvad den gør:**
Forbinder motor og propel til dronens centrale krop. Holder dem i korrekt position. Bærer last, vibrationer og aerodynamiske kræfter.

---

**Udfordringen uden FF Twin:**

Armen ser simpel ud — en stang der stikker ud. Men den er udsat for konstante op-og-ned kræfter: propellerne trækker op, dronens vægt trækker ned, turbulens presser i alle retninger. Over tid akkumulerer disse kræfter materialetræthed — armen slides op, og der er ingen der ved hvornår den bryder.

Armens form er næsten altid rund eller firkantet. Men en arm der stikker ud i luftstrømmen fungerer aerodynamisk som en vinge — bare en meget dårlig en. En rund arm skaber unødvendig luftmodstand og løfter ikke. En arm formet som et vingeprofil ville reducere luftmodstanden og potentielt bidrage til løft.

Materialevalget (stål, aluminium, glasfiber, karbonfiber) påvirker både armens vægt, stivhed og levetid — men de færreste beregner hvad det rigtige materiale er. Tunge arme øger dronens totalvægt og reducerer batteritid.

---

**FF Twin løsning:**

FF Twin beregner de faktiske kræfter armen er udsat for under normal drift og worst case. Ud fra det bestemmes: nødvendig stivhed og styrke, optimalt materiale (karbonfiber vs. glasfiber vs. aluminium), minimal vægt der stadig klarer belastningen, og estimeret levetid i flyvetimer.

Armens aerodynamiske profil kan optimeres til den luftstrøm den faktisk oplever — baseret på beregnet inflow fra propellerne over.

Det er den samme tilgang som bruges på vindturbineblade: præcis beregning af "damage equivalent load" for at vide hvornår komponenten skal udskiftes.

---

## KOMPONENT 4 — Dronekrop / Frame

**Hvad den gør:**
Bærer alt: batteri, elektronik, cargo, sensorer. Er udgangspunktet for dronens aerodynamiske profil under flyvning.

---

**Udfordringen uden FF Twin:**

En standard dronekrop er en boks — praktisk til at montere dele på, men aerodynamisk katastrofal under fremadflyvning.

Når dronen flyver fremad tiltes den 10-20 grader forover. Nu rammer vinden dronekroppens flade underflade. Det giver ikke bare luftmodstand — det giver en nedadgående kraft. Dronen skal altså bruge ekstra energi på at bekæmpe en kraft, som dens eget design skaber.

Den modsatte løsning — at forme kroppen som et bærende profil der skaber løft når den tiltes — findes næsten ikke i kommercielle droner. Alle kopierer det samme box-design, fordi det er nemt at producere. Ingen har beregnet hvad det koster dem i energi.

Kroppen er heller aldrig designet til at arbejde med propellernes inflow. Hvis kroppen blokerer for luftindstrømninen under en propel, fungerer den centrale del af propelbladet ikke.

---

**FF Twin løsning:**

FF Twin beregner de aerodynamiske kræfter på dronekroppen som funktion af flyvevinkel og hastighed — og viser præcist hvad det koster i energi at flyve med en given kropsform. Det giver et konkret grundlag for at vurdere om en redesignet krop vil give en målbar gevinst.

For kunden: du ved ikke hvad din kropsform koster dig. Vi kan beregne det — og estimere forbedringspotentialet.

---

## KOMPONENT 5 — Batteri

**Hvad den gør:**
Lagrer energi. Er typisk den tungeste enkeltkomponent på dronen. Placering og størrelse påvirker både flyvetid og hvilke motorer der arbejder hårdest.

---

**Udfordringen uden FF Twin:**

De fleste placerer batteriet i midten af dronen fordi det er symmetrisk og praktisk. Men "symmetrisk" er ikke det samme som "optimalt."

Når dronen flyver fremad er den forreste propel mere effektiv end den bageste (fordi den forreste ikke bliver forstyrret af udstrøm fra andre propeller). Hvis batteriet — der er tungest — flyttes fremad, skal den forreste, mere effektive motor bære mere af lasten. Samlet bruger dronen mindre energi.

Omvendt gælder det for cargo: afhængig af om payload er tung eller let, er der en optimal cargo-placering der maksimerer effektiviteten præcis i det flyveregime, der tæller.

Online-beregningsværktøjer til batteristørrelse ignorerer disse effekter. De regner bare med total P. De giver et forkert estimat af flyvetid.

**Avanceret design:** De bedste droner placerer et batteri direkte under hver motor, så kabelstrækning minimeres. Kortere kabler = lavere modstand = lavere tab = lettere system. Det har de færreste tænkt på.

---

**FF Twin løsning:**

FF Twin beregner optimal batteriplacement for en given mission: fordeling af løftekraft på tværs af propeller, energiforbrug per motor, og samlet systemeffektivitet som funktion af batteriens position.

For cargo-droner beregnes optimal placering for fuldt lastet vs. tom retur-flyvning — separat, fordi optimal placering kan være forskellig.

Batteristørrelse beregnes ud fra faktisk modelleret energiforbrug — ikke tommelfingerregler.

---

## KOMPONENT 6 — ESC (Electronic Speed Controller)

**Hvad den gør:**
Tager strøm fra batteriet og omsætter den til den præcise strøm motoren skal have. En ESC per motor. Matcher batteriets DC til motorens krav.

---

**Udfordringen uden FF Twin:**

ESC skal matche motor og batteri nøjagtigt. Forkert kobling koster 5-10% i effektivitet. De fleste vælger ESC efter det der passer til motorens nominelle strøm — men kigger ikke på om den opererer i sin optimale zone for de faktiske belastninger dronen oplever i brug.

---

**FF Twin løsning:**

FF Twin definerer de faktiske strøm- og spændingskrav per motor for dronens forventede flyveregime. Det giver et præcist grundlag for ESC-valg — og kan vise om den valgte ESC arbejder inden for sin effektive zone eller ej.

---

## KOMPONENT 7 — Flight Controller / Styringshjernen

**Hvad den gør:**
Modtager kommandoer (fra pilot eller mission planner), beregner hvad hver motor skal gøre, og sender signaler til ESC'erne. Indeholder kontrolalgoritmer i et hierarki: mission → hastighed → acceleration → attitude → motorkommando.

---

**Udfordringen uden FF Twin:**

Styringsalgoritmerne kalibreres iterativt ved fysiske flyvetests. Man installerer et kontrolsystem der synes rigtigt, flyver dronen, observerer hvad der sker, justerer koefficienter, flyver igen. Det tager dage til uger — for hvert nyt design eller ny konfiguration.

Pilottræning kræver en fysisk drone. Kunden der køber dronen kan ikke begynde at træne sin pilot, før dronen er leveret.

Den optimale flyvealgoritme til en given mission (hvad er den mest energieffektive flyvevej, hvornår skal dronen svinge ud for at udnytte vinden, hvad er optimal hastighed) er aldrig beregnet. Piloten flyver på erfaring. Den autonome algoritme er kalibreret til "flyver uden at styrte" — ikke til "flyver optimalt."

---

**FF Twin løsning:**

Fordi FF Twin har en præcis digital model af dronen, kan kontrolalgoritmerne kalibreres og optimeres digitalt — uden en eneste fysisk flyvning. Iterationen tager sekunder i stedet for dage.

Det muliggør to ting som ikke er mulige i dag:

**Pilottræning før dronen eksisterer:** Kunden kan træne sin pilot på en simulator der opfører sig præcist som den faktiske drone — allerede måneder før levering. Dag 1 med den rigtige drone er allerede dag 300 i simulatoren.

**Optimal mission planning:** FF Twin kan beregne den mest energieffektive flyvevej for en given mission — inkl. udnyttelse af vindforhold, optimal højde, optimal hastighed. Det er ikke noget nogen pilot kan intuitivt beregne.

---

## KOMPONENT 8 — Payload / Cargo

**Hvad den gør:**
Det dronen skal transportere eller bære: pakker, kameraer, sensorer, medicin, sten, industri-udstyr.

---

**Udfordringen uden FF Twin:**

Payload-placering behandles som et praktisk problem: hvor er der plads? Men placering påvirker direkte hvilke motorer der bærer lasten — og dermed om dronen er effektiv eller ej under arbejdslast.

En tung cargo foran og et let batteri bag = én konfiguration. En tung cargo bag = en anden. Det optimale afhænger af cargotypen.

De fleste laver én standarddrone og sælger den til alle kunder med alle typer cargo. De beregner aldrig om cargo-placeringen er optimal for kundens specifikke mission.

---

**FF Twin løsning:**

FF Twin beregner optimal cargo-placering som funktion af cargo-vægt og flyveregime. For kunder der flyver med varierende cargo kan vi beregne optimal konfiguration for de hyppigste brug-cases.

**Den undervurderede fordel — custom drone per kundeordre:**
Når grunddesignet er modelleret, kan vi på minutter beregne en variant optimeret til en specifik kundes behov. Ikke én standarddrone til alle — men en basisplatform der tilpasses per ordre med de rette aerodynamiske specifikationer til kundens specifikke mission og cargo-profil.

---

## SYSTEM-LAG — Aerodynamiske Interaktioner

**Hvad det er:**
Propellerne på en multirotor-drone påvirker hinandens luftindstrømning. Det er ikke synligt på nogen enkelt komponent — men er årsag til 10-70% effektivitetstab som ingen andre beregner.

---

**Udfordringen uden FF Twin:**

~80% af drone-udviklere antager at propellerne er uafhængige. De beregner dem enkeltvis.

Det er forkert. Propellerne "stjæler" luft fra hinanden. En propel der sidder bag en anden ser ikke ren luft — den ser udstrøm fra den forreste, der allerede er accelereret og komprimeret. Den bageste propel skal arbejde hårdere for samme kraft.

Når dronen flyver fremad ændrer dette interaktionsmønster sig. Nogle interaktioner der er negative i hover er positive under fremadflyvning. Det er komplekst, ikke-lineært, og umuligt at se fra fysiske tests — fordi kontrolsystemet altid kompenserer automatisk.

---

**FF Twin løsning:**

Inflow-modellen er Finn Matras' kerneforskning — dynamisk inflow-modellering for multirotor-systemer, publiceret i The Aeronautical Journal (2025) og Wind Energy Science (2025), award-winning forskning.

FF Twin beregner præcist hvordan propellerne påvirker hinandens indstrømningsmønster — i alle flyvetilstande. Det giver designanbefalinger om:
- Optimal afstand og placering mellem propeller
- Rotationsretning per propel (medurs/modurs)
- Armgeometri der minimerer negativ interferens
- Propelgeometri tilpasset den inflow de faktisk ser

---

## SAMLET DRONE — Udfordring og løsning

**Udfordringen i dag (samlet billede):**

En drone-startup bruger 3 måneder på at bygge en prototype. Derefter 3-6 måneder på at debugge og flyve tests. Analysen af data fra flyvetests tager yderligere måneder — og selv da er analysen begrænset, fordi de kun kan måle total effektforbrug (P), ikke de tre underkomponenter (Pi, Pr, Pa) der fortæller hvad der faktisk sker.

Næste designbeslutning tages på mavefornemmelse og trial-and-error. En ny prototype bygges. Loopen starter forfra.

5-6 iterationer = 2-3 år og millioner i kapital spildt på at opdage det, vi kan beregne på dage.

**FF Twin løsning (samlet billede):**

Du beskriver dit mål. FF Twin's model (Mechanics + Air Loads + Inflow) beregner hvad der sker med din drone i alle flyvetilstande. Simulatoren itererer i sekunder. Optimeringsalgoritmen finder den bedste løsning automatisk.

Output er Pi, Pr og Pa separat — ikke bare total P. Du ser præcist hvor energien forsvinder og hvad du skal investere i.

Fra design til digital drone: en session. Fra digital drone til optimeret design: minutter per iteration.

Og modellen du bygger i designfasen er den samme, der bruges til at kalibrere styringssystemet, træne piloten og overvåge dronen i drift. Du bygger én gang — og høster værdi i hele dronens levetid.

---

## Tre faser — platformens levetidsværdi

**Fase 1 — Design og optimering (grøn)**
Én gang. Sættes op med dronens specifikationer og mål.
Resultater: optimeret design, verificeret performance, præcis komponentliste.
Tidsforbrug med FF Twin: dage. Uden: måneder.

**Fase 2 — Styring og kontrol (blå)**
Løbende. Kontrolalgoritmer kalibreres digitalt. Pilottræning i simulator. Mission planning optimeret for energi og vejr.
Resultater: optimal autonomi, trænede piloter fra dag 1, bedste flyvevej beregnet automatisk.

**Fase 3 — Digital twin og vedligehold (rød)**
Løbende. Faktiske flyvedata sammenlignes med model. Afvigelser detekteres og diagnosticeres automatisk. Vedligehold planlægges prædiktivt.
Resultater: ved præcist hvornår en komponent fejler inden det sker. Ingen uventede nedbrud. Fleet management for 500+ droner.

---

*Dokumentstatus: v1.0 — baseret på deep dive sessions med Finn Matras, juni 2026*
*Bruges som indholdskilde til drone-animations-eksploderings-visning og VSL*
