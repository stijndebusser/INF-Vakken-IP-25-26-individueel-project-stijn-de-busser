# Literatuurstudie

## Verduidelijking
De geselecteerde literatuur behandelt verschillende aspecten van robotprogrammering en -bediening die raakvlakken hebben met de kerncomponenten uit de probleemstelling: traject-voorspelling, collision awareness, en spatial awareness.

De artikelen variëren in aanpak, van AR-visualisatie voor motion intent tot autonome collision avoidance systemen, en adresseren elk één of meerdere kerncomponenten op verschillende manieren. _Sommige artikelen sluiten nauw aan bij de probleemstelling door expliciet te focussen op visualisatie voor operators, terwijl andere primair technische oplossingen bieden zonder visuele feedback._ Deze verscheidenheid helpt zowel bestaande visualisatie-methoden als gaps in operator awareness te identificeren en onduidelijkheden en pijnpunten te omschrijven.

De gevonden literatuur wordt hieronder samengevat en besproken.

---
## Literatuurlijst

### 1. Interactive robot trajectory planning and simulation using Augmented Reality

**Auteurs:** H.C. Fang, S.K Ong, A.Y.C. Nee  
**Jaar:** 2011  
**Link:** https://www.sciencedirect.com/science/article/abs/pii/S0736584511001116

| Bevindingen | Problemen/Gaps | Kerncomponent(en) |
| ----------- | -------------- | ----------------- |
| RPAR-II combineert AR-simulatie met robot dynamica en time-optimal trajectory optimization; pre-validatie van trajecten inclusief overshoot detectie; visuele evaluatie en tuning van controller-parameters | Bestaande AR-methoden negeren dynamische beperkingen (velocity, acceleration); VR vereist complete a priori kennis; PbD produceert suboptimale/jittery paden; teaching pendant programmering onintuïtief | Traject-voorspelling, spatial awareness |

**Feedforward aspect**: RPAR-II biedt feedforward door trajecten te pre-valideren en simuleren **voordat** deze uitgevoerd worden. Operators kunnen dynamische aspecten (overshoot, snelheid, acceleratie) vooraf evalueren en parameters aanpassen vóór fysieke uitvoering.

### Onduidelijkheden & gaps

**Visualisatie**: Hoewel traject-voorspelling in AR wordt aangehaald, is niet duidelijk hoe dit wordt gevisualiseerd: animatie? ghost-trail? snelheids-/acceleratie-indicatoren? Hoe wordt overshoot getoond? Is dit real-time of pre-calculated?

**Collision awareness**: Collision detection met omgevingselementen wordt niet expliciet behandeld. Onduidelijk of simulatie enkel de robot betreft, of ook interactie met werkstukken/tooling/obstakels. Geen collision zone visualisatie of proximity warnings vermeld. Risico: Dynamisch traject kan toch leiden tot botsingen.

**Dynamische omgevingen**: Onduidelijk hoe real-time veranderingen in werkruimte worden verwerkt. Geen info over tracking-robuustheid in variabele industriële condities en dus mogelijk beperkt tot statische setups.

---

### 2. Robot programming using augmented reality: An interactive method for planning collision-free paths

**Auteurs:** J.W.S. Chong, S.K. Ong, A.Y.C. Nee, K. Youcef-Youmi  
**Jaar:** 2008  
**Link:** https://www.sciencedirect.com/science/article/pii/S0736584508000665

| Bevindingen | Problemen/Gaps | Kerncomponent(en) |
| ----------- | -------------- | ----------------- |
| AR + heuristic beam search voor n-DOF collision-free paths; mens definieert CFV en start/goal; geen C-space constructie; single demonstration; volledige manipulator collision check | VR duur/complex; offline programmering onintuïtief; PbD meerdere demonstraties nodig, suboptimaal, beperkt tot 2D/3D, enkel end-effector collisions | Spatial awareness, collision awareness |

**Feedforward aspect**: Systeem biedt feedforward door collision-free pad te berekenen en tonen **voordat** robot beweegt. Operator definieert collision-free volumes (CFV) en kan pad evalueren alvorens uitvoering. Focus op planning-fase, het systeem toont geen feedforward tijdens uitvoering zelf.

### Onduidelijkheden & gaps

**Visualisatie**: Onduidelijk hoe CFV wordt gevisualiseerd (wireframe? transparant volume?), hoe beam search paden worden getoond, of er real-time feedback is tijdens CFV-definitie.

**Traject-voorspelling**: Onduidelijk hoe dit pad via de beam search gevisualiseerd wordt.

---

### 3. Mind the ARm: realtime visualization of robot motion intent in head-mounted augmented reality

**Auteurs:** Uwe Gruenefeld, Lars Prädel, Jannike Illing, Tim Stratmann, Sandra Drolshagen, Max Pfingsthorn  
**Jaar:** 2020  
**Link:** https://dl.acm.org/doi/abs/10.1145/3404983.3405509  
**PDF:** https://uwe-gruenefeld.de/pub/mindthearm-paper.pdf

