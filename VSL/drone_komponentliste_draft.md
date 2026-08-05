# Drone Komponentliste — Optimeringsmuligheder
**DRAFT — opdateret efter review fra Finn Matras, april 2026**

---

## Formål
Dette dokument er råmateriale til salgspitch og den visuelle drone-platform. Det kortlægger alle relevante komponenter i et multirotor-system og beskriver hvad der kan optimeres — og hvad konsekvensen er af *ikke* at optimere det.

Strukturen følger dronen fra energikilde til mission og er opdelt i seks kategorier.

---

## Kategori 1: Propulsion — Propeller & Rotor

### 1.1 Propellerstørrelse og -form
**Hvad det er:** Bladenes geometri, længde, kordeprofil og twist.
**Typisk problem:** Valgt ud fra tommelfingerregel eller leverandøranbefaling, ikke ud fra den specifikke missions krav.
**Hvad kan optimeres:** Bladform, pitch-distribution og størrelse kan optimeres til det specifikke vægt/mission/hastigheds-scenarie. Forkert valg her giver direkte tab i induced power (Pi) — den største energipost.

### 1.2 Propellerplacering og -antal
**Hvad det er:** Afstanden mellem rotorer, layout (kvadrat, hexagon, o.a.) og antal propellere.
**Typisk problem:** Layout besluttes tidligt ud fra strukturelle hensyn, uden forståelse for aerodynamiske interaktioner.
**Hvad kan optimeres:** Optimal placering minimerer rotor-rotor-interaktioner, som kan udgøre 10–70% effektivitetstab. Finn's forskning viser at disse interaktioner er kritiske og i dag ignoreres af langt de fleste.

### 1.3 Rotationsretning
**Hvad det er:** Hvilke propellere drejer med/mod uret (CW/CCW).
**Typisk problem:** Sættes som default, sjældent analyseret for torque- og interaktionseffekter.
**Hvad kan optimeres:** Korrekt kombination reducerer uønskede moment-bidrag og forbedrer stabilitet.

### 1.4 Rotor-rotor aerodynamiske interaktioner
**Hvad det er:** Luftstrøm fra én rotor der påvirker naborotorernes inflow.
**Typisk problem:** Ignoreres systematisk af ~80% af industrien. Kontrolsystemet kompenserer, så fejlen er usynlig for operatøren — men energitabet er reelt.
**Hvad kan optimeres:** Korrekt modellering af interaktioner er Finn's kernebidrag. Kan kvantificere og minimere interaktionstab som ellers er skjulte.

---

## Kategori 2: Drivlinje — Motor, ESC, Batteri

### 2.1 Motor
**Hvad det er:** KV-rating, effektivitetskurve, termisk kapacitet.
**Typisk problem:** Vælges *efter* propelleren — eller endnu værre, propelleren vælges til at matche en allerede købt motor. Den korrekte rækkefølge er: propeller → motor → batteri → controller.
**Hvad kan optimeres:** Motor-propeller-match ved den specifikke operationshastighed. En forkert matchet motor spilder energi som varme.

### 2.2 ESC / Speed Controller
**Hvad det er:** Elektronisk hastighedsregulator — konverterer batsignal til motorstyring.
**Typisk problem:** Sjældent analyseret som en del af det samlede energisystem.
**Hvad kan optimeres:** Effektivitetstab i ESC under teillast vs. fuld last kan kvantificeres og indgå i samlet systemoptimering.

### 2.3 Batteri
**Hvad det er:** Kapacitet (mAh), C-rating, indre modstand, vægt.
**Typisk problem:** Dimensioneres ofte ud fra "mere er bedre" — men ekstra vægt koster mere end det giver i rækkevidde.
**Hvad kan optimeres:** Optimal batteristørrelse for en given mission. Afvejning af kapacitet vs. vægttillæg er et optimeringsproblem der kræver korrekt inflow-model for at løse præcist.

---

## Kategori 3: Airframe / Fuselage

### 3.1 Fuselage-geometri og aerodynamisk modstand
**Hvad det er:** Kroppens form og det parasitiske luftmodstandsbidrag (Pa — Parasitic power).
**Typisk problem:** Beregnes sjældent ved design. Antages konstant eller ubetydelig.
**Hvad kan optimeres:** Fuselage-airloads kan parametriseres og indgå i samlet power-budget. Vigtigere ved forward-flight profiler (leveringsdrones, inspektion).

### 3.2 Vægtfordeling og tyngdepunkt
**Hvad det er:** Hvor massen er placeret i forhold til rotorernes løftpunkt.
**Typisk problem:** Tyngdepunktsforskydning ved payload skaber skæve kraftfordelinger og ineffektiv hover.
**Hvad kan optimeres:** Analyse af statisk og dynamisk balance som en del af designoptimeringen.

### 3.3 Strukturel mekanik
**Hvad det er:** Arme, beslag, landingsgear — stivhed og svingningsfrekvenser.
**Typisk problem:** Resonansfrekvenser beregnes ikke og opdages først ved test (eller havari).
**Hvad kan optimeres:** Strukturanalyse der kobler mekanisk og aerodynamisk modellering.

---

## Kategori 4: Flydynamik & Styring

