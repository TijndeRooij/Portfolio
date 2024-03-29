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

<details open>
  <summary>
    Web application
  </summary>

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
</details>

<details open>
  <summary>
    Software quality
  </summary>

### Software quality
Voor mijn individueel project heb ik gebruik gemaakt van End to End testing en SonarCloud om mijn code te testen en te analyseren. Ik heb heel lang geprobeerd Endpoint testen werkend te krijgen maar dit is mij uiteindelijk niet gelukt. 
  
#### Testing
Voor mijn tests heb ik gebruik gemaakt van End to End testing in Cypress. Dit is een goed programma voor End to End testen. Ik heb voordat ik begonnen was aan End to End testing heel lang geprobeerd Endpoint testing werkend te krijgen. Dit is mij niet gelukt. Ik heb deze Endpoint testen proberen te maken met Mockito en JUnit 5. Mockito is een handig framework voor het efficiënt schrijven van je tests en het mocken van de repo's.
``` java
@Test
public void getAllProductsEndPoint() throws Exception {
  String sorter = "id";

  when(productRepository.findAll()).thenReturn(Arrays.asList(Product_1, Product_2, Product_3));

  MvcResult mvcResult = mockMvc.perform(MockMvcRequestBuilders.get("/{sorter}", sorter))
              .andExpect(MockMvcResultMatchers.status().isOk())
              .andExpect(MockMvcResultMatchers.content().contentType(MediaType.APPLICATION_JSON))
              .andReturn();

  assertEquals(3, mvcResult.getResponse().getContentLength());
}
```
Hierboven staat een van mijn mislukte endpoint tests. Ik probeer hier het ophalen van alle producten te testen. Deze producten worden op hun 'id' gesorteerd en dat wordt teruggegeven aan de fontend.<br/>
Als eerste maakt ik een string aan met de waarde "id", dit is waar de service laag de opgehaalde producten op gaat sorteren.<br />
Vervolgens mock ik de Repository die de producten terug zou moeten geven. Ik mock dit zodat ik niet mijn echte database gebruik om de tests op uit te voeren. De 2e lijn zou zodra de findAll() method wordt aangeroepen een lijst van 3 predefinend producten moeten teruggeven.<br/>
Vervolgens ga ik mijn controller aanroepen. Dit doe ik door een request te maken naar '/{sorter}. Als ik dit heb gedaan check ik of de status 200 is, of ik JSON terugkrijg en of het response een lengte heeft van 3.<br/>
<br/>
Als ik de test op deze manier run krijg ik de volgende error.

> org.springframework.web.util.NestedServletException: Request processing failed; nested exception is java.lang.NullPointerException: Cannot invoke 
> "com.reserver.ProductReserver.API.Product.ProductService.sortProductList(String)" because "this.productService" is null

