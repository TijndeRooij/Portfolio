# Groepsproject

## Leeruitkomsten
<details open>
<summary> 
Agile werken
</summary>
<br />
Er zijn verschillende methodes om in een software development team te werken. Voorbeelden hiervan zijn de Waterfall method, agile method en de hybrid method. Al deze methodes zijn goed om mee te werken en vaak kiest de ontwikkelaar samen met de stakeholder welke methode gekozen gaat worden.

Bronnen: [BigPicture](https://bigpicture.one/waterfall-agile-hybrid-differences/)

#### Waterfall 
<img src='https://user-images.githubusercontent.com/113592556/207596108-ee09b075-f55c-41eb-94cf-80f236d10971.png' align="left" height="200" />
Waterfall is een methode om development teams te helpen hun 
Zoals hierlangs zichtbaar is in de afbeelding bestaat de Waterfall methode uit 5 verschillende fases. Dit zijn: Requirements, Design, Implementation, Verification or testing, Deployment and maintenance. Deze fases staan los van elkaar. Dit houdt in dat er niet zomaar terug naar de vorige stap gegaan kan worden. Dit is namelijk lastig en duur. Vandaar ook de naam waterfall. 

<br />

| Voordelen | Nadelen|
| --- | --- |
| - De software ontwikkelaars kunnen eerder fouten in het design vinden, wat ervoor zorgt dat er in een later stadium geen fouten worden gemaakt.| - Projecten kunnen lager duren met deze methoden.
| - De totale van het project kosten kunnen makkelijker worden geschat.| - Stakeholders weten niet meteen hoe ze de frontend willen hebben, dit zorgt voor veranderingen in de toekomst maar dan zijn ze lastiger te implementeren.
| - De voorgang kan makkelijker worden geschat.| - Stakeholders worden niet op de hoogte gehouden van de design en implementation stage.
| - Software ontwikkelaars die later in het project erbij komen kunnen makkelijker worden bijgepraat.| - Wanneer er 1 fase langer duurt dan verwacht worden alle fases opgeschoven.
| - Klanten kunnen niet zomaar requirements veranderen.|

#### Azure
In ons groepsproject maken wij gebruik van Agile werken. We hebben een Azure board opgezet met alle userstories. Deze stories staan opgedeelt per sprint. Iedere userstorie is opgedeeld in tasks. Deze tasks zijn klein genoeg dat ze door 1 persoon gedaan kunnen worden. Ook staat er per task een bepaalde tijd ingedeeld. Uiteindelijk wordt hier een burndown chart van gemaakt. 
![image](https://user-images.githubusercontent.com/113592556/202182109-f89abe70-f032-42ec-a7d5-69516b917f67.png)
Hierboven ziet u ons azure board. Deze is niet compleet omdat er altijd tasks bij kunnen komen. Er kunnen ook altijd tasks veranderen. Een goed voorbeeld daarvan staat hieronder. <br />
<br />
|Voorbeeld|
|:--:|
|In het begin van ons groepsproject gepraat werd over SSO. Dit is een manier van inloggen en iO had gewilt dat wij dit in ons project hadden geïmplementeert. We hebben hier vervolgens alles voor opgezet maar kwamen er achter dat er vanuit iO niet de goede producten geleverd konden worden. We zijn daarom alsnog van plan moeten veranderen en hebben nu Amazon Cognito gebruikt voor de login.| <br />

#### Burndown chart
Omdat wij gebruik maken van azure krijgen wij ook een burndown chart. Dit is een grafiek die laat zien of wij onze tasks goed hadden gepland. Je kan namelijk in iedere task aangeven hoelang je erover denkt te doen. Doe je er vervolgens langer of korter over verandert de burndown chart. Een correcte burndown chart ziet er zo uit:

<img src='https://user-images.githubusercontent.com/113592556/206189571-50f08dcc-9549-4549-a6b9-accbbf526d30.png' height="300" />
</details>

<details open>
  <summary>
    Cultural differences en ethics
  </summary>
  
#### Cultural differences

Ik heb een IDI afgelecht om mijn gedachten over cultuur verschillen te zien. Hier kwam uit dat ik zelf het gevoel heb dat ik goed kan omgaan met culturele verschillen en dat ik me in beide schoenen kan plaatsen omdat ik gemakkelijk overeenkomsten zie.
![image](https://user-images.githubusercontent.com/113592556/206206874-ec00972a-860a-441c-a7dd-b092b06ba64b.png)

Dit is volgens de test niet helemaal waar. Volgens de test kom ik uit op Polarization. Dit houd in dat ik een *'jugemental view'* heb naar andere culturen.<br />
![image](https://user-images.githubusercontent.com/113592556/206207527-109c1831-7869-4389-9b0e-93521f1f52a1.png)<br />
Dit heeft ook bepaalde goede punten. Zo zal ik waarschijnlijk goed om gaan met moeilijke culturele conflicten en zal ik niet de neiging krijgen om dit te negeren.
Ook geeft mij dit mogelijkheden om te verbeteren. Een bepaalde mogelijkheid kan zijn om opzoek te gaan naar culturele verschillen en mezelf hier bij neer te leggen. Hierdoor zal ik de overeenkomsten tussen mijn cultuur en iemand anders zijn cultuur makkelijker zien.
<br/>
Omdat mijn PO hoger is dan mijn DO overschat ik mezelf in hoe ik mij aanpas in andere cuturen. Andere zullen mij waarschijnlijk zien als iemand die zich niet zo gemakkelijk zou aanpassen aan culturele verschillen.<br />
<br />
Ik heb in mijn IDI ook een test gemaakt over dit onderwerp. Hier werd ik bekend gemaakt met de verschillen tussen PO en DO en waarom dit zo is. Ik heb op deze test een score gehaalt van 83%.

![image](https://user-images.githubusercontent.com/113592556/206204689-9afc2ebe-3d4d-4f11-a8a4-0e3dfeae8ea6.png)

<br />

#### Ethics
Het onderdeel ethics wil ik aantonen door over het etisch aspect van ons groepsproject te gaan. We maken namelijk een app om te zien waar een collega zichzelf bevind. Dit doen wij door middel van WiFi data. Deze data wordt een keer per kwartier naar ons gestuurd. Hierdoor kunnen we zien of een werknemer thuis, niet of op kantoor aan het werk is. Als een werknemer op kantoor is kunnen we ook zien op welke verdieping hij zich bevind. <br />
Ikzelf vind de ethiek achter een trakker app niet heel goed. Goede voorbeelden hiervan zijn deze apps: Spy Tracker, SMS Tracker, Phone Cell Tracker, Spy Kids Tracker en Employee Work Spy. Deze 7 apps waren bedoeld om kinderen, werknemers of partners te volgen. Zolang de app op de telefoon van de gezochte persoon geïnstalleerd was konden je werkgevers, ouders of partner zien waar u zich bevond. Toen google play hierachter kwam werden deze apps meteen verwijdert van de playstore. Deze apps gaven ook instructie om de installatie van deze apps te verbergen zodat het slachtoffer niks doorhad. <br />
Nou gaat het voorbeeld hierboven wel heel ver. Wij vragen namelijk aan de gebruiker of wij zijn WiFi data mogen uitlezen. Dit wordt 1 keer in de 12 uur opnieuw gedaan. Ook als de gebruiker op nee drukt kan de gebuiker de app gewoon normaal gebruiken maar wordt zijn data niet gebruikt. Zijn data wordt wel (ook als er op nee gedrukt wordt) doorgegeven met de rest van de WiFi data. Deze data komt ook in de backend. Hier wordt er pas gekeken wat de voorkeur was. Dit laatste verandert het ethisch aspect drastich voor mij. Want ook als de gebruiker op nee drukt wordt hij dus wel gevolgd. <br />
Om het ethisch aspect van de app beter te maken zijn er wel bepaalde dingen die de wergever kan doen. 
- De werkgever zou de app goed kunnen uitleggen en daarmee ook uitleggen dat je de keuze altijd kan aanpassen. 
- De werkgever zou het installeren van de app niet verplicht hoeven te maken.
- Er zou in een later stadium van de ontwikkeling van de app een optie kunnen komen om zelf handmatig jouw status aan te passen.

Bronnen: [Tweakers](https://tweakers.net/nieuws/155278/google-verwijdert-zeven-apps-bedoeld-om-mensen-te-volgen-uit-play-store.html)
</details>
  
### Requirements and design
You analyze (non-functional) requirements, elaborate (architectural) designs and validate them using multiple types of test techniques.

Clarification:
Multiple types of test techniques: You apply user acceptance testing and stakeholder feedback to validate the quality of the requirements. You evaluate the quality of the design (e.g., by testing or prototyping) taking into account the formulated quality properties like security and performance.

### Professional
You act in a professional manner during software development and learning.

Clarification:
Professional manner: 

You develop software as a team effort according to a prescribed software methodology and following team agreements. You are able to track your work progress and communicate your progress with the team.

You actively ask and apply feedback from stakeholders and advise them on the most optimal technical and design (architectural) solutions.
You choose and substantiate solutions for a given problem.


