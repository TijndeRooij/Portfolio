# Individual project
Voor mijn inividueel project ga ik een webapplicatie maken die producten voor een school bijhoud. De bedoeling is dat de gebruiker alle producten die deze school heeft kan zien en reserveren. Per product wordt bijgehouden welke leerlijnen eraan gekoppelt zijn zodat de docent een betere keuze kan maken. Ook wordt er per product bijgehouden wie dit product heeft, hierdoor kan een product nooit meer kwijtraken. Dit is nu namelijk wel nog een probleem.

## Keuzes

  - Vue.js. Voor de frontend heb ik gekozen om Vue.js te gebruiken. Ik heb deze keuze gemaakt omdat ik nog nooit met een dergelijk framework heb gewerkt en dit het meeste leek op HTML/CSS waar ik al wel bekend mee was.
  - Java Spring. Voor de backend heb ik gekozen om Java Spring te gebruiken. Ik wilde de taal java al wat langer leren. Daarom heb ik voor deze taal gekozen. Ik gebruik het spring framework omdat hier het meest over te vinden is. Ik had nog nooit met java gewerkt daarom leekt het mij slim om een framework te kiezen waar veel over te vinden is.
  - MYSQL. Voor de database heb ik gebruik gemaakt van een MYSQL database. Als oorspronkelijke keuze wilde ik MongoDB gebruiken, maar na heel lang proberen lukte het mij niet om deze database te koppelen aan Intellij. Daarnaast wordt de data in MonogDB niet makkelijk opgeslagen voor mijn app, aangezien ik rationele data gebruik.
  - JWT. Voor de Authorizatie en Authenticatie heb ik gekozen voor JWT tokens. Ik heb deze keuze gemaakt omdat ik nog nooit iets met authorizatie/authenicatie had gedaan en er over JWT tokens het meest te vinden was. Ook hebben de meeste klasgenoten van mij gekozen voor JWT tokens. Dit is makkelijk omdat ik nu overal terecht kan als ik vast loop.

## User stories

  - De gebruiker moet een duidelijk overzicht hebben van alle producten. Zodat hij gemakkelijk een product kan uitzoeken om zijn/haar les mee te vullen.
  - De gebruiker moet kunnen sorteren op id, rating, hoeveelheid. Zodat de gebruiker producten kan gebruiken die het beste bij zijn/haar les passen.
  - De gebruiker moet een product van tevoren kunnen reserveren. Zodat hij nooit mispakt op dit product.
  - De gebruiker moet een duidelijk overzicht hebben van zijn producten en wanneer hij/zij deze weer moet inleveren. Zodat hij/zij precies weet welk product hij/zij nog heeft en het product ook weer gereserveerd kan worden als hij/zij dit product niet meer.
  - De gebruiker moet kunnen aangeven of hij/zij het product heeft. Ook als hij/zij deze niet had gereserveerd. Zodat dit product nooit kwijtraakt.
  - Alleen gebruikers met de rol van ‘admin’ kunnen producten toevoegen. Zodat de database onder controle blijft.

## Leerdoelen

### Web application
#### Frontend
Ik heb voor mijn frontend in mijn individueel project gekozen voor Vue.js. In mijn groepsproject ben ik ook verantwoordelijk geweest voor de frontend. Hier hebben wij gekozen voor React-native. Dit is de mobile versie van React. Onze stappen gingens als volgt:
- 1. Eerst hebben wij ervoor gekozen om wireframes te maken van alle schermen. Dit hielp ons goed te begrijpen waar alle knoppen en tekstbalken op het scherm geplaatst moetsten worden zonder dat het veelste druk werd. 
- 2. Vervolgens hebben wij alle schermen gedesignt in [Figma](https://www.figma.com/file/xFwUW9U0uNMT426Bo1XvKa/IO-team-library?node-id=0%3A1). Figma is een heel goed programma om designs te maken. Van alle scheren hebben wij meerdere designs gemaakt en deze onder elkaar geplaatst. Hieronder ziet u ons figma bord.<br />  <img src="https://user-images.githubusercontent.com/113592556/206133314-ce3d159d-9a44-4d9a-9f2f-dc75cb82bef4.png" width="600" height="410" /> <br /> 
Zodra wij tevreden waren over de hoeveelheid aan schermen, hebben we samen met ons groepje gekozen voor een design. <br /> 

- 3. Het laatste wat er nu moet gebeuren is het maken van alle scheren in React-native. Aangezien ikzelf nog nooit had gewerkt met React-native heeft me het veel tijd gekost om dit te gaan begrijpen. 
In React-native hebben wij gebruik gemaakt van het atomic-design. Dit is een manier om alle components op te splitsen in 4 onderdelen:<br /> 
    - Atoms<br /> 
    - Molecules<br /> 
    - Organisms<br /> 
    - Templates<br /> 
Deze 4 ondedelen gaan van klein naar groot. Bijvoobeeld: De Atoms is een vrijstaant object, een molecule is meerdere atoms bij elkaar, een organisme is meerdere molecules bij elkaar en een template is meerdere organismes bij elkaar. Hieronder ziet u daar een afbeelding over:<br /> 

![image](https://user-images.githubusercontent.com/113592556/206136242-277887a6-896a-4f51-b011-e9de0c5fc4b9.png)

#### Communicatie met backend
Ik heb voor mijn inividueel project een full stack webapp gemaakt. Voor de frontend heb ik gebruik gemaakt van Vue.js en voor de backend heb ik gebruik gemaakt van Java Spring. Ik heb in mijn individueel project wat minder de focus gelegt op het maken van een mooie frontend maar meer op het maken van een goed lopende backend. Voor de communicatie tussen de client en de server gebruik ik in mijn individueel project axios. <br />
![image](https://user-images.githubusercontent.com/113592556/202159213-cdf4cafe-fc5f-46ef-8abe-a10606581785.png)

In de afbeelding hierboven kunt u zien dat ik gebruik maakt van een authorization header. Deze header is gevult met een bearer token. Door deze header moet er voordat het werkelijke request gerunt kan worden een preflight request gedaan worden. Hierdoor zien de communicatie er zo uit:
![image](https://user-images.githubusercontent.com/113592556/202164303-264ccd7b-bf6c-429a-8956-da0b1f07e553.png)