| Bevindingen | Problemen/Gaps | Kerncomponent(en) |
| ----------- | -------------- | ----------------- |
| 3 AR-visualisaties vergeleken voor robot motion intent: Path (end-effector pad), Preview (complete robot configuratie), Volume (occupied space als 2D circle projection). User study met cognitive load task (math equations) tijdens robot avoidance. Bevindingen: Volume vereist kortste head rotation, hoogste perceived safety, laat dichtste proximity toe zonder shutdown. Path & Preview vereisten significant langere hoofd rotaties. Zoals besproken zijn de head rotation, proximity en robot shutdowns hoofdmetingen in dit geval. Ook subjectieve metingen waren in acht genomen. Head-mounted AR device gebruikt. | Reactive safety → productiviteitsverlies; geen proactieve motion intent communicatie; onduidelijk welke visualisatie werkt best | Collision awareness, spatial awareness |

**Feedforward aspect**: Visualiseert motion intent in real-time door toekomstige robot-positie te projecteren. Path toont waar end-effector naartoe gaat, Preview toont volledige toekomstige robot-configuratie, Volume toont ruimte die robot zal innemen. Feedforward tijdens uitvoering (niet planning-fase).

### Onduidelijkheden & gaps

**Traject-voorspelling**: Toont toekomstige robot positie enkel voor nabije toekomst en niet het volledige pad. Ook geen bewegingsdynamica (snelheid, acceleratie).

---

### 4. On-line collision avoidance for collaborative robot manipulators by adjusting off-line generated paths: An industrial use case

**Auteurs:** Mohammad Safeea, Pedro Neto, Richard Bearee  
**Jaar:** 2019  
**Link:** https://www.sciencedirect.com/science/article/pii/S0921889019300648  

| Bevindingen                                                                                                                                                                                                                                                       | Problemen/Gaps                                                                                                                  | Kerncomponent(en)                      |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------- |
| Robot collision avoidance door het definiëren van geometrische capsules voor representatie van beide mens als robot; houdt de robot bezig met operaties zonder de taak te doen ontbreken; bij plotse beweging zal de robot repulsion-vector-reshaping toepassen om geen abrupte beweging of schokken te maken; traject van de arm kan dus live aangepast worden. Context van industrieel speelveld gebruikt en goed ontvangen door menselijke medewerkers. | Bevat geen spatial awareness of traject-voorspelling en beide ontbreken visueel; enige fallback is het stoppen of vertragen van de machine. | Collision awareness |

### Onduidelijkheden & gaps

**Traject-voorspelling**, **Spatial awareness**: Dit artikel bevat geen concrete manier van visualisatie of ruimtelijk overzicht. De fallback voor complicaties zoals beschreven in de probleemstelling is dat deze machine goede collisie-avoidance bevat. Hoewel dit een pluspunt is, kan via mijn probleembeschrijving ook collision awareness onder onduidelijkheden geplaatst worden omdat dit niet visueel ondersteund wordt. De operator heeft geen AR omgeving en de machine handelt intern zonder enige communicatie.

**Feedforward aspect**: Geen feedforward - systeem reageert reactief op menselijke aanwezigheid zonder vooraf te visualiseren wat de aangepaste beweging zal zijn. Operator ontvangt geen voorspellende informatie over toekomstige robot-acties.

---

### 5. Development and Implementation of a Collaborative Workspace for Industrial Robots Utilizing a Practical Path Adaptation Algorithm and Augmented Reality

**Auteurs:** Serhat Demirtas, Tolga Cankurt, Evren Samur  
**Jaar:** 2022  
**Link:** https://www.sciencedirect.com/science/article/pii/S0957415822000204

| Bevindingen                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Problemen/Gaps                                                                                                                                                                                                                                                                                                                                | Kerncomponent(en)   |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- |
| Conventional robots vereisen fences voor veiligheid → grote ruimte, beperkte HRC, productie delays bij human entry. Cobots lossen dit op maar zijn kostbaar en beperkt beschikbaar. Behoefte aan praktische oplossing die bestaande conventional robots collaborative features geeft zonder dure nieuwe aankopen of controller modifications. Path adaptation algorithm past robot pad aan bij menselijke interventie (slowdown, avoidance, full stop op basis van minimum distance). AR-based warning system (projector + HMD) voor operator warnings/info. Safety laser scanner voor human detection. Palletizing test bij HKTM Inc. production site. User study (16 subjects): AR verbetert perceived safety/collaboration, maar negatieve impact op physical comfort. Algoritme als custom movement function implementeerbaar zonder robot controller wijzigingen. | Fences occuperen grote ruimte en beperken HRC; robot stop bij human entry → significant delays in production cycle; conventional industrial robots missen collaborative features (in tegenstelling tot cobots); cobots duur en beperkt beschikbaar; behoefte aan oplossing voor bestaande conventional robots zonder controller modifications | Collision awareness, traject voorspelling |

### Onduidelijkheden & gaps

