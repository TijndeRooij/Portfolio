# Individual project
Voor mijn inividueel project ga ik een webapplicatie maken die producten voor een school bijhoud. De bedoeling is dat de gebruiker alle producten die deze school heeft kan zien en reserveren. Per product wordt bijgehouden welke leerlijnen eraan gekoppelt zijn zodat de docent een betere keuze kan maken. Ook wordt er per product bijgehouden wie dit product heeft, hierdoor kan een product nooit meer kwijtraken. Dit is nu namelijk wel nog een probleem.

### Keuzes

  - Vue.js. Voor de frontend heb ik gekozen om Vue.js te gebruiken. Ik heb deze keuze gemaakt omdat ik nog nooit met een dergelijk framework heb gewerkt en dit het meeste leek op HTML/CSS waar ik al wel bekend mee was.
  - Java Spring. Voor de backend heb ik gekozen om Java Spring te gebruiken. Ik wilde de taal java al wat langer leren. Daarom heb ik voor deze taal gekozen. Ik gebruik het spring framework omdat hier het meest over te vinden is. Ik had nog nooit met java gewerkt daarom leekt het mij slim om een framework te kiezen waar veel over te vinden is.
  - MYSQL. Voor de database heb ik gebruik gemaakt van een MYSQL database. Als oorspronkelijke keuze wilde ik MongoDB gebruiken, maar na heel lang proberen lukte het mij niet om deze database te koppelen aan Intellij. Daarnaast wordt de data in MonogDB niet makkelijk opgeslagen voor mijn app, aangezien ik rationele data gebruik.

### User stories

  - De gebruiker moet een duidelijk overzicht hebben van alle producten. Zodat hij gemakkelijk een product kan uitzoeken om zijn/haar les mee te vullen.
  - De gebruiker moet kunnen sorteren op id, rating, hoeveelheid. Zodat de gebruiker producten kan gebruiken die het beste bij zijn/haar les passen.
  - De gebruiker moet een product van tevoren kunnen reserveren. Zodat hij nooit mispakt op dit product.
  - De gebruiker moet een duidelijk overzicht hebben van zijn producten en wanneer hij/zij deze weer moet inleveren. Zodat hij/zij precies weet welk product hij/zij nog heeft en het product ook weer gereserveerd kan worden als hij/zij dit product niet meer.
  - De gebruiker moet kunnen aangeven of hij/zij het product heeft. Ook als hij/zij deze niet had gereserveerd. Zodat dit product nooit kwijtraakt.
  - Alleen gebruikers met de rol van ‘admin’ kunnen producten toevoegen. Zodat de database onder controle blijft.

### Leerdoelen

#### Web application
Ik heb voor mijn inividueel project een full stack webapp gemaakt. Voor de frontend heb ik gebruik gemaakt van Vue.js en voor de backend heb ik gebruik gemaakt van Java Spring. Voor de communicatie tussen de client en de server gebruik ik axios.
![image](https://user-images.githubusercontent.com/113592556/202159213-cdf4cafe-fc5f-46ef-8abe-a10606581785.png)

In de afbeelding kunt u zien dat ik gebruik maakt van een authorization header. Deze header is gevult met een bearer token. Door deze header moet er voordat het werkelijke request gerunt kan worden een preflight request gedaan worden. Hierdoor zien de communicatie er zo uit:
![image](https://user-images.githubusercontent.com/113592556/202164303-264ccd7b-bf6c-429a-8956-da0b1f07e553.png)