### 4.1 Inflow-dynamik (per rotor)
**Hvad det er:** Hvordan luftstrømmen ind mod rotoren opfører sig dynamisk — ikke blot i steady-state.
**Typisk problem:** De fleste modeller antager stationær inflow. Det er kun korrekt for helt isolerede, stationære rotorer under specifikke betingelser.
**Hvad kan optimeres:** Finn's dynamiske inflow-model (publiceret i The Aeronautical Journal 2025) er det eneste kendte peer-reviewede værktøj der modellerer dette korrekt for multirotor-systemer.

### 4.2 Kontrolsystem / Autopilot
**Hvad det er:** PID-loops, feed-forward, tilstandsestimator (EKF), waypoint-navigation.
**Typisk problem:** Kontrolsystemet kompenserer for aerodynamiske inefficienser — og gør dem dermed usynlige. Man ser et stabilt fly, ikke det underliggende energitab.
**Hvad kan optimeres:** Optimal controller-tuning kan kun ske med korrekt underliggende model. Forkert inflow-model = suboptimal controller.

### 4.3 Stabilitet og passivitet
**Hvad det er:** Om systemet er stabilt uden aktiv kontrol, og under hvilke betingelser.
**Typisk problem:** Analyseres typisk ikke analytisk — kun empirisk ved test.
**Hvad kan optimeres:** Analytisk stabilitetsanalyse som del af designprocessen.

---

## Kategori 5: Mission & Miljø

### 5.1 Flyveprofil
**Hvad det er:** Kombination af hover-tid, forward-flight hastighed, højde og payload.
**Typisk problem:** Energibudget beregnes som "hover-ækvivalent" — men forward flight ved optimal hastighed (~8 m/s) kan give op til 13% bedre flyvetid.
**Hvad kan optimeres:** Missionsprofil-optimering: hvornår skal dronen flyve hurtigt vs. langsomt, og hvilken hastighed er energioptimal for den specifikke konfiguration.

### 5.2 Vindpåvirkning og turbulens
**Hvad det er:** Ekstern vindbelastning og dens effekt på inflow og styring.
**Typisk problem:** Modelleres sjældent — dronen testes i godt vejr og forventes at klare resten via kontrolsystemet.
**Hvad kan optimeres:** Vindmodellering i simulator giver realistisk performance-estimat under operationelle forhold.

### 5.3 Payload og lastprofil
**Hvad det er:** Vægt og placering af nyttelast, inkl. variabel last (leveringsdrone der slipper pakken).
**Hvad kan optimeres:** Dynamisk ændring i tyngdepunkt og vægtniveau som funktion af mission-fase.

---

## Kategori 6: Akustik & Signatur

### 6.1 Akustisk støjprofil
**Hvad det er:** Det støjniveau dronen producerer under drift — primært genereret af propellerblades passage gennem luft, tipsvirvel, og rotor-rotor-interaktioner.
**Typisk problem:** Støj optimeres sjældent proaktivt. De fleste teams tester støjniveau som en egenskab *efter* design er fastlagt — ikke som en designparameter fra start. Civile operatører møder støjkrav i regulativer (BVLOS-tilladelser, urban air mobility), og militære brugere ønsker minimal akustisk signatur for ikke at afsløre position.
**Hvad kan optimeres:** Bladantal, bladgeometri og RPM-punkt har stor indflydelse på støjprofilen. Rotor-rotor-interaktioner kan skabe periodiske støjtoner (blade passing frequency) der forværrer den samlede signatur. Med korrekt modellering kan støjprofilen indgå som et optimeringskriterium fra designfasen.
**Relevant for:** Civile operationer (bymissioner, inspektion, levering) og militære anvendelser.

### 6.2 Radar-signatur (RCS)
**Hvad det er:** Dronens Radar Cross Section — hvor synlig den er for radarbaserede detektionssystemer.
**Typisk problem:** Ikke relevant for civile brugere, men afgørende i militær og forsvarssammenhæng. Form, materialer og rotorbevægelse påvirker RCS.
**Hvad kan optimeres:** Geometrisk udformning og placering af rotorer i forhold til forventet detektionsvinkel. Kan indgå som parameter i platform-designoptimering.
**Relevant for:** Militære og forsvarsrelaterede anvendelser.

---

## Overblik: Energibudgettet
Samlet forbrug i en multirotor kan dekomponeres i tre bidrag:

| Komponent | Betegnelse | Typisk andel | Optimeringspotentiale |
|-----------|-----------|-------------|----------------------|
| Induced power (rotor-inflow) | Pi | ~60% | Højt — Finn's kerneekspertise |
| Profile power (bladmodstand) | Pr | ~20–30% | Moderat — propellergeometri |
| Parasitic power (fuselage/luft) | Pa | ~10–20% | Stigende ved forward flight |

*Pi er det største og mindst forståede bidrag — og det eneste som korrekt modellering af dynamisk inflow og rotor-interaktioner kan adressere fuldt ud.*

---

## Noter til videre bearbejdning
- [x] Finn har reviewet listen — lyd/støj bekræftet som relevant for både civile og militære, radar-signatur bekræftet som militær parameter
- [ ] Prioritering: hvilke komponenter er mest relevante for v1-pitch vs. v2+?
- [ ] Koble hver komponent til konkret "hvad kan FF Twin beregne/optimere her?" (platform-version for version)
- [ ] Beslutte visuel repræsentation: 2D/3D drone-diagram med klikbare zoner
- [ ] Afklare: er der yderligere komponenter Finn vil tilføje?