**Traject-voorspelling**, **Spatial awareness**, **Collision awareness**: Wat wordt er getoond? Ook dit artikel geeft weinig inzicht in de soort visualisaties en welke concrete elementen getoond worden. _Wordt het robot pad gevisualiseerd? Zijn er collisiezones of visuele indicatie van proximity? Zijn er safety zones en identificering van boundaries of objecten? Hoe wordt intent overgedragen? Pijlen, animaties?_

**Feedforward aspect**: Paper vermeldt "warnings/info" via AR maar specificeert niet wat vooraf getoond wordt. Onduidelijk of systeem toekomstige robot-bewegingen visualiseert of enkel real-time waarschuwingen geeft bij te korte afstand.

---

# Conclusie uit alle artikelen

## Feedforward coverage per kerncomponent

| Paper | Traject-voorspelling | Collision Awareness | Spatial Awareness | Feedforward Type |
|-------|---------------------|---------------------|-------------------|------------------|
| 1. RPAR-II | ✅ Pre-validatie | ⚠️ Niet expliciet | ✅ AR-simulatie | Planning-fase, pre-calculated |
| 2. Collision-free paths | ⚠️ Onduidelijk | ✅ CFV + beam search | ✅ AR volumes | Planning-fase, interactive |
| 3. Mind the ARm | ⚠️ Nabije toekomst | ✅ Proximity via Volume | ✅ 3 visualisatie-types | Real-time, tijdens uitvoering |
| 4. On-line collision avoidance | ❌ Geen visualisatie | ⚠️ Technisch, niet visueel | ❌ Geen AR | Geen feedforward (reactief) |
| 5. Collaborative workspace | ⚠️ Onduidelijk | ⚠️ Warnings vermeld | ⚠️ AR vermeld | Onduidelijk wat getoond wordt |

## Belangrijkste bevindingen

**Visualisatie-onduidelijkheden**: Terwijl artikelen claimen AR-visualisatie te gebruiken, blijven concrete implementatie-details vaag. Specifiek ontbreekt informatie over:
- **Animatie-types**: ghost-trails, pijlen, opacity-variaties?
- **Dynamische aspecten**: snelheid, acceleratie, timing?
- **Real-time vs pre-calculated**: wanneer wordt wat getoond?
- **Visuele feedback elementen**: kleuren, vormen, patronen?

**Feedforward gaps**: 
- Papers 1-2 focussen op **planning-fase** (vooraf simuleren), maar misschien onnutig wegens dit niet real-time gebeurt.
- Paper 3 biedt **real-time feedforward** maar beperkt tot nabije toekomst. 
  - _Dit artikel is waarschijnlijk het beste en meest overeenkomende met de huidige use case._
- Papers 4-5 vermelden technische collision avoidance maar geven geen/onduidelijke operator feedforward

**Kerncomponent coverage**: Geen enkel artikel adresseert alle 3 kerncomponenten volledig met expliciete visualisatie-methoden. Meeste artikelen behandelen 2 van de 3 componenten, **waarbij traject-voorspelling het minst uitgewerkt is qua visuele feedforward.**

---

## Alle bezochte artikels

**Niet relevant:**
- https://ieeexplore.ieee.org/abstract/document/7588033 - Hand grip via robotische hand als prosthese (geen toekomstige bewegingen, geen feedforward visualisatie, prosthetics)
- https://www.sciencedirect.com/science/article/pii/S2405896319300278 - Feedforward als controlmechanisme in motor tasks (geen AR, geen robotarm, geen industriële context, geen visualisatie, geen HRI)

**Relevant:**
- https://www.sciencedirect.com/science/article/abs/pii/S0736584511001116 - Interactive robot trajectory planning (zie sectie 1)
- https://www.sciencedirect.com/science/article/pii/S0736584508000665 - Collision-free paths (zie sectie 2)
- https://dl.acm.org/doi/abs/10.1145/3404983.3405509 - Mind the ARm (zie sectie 3)
- https://www.sciencedirect.com/science/article/pii/S0921889019300648 - On-line collision avoidance (zie sectie 4)
- https://www.sciencedirect.com/science/article/pii/S0957415822000204 - Development and Implementation of a Collaborative Workspace (zie sectie 5)


## Gebruikte keywords:
- HRI
- feedforward HRI
- feedforward augmented reality
- feedforward augmented reality robotics
- predictive visualization
- trajectory visualization 
- trajectory visualization feedforward
- robot trajectory visualization AR - https://www.sciencedirect.com/science/article/abs/pii/S0736584511001116
  - Doorgeklikt via vorige: https://www.sciencedirect.com/science/article/pii/S0736584508000665
- motion intent visualization for robot arms - https://dl.acm.org/doi/abs/10.1145/3404983.3405509
- AR collision avoidance industrial robots - https://www.sciencedirect.com/science/article/pii/S0921889019300648 
  - Nog een artikel onder deze zoekterm - https://www.sciencedirect.com/science/article/pii/S0957415822000204

## Mogelijks goede (nog te gebruiken) termen:
- visualizing robot reachability in danger zones AR
- augmented reality to improve operator spatial awareness robots
- AR robot programming visualization