Ik heb verschillende dingen geprobeerd om deze error op te lossen. Zo heb ik geprobeerd mijn service laag te mocken, maar dit is natuurlijk niet de bedoeling omdat ik hier dan niet mee test wat ik wil testen. Ook heb ik geprobeerd hetzelfde te doen als een klasgenoot van mij. Hij roept voor het ophalen van alle producten niet de service laag aan. Hij heeft de repo.findAll() in zijn controller staan. Maar op deze manier heb ik niks aan mijn service laag, hierin sorteer ik namelijk alle producten. Dit is dus ook geen optie. Verder heb ik nog veel opgezocht over deze error, maar ik kwam er niet uit dus toen heb ik de keuze gemaakt om End to End testen te gaan maken in Cypress. <br/>
<br/>
ETE testing is mij wel gelukt. Met deze tests test ik niet alleen mijn backend maar ook mijn frontend. Omdat de frontend een connectie heeft mijn backend test ik hier ook mijn endpoints mee. Het nadeel van ETE testing is dat je jouw testen uitvoert op je eigen database.<br/>
Mijn ETE testen zien er als volgt uit.<br />
![image](https://user-images.githubusercontent.com/113592556/212326970-eea9f356-6660-42a8-8040-c67675c2c085.png)<br/>
Met deze test test ik mijn updatefunctie. Eerst moet ik inloggen om al mijn producten te zien. Met deze test test ik dus ook mijn inlogfunctie. Ook test ik met deze test mijn searchfunctie. Hierna kan ik pas beginnen aan het testen van mijn updatefunctie. Met een ETE test test ik dus veel meer dan oorspronkelijk mijn doel was.<br/>
Een ETE test werkt als volgt. Elk onderdeel in je frontend heeft een id. Met Cypress kan ik dit id aanroepen door cy.get('') te doen. Hierin zet ik mijn id en dan kan ik verschillende acties daarop uitvoeren. Een groot voordeel van Cypress is dat je vervolgens deze actie ook kan zien in hun webapplicatie. (Zie afbeelding hieronder)
![image](https://user-images.githubusercontent.com/113592556/212328915-fc8b9972-29b4-460b-98d1-bc6ba4ab4c65.png)
Iedere test kan je aanmaken in Cypress als spec en deze specs kun je programmeren in visual studio code.
  
#### Code analyse
Ook heb ik voor dit leerdoel mij code geanalyseerd moet sonarcloud. Dit is een programma wat code analyseert en de problemen in je code laat zien. Deze problemen zijn vaak problemen die je zelf niet zomaar ziet. Mijn sonarcloud ziet er als volgt uit:
![image](https://user-images.githubusercontent.com/113592556/212330053-f7d763b3-7a1f-49de-ba77-5b26e0e62f40.png) <br/>
Zoals je kan zien in de afbeelding heb ik 8 vulnerabilities. Ook heb ik 43 codesmells en 0 bugs. Het verschil is als volgt:
- Bug: Een fout in je code die naar een error kan lijden.
- Vulnerability: Een security issue wat open staat tot cyber aanval.
- Code Smell: Een onderhoudsprobleem wat kan lijden tot onduidelijkheid.

Ik heb sonarcloud ook in mijn CI-file gezet. Dit heb ik gedaan zodat er bij iedere push of pull een nieuwe analyse wordt gemaakt. Hierdoor weet ik meteen of er iets mis is met mijn code en hoe ik het moet veranderen. Dit deel in de CI-file ziet er als volgt uit: 
```yml
    - name: Cache SonarCloud packages
      uses: actions/cache@v1
      with:
        path: ~/.sonar/cache
        key: ${{ runner.os }}-sonar
        restore-keys: ${{ runner.os }}-sonar
    - name: Cache Maven packages
      uses: actions/cache@v1
      with:
        path: ~/.m2
        key: ${{ runner.os }}-m2-${{ hashFiles('**ProductReserver/pom.xml') }}
        restore-keys: ${{ runner.os }}-m2
    - name: Build and analyze
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}  # Needed to get PR information, if any
        SONAR_TOKEN: ${{ secrets.SONAR_TOKEN }}
      run: mvn -B verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=TijndeRooij_ProductReserver2 -f "ProductReserver/pom.xml" 
```
De eerste stap gebruikt de actie 'actions/cache@v1' om SonarCloud te cache. Deze cache gaat naar /.sonar/cache. Hetzelfde geld voor Maven. Alleen de maven cache gaat naar /.m2.<br />
Hierna wordt de code scan uitgevoerd in sonarcloud. Hiervoor heeft hij mijn pom-file nodig, vandaar de -f ProductReserver/pom.xml.

</details>  
  
<details open>
  <summary>
    CI/CD
  </summary>

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
  </details>
  
#### CI
Voor het onderdeel CI ben ik bezig geweest met github actions.
```yml
name: Java CI with Maven

on:
  push:
    branches: [ "master" ]
  pull_request:
    branches: [ "master" ]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - name: Checkout
      uses: actions/checkout@v3
      with:
        fetch-depth: 0  # Shallow clones should be disabled for a better relevancy of analysis
    - name: Set up JDK 17
      uses: actions/setup-java@v3
      with:
        java-version: '17'
        distribution: 'temurin'
        cache: maven
    - name: Cache SonarCloud packages
      uses: actions/cache@v1
      with:
        path: ~/.sonar/cache
        key: ${{ runner.os }}-sonar
        restore-keys: ${{ runner.os }}-sonar
    - name: Cache Maven packages
      uses: actions/cache@v1
      with:
        path: ~/.m2
        key: ${{ runner.os }}-m2-${{ hashFiles('**ProductReserver/pom.xml') }}
        restore-keys: ${{ runner.os }}-m2
    - name: Build and analyze
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}  # Needed to get PR information, if any
        SONAR_TOKEN: ${{ secrets.SONAR_TOKEN }}
      run: mvn -B verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=TijndeRooij_ProductReserver2 -f "ProductReserver/pom.xml" 
  
    - name: Build with Maven
      run: mvn -B package -f ProductReserver/pom.xml
    - name: Start containers
      run: docker-compose -f "ProductReserver/docker-compose.yml" up -d --build
```
De pijplijn wordt getriggerd door een push naar de master branch of een pull request naar de master branch. In de file wordt 1 job gerunt die uit een aantal stappen bestaat.
 - De stap "Checkout" gebruikt de actie actions/checkout@v3 om de code in de repository uit te checken. Door dit te doen wordt er uit gecheckt naar de default directory. Dit is "/". Om deze reden heb ik "ProductReserver/" voor iedere file staan die de job moet hebben. 
 - Nu komt er een groot deel wat te maken heeft met sonarCloud kijk bij code analyse.
 - De "Set up JDK 17" stap gebruikt de actions/setup-java@v3 actie om JDK versie 17 in te stellen, hij gebruikt temurin als distributie en maven als cache.
 - De "Build with Maven" stap voert het mvn commando uit om het project te bouwen met behulp van het ProductReserver/pom.xml bestand.
 - De stap "Start containers" start de container door het commando docker-compose -f "ProductReserver/docker-compose.yml" up -d --build uit te voeren. Deze runt de docker-composefile en hiermee ook de dockerfile.
</details>

<details open>
  <summary>
    Business processes
  </summary>
  
### Business processes
  
  
Ik heb 2 verschillende business processen gemaakt over het reserveren van een product zonder app en het reserveren van een product met app. Door ze lang elkaar te leggen kun je nu goed zien welke inpact mijn applicatie gaat hebben en ook of deze inpact het process juist handiger of moeilijker maakt.
<img src="https://user-images.githubusercontent.com/113592556/210853327-c34c9de4-4a04-4c2c-9710-69fe59636a62.png" /> <br/>
<img src="https://user-images.githubusercontent.com/113592556/210853742-91c1d289-6ee1-4273-87f0-4efcc3b4b4aa.png" />
<br/>
Zoals je nu kunt zien heeft het bovenste busniness process (het process zonder app) meer risk points, er kan dus vaker wat mis gaan. Zo zou een gebruiker bijvoorbeeld zijn naam kunnen vergeten op te schrijven als hij een product pakt. Dit zou een groot probleem kunnen veroorzaken in een later staduim. Mijn applicatie process (de onderste) heeft maar 1 risk point en dat is het terugbrengen van het product. Een gebruiker zou dit namelijk altijd kunnen vergeten. Maar deze kans is een stuk kleiner door de pushnotificatie die de gebruiker ook nog krijgt als hij op de inleverdatum het product nog bezit. <br/>
  <br/>
Door op deze manier naar de processen te kijken zie je dat de applicatie wel degelijk nut gaat hebben en hierdoor de moeite waart is om te maken.
</details>
