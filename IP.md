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
<img src="https://user-images.githubusercontent.com/113592556/210814218-5d0a45ec-74b0-470a-8dd6-aaf9b921b46a.png" height=300 align="right" />
Voor de frondend heb ik gekozen voor Vue.js. Omdat dit de eerste keer was dat een distributed system maakte wilde ik zoveel mogelijk manieren leren. Daarom heb ik niet gekozen voor React-native omdat we dat gebruikten in ons groepsproject. Omdat Vue.js HTML/CSS gebruikt kon ik ook gebruik maken van bootstrap. Dit schild mij veel werk en tijd en het ziet er prima uit voor de applicatie die ik van plan was te maken. Hierlangs staat een voorbeeld van een stukje code voor de homescreen.<br/>
Op het moment laat ik de database id nog in de frontend zien. Ik snap dat dit een security issue met zich mee brengt want een hacker kan nu zien dat hoeveel producten er allenmaal zijn. Hij kan namelijk bedenken dat als er een id van 14 is er ook een id van 13, 12 enzovoort moet zijn. Een oplossing hiervoor zou zijn om een string te gebruiken als id. Dit zou er zo uit kunnen zien: 3388a6f7-c090-44ba-b83c-9cb0ea1460f5.

#### Communicatie met backend
Ik heb voor mijn inividueel project een full stack webapp gemaakt. Voor de frontend heb ik gebruik gemaakt van Vue.js en voor de backend heb ik gebruik gemaakt van Java Spring. Ik heb in mijn individueel project wat minder de focus gelegt op het maken van een mooie frontend maar meer op het maken van een goed lopende backend. Voor de communicatie tussen de client en de server gebruik ik in mijn individueel project axios. <br />
![image](https://user-images.githubusercontent.com/113592556/202159213-cdf4cafe-fc5f-46ef-8abe-a10606581785.png)

In de afbeelding hierboven kunt u zien dat ik gebruik maakt van een authorization header. Deze header is gevult met een bearer token. Dankzij deze header moet er voordat het werkelijke request gerunt kan worden een preflight request gedaan worden. Hierdoor zien de communicatie er zo uit: <br />
<img src="https://user-images.githubusercontent.com/113592556/202164303-264ccd7b-bf6c-429a-8956-da0b1f07e553.png" width="200" height="300" />

#### Backend
Voor de backend van mijn individueel project heb ik gebruik gemaakt van Java Spring. Dit is een java framework wat het maken van webapplicatie makkelijker maakt. De opbouw van de backend is als volgt: 
  - Het request wat vanuit de frontend wordt verstuurd komt binnen in de Authorization filter. Hierin wordt het echte request onderscheiden van het prefligt request en de JWT token gedecrypt. Het wordt hier gecrypt omdat in deze classe ook de rollen uit het JWT token worden gehaald. Voor meer info over tokens en authorization zie het [onderzoek over inloggen](https://github.com/TijndeRooij/Portfolio/blob/main/Onderzoeken.md#wat-is-een-goede-manier-om-je-applicatie-te-beveiligen). Hieronder ziet u de Authorization filter: <br />
![image](https://user-images.githubusercontent.com/113592556/206147899-edb58aba-fa05-44ec-b88e-30ab0fa31f6d.png)
  - Na de Authorization filter gaat het request door naar de controllers. De controllers roepen de serviceclasses aan en die classes zorgen er samen met de models voor dat het correcte uit de database wordt gehaalt, toegevoegt, verandert of verwijdert. Vervolgens wordt dit weer naar de controllers verstuurd en die zorgen dat er bij een get request json formated producten worden terug gegeven en bij de andere requests een statuscode wordt meegegeven. Hieronder ziet u een foto van een put (update) en een get request: <br />
![image](https://user-images.githubusercontent.com/113592556/206152476-bfb5f025-f4f8-47c6-a0ca-6c70ab4f4b23.png)

#### Database
Voor de database in mijn individueel project heb ik gekozen voor een MYSQL database. Deze heb ik op phpmyadmin runnen. Ik run phpmyadmin zelf in docker:<br />
![image](https://user-images.githubusercontent.com/113592556/206154659-09e5f0f5-93b9-442e-b005-4ddd63e51272.png)
In mijn database staan mijn users, products en rollen opgeslagen. Tussen Users en Rollen zit een koppeltabel die bijhoud welke rollen een user heeft. In mijn user tabel staat ook het password opgeslagen. Deze staat encrypted in de database.

### Software quality
You use software tooling and methodology that continuously monitors and improve the software quality during software development.

Clarification:
Tooling and methodology: Carry out, monitor and report on unit integration, regression and system tests, with attention for security and performance aspects, as well as applying static code analysis and code reviews.

### CI/CD

#### CD
Ik heb in mijn Intellij project een dockerfile en een dockercompose file gemaakt. De dockerfile is verantwoordelijk voor het opbouwen van de docker image. Deze image wordt gerunt in een container. In mijn dockercompose file worden alle images aangemaakt. Dit zijn er meerdere. Ik run namelijk ook mijn SQL en PHPMYADMIN in docker. Ik heb hiervoor gekozen omdat ik dacht dat ze op deze manier makkelijker met elkaar konden communiceren. <br />
Mijn Dockerfile ziet er zo uit: <br />
<details open>
  <summary>
    dockerfile
  </summary>
  
``` dockerfile
FROM eclipse-temurin:11-jdk-jammy

WORKDIR /app

COPY .mvn/ .mvn
COPY mvnw pom.xml ./
COPY src ./src

EXPOSE 6000

CMD ["./mvnw", "spring-boot:run"]
```
</details>
In mijn dockerfile stel ik eerst een werkmap in voor de rest van de opdrachten in de dockerfile. Deze komt op de locatie /app. 
Vervolgens kopiëer ik de bestanden 'mvnw, .mvn, pom.xml' van mijn computer naar de container. 
Dan maak ik een nieuwe map aan op /opt/app.
Dan stel ik de poort 6000 bloot aan de container.
Als laaste vertel ik het script mvnw om de opdracht 'spring-boot:run' te runnen zodra de container gestart wordt. Dit laatste runt de applicatie

En mijn dockercomposefile ziet er zo uit:
<details open>
  <summary>
    dockercompose file
  </summary>

``` yml
version: '3.3'

services:
  #service 1: definition of mysql database
  db:
    image: mysql:latest
    container_name: mysql-2
    networks:
      - productreserver-mysql
    environment:
      MYSQL_ALLOW_EMPTY_PASSWORD: 1
      MYSQL_DATABASE: productreserver
    ports:
      - "3306:3306"
    restart: "no"



  #service 2: definition of phpMyAdmin
  phpmyadmin:
    image: phpmyadmin/phpmyadmin:latest
    container_name: my-php-myadmin
    ports:
      - "8082:80"
    restart: "no"
    networks:
      - productreserver-mysql
    depends_on:
      - db
    environment:
      SPRING_DATASOURCE_USERNAME: root
      SPRING_DATASOURCE_PASSWORD: ""



  #service 3: definition of your spring-boot app
  productreserver:                        #it is just a name, which will be used only in this file.
    image: springio/gs-spring-boot-docker #name of the image after dockerfile executes
    container_name: product-reserver-app  #name of the container created from docker image
    networks:
      - productreserver-mysql
    depends_on: #define dependencies of this app
      - db
    build:
      context: .                          #docker file path (. means root directory)
      dockerfile: Dockerfile              #docker file name
    ports:
      - "5000:6000"                       #docker containter port with your os port
    restart: "no"
    environment:
      SPRING_DATASOURCE_URL: jdbc:mysql://db:3306/productreserver?createDatabaseIfNotExist=true
      SPRING_DATASOURCE_USERNAME: root
      SPRING_DATASOURCE_PASSWORD: ""                            #dependency name (which is defined with this name 'db' in this file earlier)

networks:
  productreserver-mysql:
```
</details

You design and implement a (semi)automated software release process that matches the needs of the project context.

Clarification:
Design and implement: You design a release process and implement a continuous integration and deployment solution (using e.g. Gitlab CI and Docker).

### Business processes
You analyze and describe simple business processes that are related to your project.

Clarification:
Simple: Involving stakeholders, predominantly sequential processes with one or two alternative paths.

Related: Business processes during which the software that you are developing will be used (business processes that the software must support by fully or partially automating them). 

or

Business processes needed for the success of your software development project (e.g., product release, market release, financial assurance).


