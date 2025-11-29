# Literatuurlijst relevant aan kerncomponenten uit onderzoeksprobleem

## Verduidelijking
Bij het zoeken naar literatuur betreffende _feedforward_ en _robotica_ kwam ik steeds terecht bij model-based feedforward.
Gezien de frequentie van dit zoekresultaat alsook de gelijkenis in woordkeuze wil ik even toelichten dat model-based feedforward iets anders is dan feedforward met
AR laag en visualisaties. _Dit onderwerp gaat eerder over de berekening van krachten wetende de lengte en zwaarte onder meer van een robotarm 
en hoeveel kracht nodig is een bepaald gewicht of voorwerp te dragen/behandelen._

De huidige use case is een feedforward die instructies van een robotarm kan inlezen en gebruiken in een taal voor visualisaties geschikt in een AR laag.
De gevonden literatuur wordt hieronder samengevat en besproken.

---
## Literatuurlijst

### 1. Interactive robot trajectory planning and simulation using Augmented Reality

**Auteurs:** H.C. Fang, S.K Ong, A.Y.C. Nee  
**Jaar:** 2011  
**Link:** https://www.sciencedirect.com/science/article/abs/pii/S0736584511001116

| Bevindingen | Problemen/Gaps | Kerncomponent(en) |
| ----------- | -------------- | ----------------- |
| RPAR-II combineert AR-simulatie met robot dynamica en time-optimal trajectory optimization; pre-validatie van trajecten inclusief overshoot detectie; visuele evaluatie en tuning van controller-parameters | Bestaande AR-methoden negeren dynamische beperkingen (velocity, acceleration); VR vereist complete a priori kennis; PbD produceert suboptimale/jittery paden; teaching pendant programmering onintuïtief | Traject voorspelling, spatial awareness |

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

### Onduidelijkheden & gaps

**Traject voorspelling**: Toont toekomstige robot positie enkel voor nabije toekomst en niet het volledige pad. Ook geen bewegingsdynamica.

---

# Conclusie uit alle artikelen

Veel onduidelijkheden rond het visualisatie-aspect in AR. Zowel traject voorspelling als collisie als spatial awareness worden niet expliciet apart behandeld omtrent bepaalde animatie. Meeste van de artikelen raken wel bepaalde functionaliteiten maar niet altijd alle 3 kerncomponenten tegelijkertijd.

---

## Alle bezochte artikels

**Niet relevant:**
- https://ieeexplore.ieee.org/abstract/document/7588033 - Hand grip via robotische hand als prosthese (geen toekomstige bewegingen, geen feedforward visualisatie, prosthetics)
- https://www.sciencedirect.com/science/article/pii/S2405896319300278 - Feedforward als controlmechanisme in motor tasks (geen AR, geen robotarm, geen industriële context, geen visualisatie, geen HRI)

**Relevant:**
- https://www.sciencedirect.com/science/article/abs/pii/S0736584511001116 - Interactive robot trajectory planning (zie sectie 1)
- https://www.sciencedirect.com/science/article/pii/S0736584508000665 - Collision-free paths (zie sectie 2)
- https://dl.acm.org/doi/abs/10.1145/3404983.3405509 - Mind the ARm (zie sectie 3)


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

## Nog te gebruiken:


- AR collision avoidance industrial robots
- visualizing robot reachability in danger zones AR
- augmented reality to improve operator spatial awareness robots
- AR robot programming visualization





