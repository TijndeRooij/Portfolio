# Groepsproject

## Leeruitkomsten
<details open>
<summary> 
Agile werken
</summary>
<br />
Er zijn verschillende methodes om in een software development team te werken. Voorbeelden hiervan zijn de Waterfall method, agile method en de hybrid method. Al deze methodes zijn goed om mee te werken en vaak kiest de ontwikkelaar samen met de stakeholder welke methode gekozen gaat worden.

Bronnen: [BigPicture](https://bigpicture.one/waterfall-agile-hybrid-differences/)

### Waterfall 
<img src='https://user-images.githubusercontent.com/113592556/207596108-ee09b075-f55c-41eb-94cf-80f236d10971.png' align="left" height="200" />
Waterfall is een methode om development teams te helpen hun proces in orde te houden. Deze methode zorgt voor sturctuur in het proces door taken te organiseren.
Zoals hierlangs zichtbaar is in de afbeelding bestaat de Waterfall methode uit 5 verschillende fases. Dit zijn: Requirements, Design, Implementation, Verification or testing, Deployment and maintenance. Deze fases staan los van elkaar. Dit houdt in dat er niet zomaar terug naar de vorige stap gegaan kan worden. Dit is namelijk lastig en duur. Vandaar ook de naam waterfall. 

<br />

| Voordelen | Nadelen|
| --- | --- |
| - De software ontwikkelaars kunnen eerder fouten in het design vinden, wat ervoor zorgt dat er in een later stadium geen fouten worden gemaakt.| - Projecten kunnen lager duren met deze methoden.
| - De totale van het project kosten kunnen makkelijker worden geschat.| - Stakeholders weten niet meteen hoe ze de frontend willen hebben, dit zorgt voor veranderingen in de toekomst maar dan zijn ze lastiger te implementeren.
| - De voorgang kan makkelijker worden geschat.| - Stakeholders worden niet op de hoogte gehouden van de design en implementation stage.
| - Software ontwikkelaars die later in het project erbij komen kunnen makkelijker worden bijgepraat.| - Wanneer er 1 fase langer duurt dan verwacht worden alle fases opgeschoven.
| - Klanten kunnen niet zomaar requirements veranderen.|
  
Bronnen: [Adobe Experience Cloud Blog](https://business.adobe.com/blog/basics/waterfall#:~:text=The%20Waterfall%20methodology%20%E2%80%94%20also%20known,before%20the%20next%20phase%20begins.)

### Agile
Agile is ook een methode om development teams structuur te geven. Maar het is heel anders dan Waterfall. Waar waterfall zijn kracht haalt in het vooraf afspreken wat er gaat gebeuren doet agile dat precies tegenovergesteld. Agile is een methode die juist zijn kracht haalt in het hebben van een itteratief proces. Bij agile is het aanpassen van tasks niet heel lastig en ook goedkoper dan bij waterfall, maar dit gebeurt hierdoor ook meer. Het beste is om deze methode te gebruiken wanneer een snelle productie nodig is.
  
<br />
  
| Voordelen | Nadelen |
| --- | --- |
| - Je kan requirements makkelijk aanpassen midden in het proces.| - Er moet een gemotiveert team en bij het scrum framework ook een gemotiveerde scrum master zijn.
| - Het verwijderen en toevoegen van features is gemakkelijk.|
| - Bugs kunnen al vroeg weggehaald worden.|
| - De stakeholders kunnen eerder feedback geven.|

<br />

Bij het werken van agile kun je kiezen tussen verschillende frameworks. Deze framworks zijn: Scrum, Kanban, scrumban en Extreme Programming (XP). Scrum is op het moment het meest gebruikte framework. Het wordt namelijk volgens de 15th State of Agile report door 66% van alle agile teams gebruikt. Dit komt omdat agile scrum makkelijk is om mee te beginnen.
  
#### Scrum
Bij scrum werk je in een team aan een project. Het project wordt opgedeeld in sprints. Een sprint bestaat uit een aantal weken, dit spreek je van te voren af met je stakeholder. Tijdens een sprint werk je samen met je team aan verschillende userstories of requirements. Deze userstories of requirements zijn opgedeeld onder de teamleden, en ieder doet zijn deel. Aan het einde van een sprint laat je aan je stakeholder zien wat je hebt en zij geven hier feedback op. Ook zit er aan het einde van iedere sprint een retrospective. Hierin ga je met je team kijken wat er goed ging en wat er minder goed ging zodat je jezelf en je team hierop kan verbeteren. Het team in het scrum framework is opgedeeld in verschillende rollen. Deze zijn de rol van de stakeholder, de rol van de scrum master en de devops. De stakeholders zijn de eigenaren van het project en vaak ook de mensen waarvoor het project gemaakt wordt. De scrum master is de persoon die het overzicht over het team houdt en hun helpt met scrum. De devops zijn de personen in het team die zich bezig houden met het maken van het project.
Scrum is een makkelijk framework om mee te beginnen zeker als je ook met andere teams moet werken zoals marketing of design teams, zij kunnen namelijk makkelijk aansluiten op de voorgang. 

#### Kanban

  
Bronnen: [userbrain](https://www.userbrain.com/blog/agile-waterfall-hybrid), [parabol](https://www.parabol.co/resources/agile-frameworks-guide/)
### hybrid
Hybrid is de method die beide (Agile en Waterfall) bij elkaar voegt. Het gaat van het vooraf bepalen van requirements, wat bij Waterfall gebeurt, naar het itteratief proces van agile.
  
| Voordelen | Nadelen |
| --- | --- |
| - De requirements worden goed gedocumenteerd.| - Heeft een goede manager nodig.
| - De kosten en tijd worden ook goed geschat| - Kan dezelfde problemen krijgen als agile en waterfall.
| - De stakeholders geven meer feedback

Bronnen: [userbrain](https://www.userbrain.com/blog/agile-waterfall-hybrid), [devfacto](https://www.devfacto.com/blog/a-hybrid-software-development-method)
### Azure
In ons groepsproject maken wij gebruik van Agile werken. We hebben een Azure board opgezet met alle userstories. Deze stories staan opgedeelt per sprint. Iedere userstorie is opgedeeld in tasks. Deze tasks zijn klein genoeg dat ze door 1 persoon gedaan kunnen worden. Ook staat er per task een bepaalde tijd ingedeeld. Uiteindelijk wordt hier een burndown chart van gemaakt. 
![image](https://user-images.githubusercontent.com/113592556/202182109-f89abe70-f032-42ec-a7d5-69516b917f67.png)
Hierboven ziet u ons azure board. Deze is niet compleet omdat er altijd tasks bij kunnen komen. Er kunnen ook altijd tasks veranderen. Een goed voorbeeld daarvan staat hieronder. <br />
<br />
|Voorbeeld|
|:--:|
|In het begin van ons groepsproject gepraat werd over SSO. Dit is een manier van inloggen en iO had gewilt dat wij dit in ons project hadden geïmplementeert. We hebben hier vervolgens alles voor opgezet maar kwamen er achter dat er vanuit iO niet de goede producten geleverd konden worden. We zijn daarom alsnog van plan moeten veranderen en hebben nu Amazon Cognito gebruikt voor de login.| <br />

### Burndown chart
Omdat wij gebruik maken van azure krijgen wij ook een burndown chart. Dit is een grafiek die laat zien of wij onze tasks goed hadden gepland. Je kan namelijk in iedere task aangeven hoelang je erover denkt te doen. Doe je er vervolgens langer of korter over verandert de burndown chart. Een correcte burndown chart ziet er zo uit:

<img src='https://user-images.githubusercontent.com/113592556/206189571-50f08dcc-9549-4549-a6b9-accbbf526d30.png' height="300" />
</details>

<details open>
  <summary>
    Cultural differences en ethics
  </summary>
  
### Cultural differences

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

### Ethics
Het onderdeel ethics wil ik aantonen door over het etisch aspect van ons groepsproject te gaan. We maken namelijk een app om te zien waar een collega zichzelf bevind. Dit doen wij door middel van WiFi data. Deze data wordt een keer per kwartier naar ons gestuurd. Hierdoor kunnen we zien of een werknemer thuis, op kantoor aan het werk is. Als een werknemer op kantoor is kunnen we ook zien op welke verdieping hij zich bevind. <br />

#### Onze app
Ikzelf vind de ethiek achter een trakker app niet heel goed. Goede voorbeelden hiervan zijn deze apps: Spy Tracker, SMS Tracker, Phone Cell Tracker, Spy Kids Tracker en Employee Work Spy. Deze 7 apps waren bedoeld om kinderen, werknemers of partners te volgen. Zolang de app op de telefoon van de gezochte persoon geïnstalleerd was konden je werkgevers, ouders of partner zien waar u zich bevond. Toen google play hierachter kwam werden deze apps meteen verwijdert van de playstore. Deze apps gaven ook instructie om de installatie van deze apps te verbergen zodat het slachtoffer niks doorhad. <br />
Nou gaat het voorbeeld hierboven wel heel ver. Wij vragen namelijk aan de gebruiker of wij zijn WiFi data mogen uitlezen. Dit wordt 1 keer in de 12 uur opnieuw gedaan. Ook als de gebruiker op nee drukt kan de gebuiker de app gewoon normaal gebruiken maar wordt zijn data niet gebruikt. Zijn data wordt wel (ook als er op nee gedrukt wordt) doorgegeven met de rest van de WiFi data. Deze data komt ook in de backend. Hier wordt er pas gekeken wat de voorkeur was. Dit laatste verandert het ethisch aspect drastich voor mij. Want ook als de gebruiker op nee drukt wordt hij dus wel gevolgd. <br />
Om het ethisch aspect van de app beter te maken zijn er wel bepaalde dingen die de wergever kan doen. 
- De werkgever zou de app goed kunnen uitleggen en daarmee ook uitleggen dat je de keuze altijd kan aanpassen. 
- De werkgever zou het installeren van de app niet verplicht hoeven te maken.
- Er zou in een later stadium van de ontwikkeling van de app een optie kunnen komen om zelf handmatig jouw status aan te passen.

#### Culturele dimensies van Hofstede
De 6 culturele dimensies van Hofstede zijn bedacht door Geert Hofstede en vertegenwoordigen de keuzes van landen die ze onderscheiden van andere landen. De zes dimensies van hofstede zijn: Power distance, Individualism, Masculinity, Uncertainty Avoidance, Time Orientation, Indulgence.

#### Power distance
Power distace gaat over de gelijkwaardigheid tussen mensen in een land. Power distance wordt gemeten door te kijken naar wat mensen verwachten en accepteren aan machtverschil in een land. In een samenleving waar er een hoge Power distance is wordt er geaccepteerd dat er mensen zijn met meer macht dan anderen. Als er een lage Power distance is wordt dit niet geaccepteerd en wordt er rechtvaardigheid geïst voor de machtsongelijken.

#### Individualism
Individualism gaat over het individualistisch- of collectivistisch gedrag van mensen in een samenleving. Als een persoon individualistisch gedrag toont zal hij alleen voor zichzelf en zijn directe familie zorgen. Als een persoon collectivistich gedrag toont zal hij bij een groep horen die voor andere groepen zorgt en op deze manier loyaliteit tonen.

#### Masculinity
Masculinity gaat over hetgeen wat mensen motiveert. Dit kan zijn: de wil om het beste te zijn (masculinity) of houden van wat je doet (feminine). Masculinity staat voor een voorkeur voor: Prestatie, heldhaftigheid, assertiviteit en materieel succes. Deze sameleving is vaak heel erg competatief. Feminine staat daar in tegen voor een voorkeur voor: Relaties, bescheidenheid, zorg voor de zwakken en de kwaliteit van leven. Deze samenleving is vaak heel erg consensusgericht ([als de leden van een bepaalde groep of gemeenschap gezamenlijk een overeenstemming hebben bereikt](https://www.ensie.nl/redactie-ensie/consensus))

#### Uncertainty Avoidance
Uncertainty Avoidance gaat over de manier hoe een sameleving omgaat met de onwetendheid van de toekomst. Landen met een hoge Uncertainty Avoidance index hebben vaak veel regels die de toekomst een bepaalde weg insturen. Ook hebben deze landen vaak een geloof ontwikkeld die hiermee helpt. Landen met een lage Uncertainty Avoidance index hebben vaak wat minder regels die de toekomst sturen en zijn vaak wat rustiger en hebben minder principes.

#### Time Orientation
Time Orientation gaat over de manier hoe een samenleving omgaat met tradities, normen en waarden. Als een land hier hoog op scoort wordt er vooral gekeken naar de lange termijn. Zo is modern onderwijs belangrijk, familie is de basis van de sameleving en worden mannen, ouderen en hoogopgeleiden gewaardeert. Als een land hier laag op scoort wordt er vooral gekeken naar de korte termijn. Deze landen zijn vaak creatiever en individualistischer. 

#### Indulgence
Indulgence gaat over de terughoudendheid van verlangen en impulsen. Als een land hier laag op scoort is dat land vaak positiever en is de werk animo vaak lager. De mensen in dit land doen wat ze willen en geven geld uit wanneer ze dit willen. Ook zijn ze vaak optimistisch ingesteld. Als een land hier hoog op scoort heeft dit land vaak strikte normen en wordt de bevrediging van behoeftes onderdrukt.

Bronnen: [Tweakers](https://tweakers.net/nieuws/155278/google-verwijdert-zeven-apps-bedoeld-om-mensen-te-volgen-uit-play-store.html)
</details>
  
## Requirements and design
You analyze (non-functional) requirements, elaborate (architectural) designs and validate them using multiple types of test techniques.

Clarification:
Multiple types of test techniques: You apply user acceptance testing and stakeholder feedback to validate the quality of the requirements. You evaluate the quality of the design (e.g., by testing or prototyping) taking into account the formulated quality properties like security and performance.

## Professional
You act in a professional manner during software development and learning.

Clarification:
Professional manner: 

You develop software as a team effort according to a prescribed software methodology and following team agreements. You are able to track your work progress and communicate your progress with the team.

You actively ask and apply feedback from stakeholders and advise them on the most optimal technical and design (architectural) solutions.
You choose and substantiate solutions for a given problem.


