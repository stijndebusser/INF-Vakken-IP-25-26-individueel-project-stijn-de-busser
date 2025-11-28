# Probleemstelling feedforward
Huidig document introduceert een korte inleiding en beschrijft de probleemstelling voor **feedforward**, opgebouwd volgens vijf concrete stappen voor probleemdefiniëring.

---

## Inleiding: wat is feedforward?

Feedforward is een vorm van proactieve informatiebekoming waarbij toekomstige toestanden, acties en dus ook consequenties worden gevisualiseerd **alvorens** ze plaatsvinden. In tegenstelling tot normale feedback die reageert op gebeurtenissen die al hebben plaatsgevonden, anticipeert feedforward op basis van geplande instructies, coördinaten of bewegingscommando's op wat er nog te verwachten valt, en visualiseert deze overeenkomstig.

### Context: robotarm

Het is belangrijk de huidige context te illustreren alvorens we beginnen aan de probleemstelling. Op die manier is er een concreet voorbeeld ter beschikking. Deze context bestaat uit een robotarm die allerlei acties kan ondernemen in een manufacturing-omgeving. Een mogelijke toepassing van feedforward is het visualiseren van toekomstige bewegingstrajecten, potentiële collisies, gevaarzones en eindposities. Daarnaast kan feedforward aangeven waar de robot naartoe zal bewegen, hoe snel de robot zich zal verplaatsen, waar gebruikers zich niet mogen begeven, of wanneer de robot een object zal overhandigen.

Ook essentieel om te vermelden is dat moderne robotarmen al geavanceerde motion planning algoritmes bezitten. RRT, A* of PRM, collision detection systemen en trajectory optimization kunnen allemaal gebruikt worden om de robotarm optimaal te laten functioneren. Al deze effectiviteit leidt mogelijk tot kritische vragen omtrent het nut van feedforward.

### Waarom feedforward ondanks geavanceerde algoritmes?

Het antwoord ligt in de fundamentele rol van de menselijke operator in het proces:

1. **Verificatie en leerproces**: Algoritmes kunnen theoretisch correct zijn, maar deze zullen altijd geverifieerd moeten worden. Zonder visuele confirmatie ontstaat er een _black box_ situatie waarbij operators blind moeten vertrouwen op de berekeningen en theorie. Feedforward maakt dit proces verifieerbaar. Dit gaat hand in hand met programmeren en het troubleshooting proces daarachter, wat vaak een trial-and-error proces is. Het leerproces van de operator wordt op deze manier versneld.

2. **Domeinspecifieke kennis**: Operators beschikken over bepaalde domeinspecifieke informatie die algoritmes niet hebben. _Waar loopt een medewerker? Wat is fragiel materiaal dat zorgzaam behandeld moet worden?_ Met feedforward wordt dit proactief verhandeld voordat enige schade of inefficiëntie optreedt.

3. **Algoritmes zijn niet feilloos**: Motion planning algoritmes werken op basis van een digitaal model van de omgeving. Als dit model verouderd, onvolledig of onnauwkeurig is (bijvoorbeeld door niet-geregistreerde obstakels of verplaatste objecten), kunnen algoritmes foutieve plannen genereren. Feedforward fungeert als een visuele safety check waarbij de operator inconsistenties kan opmerken.

**Op het einde van de dag blijven operators verantwoordelijk voor cruciale beslissingen over veiligheid, kwaliteit en procesoptimalisatie. Feedforward versterkt de operator met essentiële inzichten in plaats van deze rol over te nemen.**

---

## 1. Onderzoeksprobleem

In moderne manufacturing-omgevingen worden robotarmen steeds vaker ingezet voor repetitieve en precisienauwkeurige taken. Operators die deze robotarmen instellen, programmeren of monitoren, missen echter vaak visuele feedback over toekomstige bewegingen. Dit gebrek aan voorspellende informatie leidt tot drie belangrijke uitdagingen. Deze zijn opgesplitst in kerncomponenten:

1. **Gebrek aan traject-voorspelling**: Operators vinden het moeilijk of kunnen helemaal niet anticiperen op het volledige bewegingspad van de robot. Dit kan leiden tot foutief of onnauwkeurig instellen of programmeren, waarbij operators onzeker blijven of de ingestelde parameters tot de gewenste beweging zullen leiden.

2. **Onvoldoende collision awareness**: Potentiële collisies worden te laat of pas na impact zichtbaar, wat schade kan aanrichten aan de fysieke robotarm, tooling of werkstukken.

3. **Beperkte spatial awareness**: Dit is een algemeen probleem dat mogelijk de vorige twee uitdagingen omvat. Bij het instellen wordt over het algemeen geen gebruik gemaakt van een reële 3D-omgeving, in tegenstelling tot hoe de situatie in realiteit ervaren wordt. Zelfs speciaal gemaakte visualisaties kunnen tekortkomen aan de noden van een volledige 3D-interpretatie. Het is ingewikkeld een ruimtelijk mentaal model te vormen op basis van 2D-schermen.

Deze uitdagingen resulteren in langere programmeertijden waarbij er vaak onzorgvuldig te werk wordt gegaan. Daarnaast is er een verhoogde kans op beschadigingen, en blijft de communicatie van planning naar menselijke operator problematisch.

---

## 2. Relevantie

Zoals eerder al vermeld op verdeelde wijze, kan het gebrek aan feedforward-visualisaties leiden tot langere programmeertijden en verhoogd risico op schade aan de robot en werkstukken. Verbeteringen in feedforward dragen bij aan meer betrouwbare en efficiënte robotbediening, verhogen de veiligheid in manufacturing-omgevingen, en ondersteunen operators bij het sneller en beter begrijpen van robotgedrag.

---

## Referenties

