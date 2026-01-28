# Onderzoeksvragen

De onderzoeksvragen vormen de uiteindelijke doelen waar ik mijn pijlen op wil richten tijdens de implementatiefase. Deze doelen komen rechtstreeks uit bevindingen van de probleembeschrijving en uit inspiratie van de literatuurstudie. De onderzoeksvragen kunnen tijdens het project verder verfijnd worden naarmate nieuwe inzichten of bepaalde prioritizering/haalbaarheid ontstaat.


## Traject-voorspelling

Uit de literatuurstudie blijkt dat er in bestaande onderzoeken veel onduidelijkheid is over hoe traject-voorspelling visueel wordt vormgegeven. Sommige artikelen vermelden het gebruik van AR en beam search voor het tonen van paden, maar geven weinig details over de concrete visualisatievormen (zoals animaties, snelheids- of acceleratie-indicatoren). Dit is mogelijks wel een uitbreiding op een basis concept of een al goed functionerende maar echter simpele traject-voorspelling visualisatie. Ook is vaak niet duidelijk of deze visualisaties real-time zijn of enkel pre-calculated. In "Mind the ARm" wordt traject-voorspelling enkel voor de nabije toekomst getoond, wat dus een beperking kan vormen waar uitbreiding op mogelijk is. Dit biedt een kans om te onderzoeken hoe deze feedforward verder kan reiken en concreter kan worden gemaakt voor de operator.

**Onderzoeksvraag:**
Het doel is om, op basis van de beperkingen uit de literatuur, een visuele feedforward te ontwikkelen die het volledige traject en eventueel ook de dynamica (zoals snelheid en acceleratie) van de robotarm duidelijk en intuïtief weergeeft aan de operator. Hiervoor zullen verschillende visualisatietechnieken (zoals ghost-trails, pijlen, animaties) voor traject-voorspelling worden ontworpen, met als focus de bruikbaarheid en effectiviteit.


## Collision awareness

Uit de literatuurstudie blijkt dat er veel onduidelijkheden zijn over hoe collision awareness visueel wordt ondersteund. Artikelen beschrijven vaak niet duidelijk hoe collisies worden vermeden, welke objecten of zones betrokken zijn, of hoe proximity warnings en collisie zones worden weergegeven. In sommige gevallen wordt enkel gecontroleerd op end-effector collisies, terwijl botsingen met andere delen van de robotarm niet worden meegenomen. Ook is het vaak onduidelijk of collision awareness dynamisch inspeelt op veranderende omgevingen of enkel statisch is. Visualisaties zoals geometrische capsules worden soms genoemd, maar de concrete uitwerking blijft vaag.

**Onderzoeksvraag:**
Het doel is om, op basis van de beperkingen uit de literatuur, visuele hulpmiddelen te ontwikkelen die collision awareness voor de operator verhogen. Hierbij ligt de focus op het ontwerpen en implementeren van verschillende visualisatietechnieken voor collisie zones en proximity warnings (zoals mogelijke capsules, kleurzones, waarschuwingen), en ook hier het vergelijken van hun bruikbaarheid en effectiviteit in een bepaalde setting.


## Spatial awareness

Spatial awareness fungeert als een overkoepelende term die zowel traject-voorspelling als collision awareness omvat, maar ook verder gaat. Het draait om het bieden van een volledig en intuïtief 3D-overzicht van de robot, zijn bewegingen en de omgeving, zodat de operator een accuraat mentaal model kan vormen van de situatie. Het doel is om de gebruiker optimaal inzicht te geven in de volledige feedforward, inclusief ruimtelijke relaties, posities, oriëntaties en mogelijke interacties tussen robot en omgeving.

Deze kerncomponent is bewust gedefinieerd als vangnet voor mogelijke onduidelijkheden of uitbreidingen die pas later in het project naar voren komen. Spatial awareness kan namelijk ook extra aspecten omvatten die niet direct onder de andere kerncomponenten vallen, en fungeert zo als categorie voor 'evolutionary requirements' die gaandeweg tevoorschijn kunnen komen.

**Onderzoeksvraag:**
Hoe kunnen verschillende 3D-visualisaties en AR-technieken bijdragen aan het vergroten van spatial awareness bij operators, zodat zij een vollediger en betrouwbaarder inzicht krijgen in de toekomstige toestand en interacties van de robot in zijn omgeving?


## Conclusie

De onderzoeksvragen in dit document zijn gericht op het verbeteren van de visuele ondersteuning voor operators bij het werken met robotarmen, met specifieke aandacht voor traject-voorspelling, collision awareness en spatial awareness. Het onderdeel van grote belang is het ontwikkelen van effectieve visualisaties die het inzicht, de veiligheid en de efficiëntie van de operator vergroten. De technische implementatie valt buiten de scope; de focus ligt volledig op het visualisatie-aspect. De onderzoeksvragen kunnen tijdens het project verder worden bijgestuurd naarmate nieuwe inzichten ontstaan.

