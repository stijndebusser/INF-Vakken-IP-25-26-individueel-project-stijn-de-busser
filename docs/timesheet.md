# 🕒 Timesheet

| Datum | Uren | Activiteit                                                                                                                 |
| ----- | ---- | -------------------------------------------------------------------------------------------------------------------------- |
| 28/11 | 0.5u | Setup omgeving                                                                                                             |
| 28/11 | 0.5u | Verslagen beschrijving                                                                                                     |
| 28/11 | 3u   | Onderzoek feedforward, bestaande algoritmen, pijnpunten, relevantie en opsplitsing in kerncomponenten van probleemstelling |
| 29/11 | 5u   | Partiële uitzoeking van gepaste literatuur en onduidelijkheden, beperkingen en kerncomponenten hieruit gehaald             |
| 30/11 | 2u   | Toevoeging aan literatuur & overzicht bevindingen + tabel |
| 28/01 | 2u   | Onderzoeksvragen |
| 29/01 | 1u   | Onderzoeksvragen |
| 12/02 | 4u   | Opzetten van Magic Leap 2 in unity |
| 12/02 | 2u   | Visualisatie bewegend blokje in unity met basis traject-lijn |
| 13/02 | 2.5u   | Eerste versie van de paper opgemaakt volgens template |
| 15/02 | 1.5u   | Powerpoint tussentijdse presentatie 19/02 |
| 19/02 | 0.5u   | Tussentijdse presentatie 19/02 |
| 19/02 | 1.5u   | Script vast pad/traject tussen punten in een ruimte. Update() functie van MonoBehaviour van Unity extension update het pad per frame naar een doelobject (nog niet getest in ML2). |
| 26/02 | 3u   | Setup XR handen met pinch/grab actie voor object (nog niet werkende)|
| 26/02 | 2u   | Setup XR handen met pinch/grab actie voor object (werkende met controllers in unity (zonder headset of handgebaren getest)) |
| 05/03 | 7u   | Setup XR handen met pinch/grab actie voor object werkende tezamen met huidige scène |
| 19/03 | 1u   | Meeting met supervisor om volgende stappen te bespreken zoals vermeld verslagen.md. |
| 20/03 | 6u   | Setup van gekregen scène met hand interaction settings (nog niet getest). Geprobeerd met AI het IK_Calculator.cs script aan te vullen om de robotarm naar nodes te kunnen verplaatsen. Dit werkt maar de arm bewegingen zijn niet exact en vaak inaccuraat. Setup van een eerste visualisatie met een traject/pad tussen nodes + collisies van pad met objecten. De objecten worden enkel geregistreerd van zodra hier een box/mesh collider op zit dus niet dynamisch. Doorgaan naar een volgende node visualiseerd een pad in de curve van de beweging, de curve loopt niet exact tot de node wat waarschijnlijk komt door de inaccuraatheid van de robotarm beweging tot node zelf. |
| 21/03 | 3u   | Kort verder de (nog inaccurate en nog steeds inaccurate curve/pad) visualisatie te verbeteren. |
| 26/03 | 6u   | Vorige voorbereidingen getest in de ML2. Vooral bezig geweest met configuratie van hand interactie tesamen met de scene. Verder de scene geprojecteerd te proberen te krijgen op een ArUco tag/marker wat momenteel ook werkt. De ArUco marker is een AprilTag 36h11 met ID: 0 en is 10cm bij 10cm. De huidige setup werkt na het tonen van de ArUco tag in de ML2. Het verplaatsen en vooral roteren hiervan werkt ook; maar slechts binnen een beperkte omgeving (de originele kijkrichting zowat). |
| 01/04 | 4.5u   | Pad traject implementatie verbeterd aangezien de vorige implementatie de arm naar achter forceerde. De nieuwe implementatie geeft een elbow up posture i.p.v. elbow down wat het een accurater resultaat geeft momenteel. Aangezien het pad nu meer nauwkeurig is, werd de visualisatie hiervan ook beter. Daarna verder gewerkt aan nieuwe visualisatie die een 'ghost skeleton' in bepaalde intervallen weergeeft met veranderingen aan opacity naargelang hoe de robotarm gepositioneerd was op dat moment. Ten laatste nog opgezocht en geprobeerd een soort clamping te maken aan een 'out of reach volume/sphere' van zodra een node buiten bereik is, maar vraag mezelf wel nog af of dit nodig is, en hoe dit aangegeven zou moeten worden. |
| 02/04 | 5u   | Gewerkt en verbetering van de ArUco tracking, deze is niet meer beperkt aan de initiële kijkrichting. De AR visualisaties zijn wel nog altijd minder accuraat dan in de Unity simulator wat mogelijks komt door micro-jitter als de scene zich de hele tijd correct wil calibreren aan de ArUco marker. In de Unity simulator zelf is de scene vastgezet waardoor de robotarm (en dus visualisaties) een stuk accurater zijn. Vorige keer had ik een ghost skeleton van het pad geïmplementeerd maar dat waren enkel editor-only gizmos dus deze zijn nu LineRenderers zodat deze zichtbaar zijn in AR. De lijnen zelf verdwijnen van zodra de robotarm hier al voorbij is. Ten laatste nog gewerkt aan het spawnen van (interactable) nodes bij een linkshandig pinchgebaar. Het probleem hierbij was dat dit onbeperkt zou blijven verschijnen, wat nu tijdelijk (of mogelijks permanent) opgelost wordt door de pinchactie 2 seconden lang te laten duren met progress bar vooraleer er daadwerkelijk één wordt gecreëerd. De pinchactie is wel erg gevoelig. De nodes worden ook automatisch afgelopen op volgorde tot de laatste node. |
| 24/04 | 4u   | Abstract en alle secties van de eerste versie in paper verbeterd + eerste versie van Methodologie met subsecties  |





