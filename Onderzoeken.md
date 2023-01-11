# Wat is een goede manier om je applicatie te beveiligen?
Authenticatie en autorisatie is een van de belangrijkste processen in een full stack app. De authenticatie zorgt namelijk voor beveiliging en de autorisatie zorgt voor een rollensysteem. In dit onderzoek ga ik onderzoeken wat een goede manier is om mijn webapp te beveiligen en hoe ik dit moet maken. 

## Wat is authenticatie
Authenticatie is het mechanisme wat jouw inloggegevens herkend en linkt aan jouw persoonlijke informatie wat opgeslagen staat in een database. Deze inloggegevens bestaan meestal uit een gebruikersnaam en een wachtwoord. Dit hoeft niet altijd zo te zijn. Verschillende systemen kunnen verschillende inloggegevens hebben. Je kan deze opsplitsen in 5 verschillende categorieën:
-	Iets wat de gebruiker weet, bijvoorbeeld een wachtwoord.
-	Iets wat de gebruiker is, bijvoorbeeld een vingerafdruk.
-	Iets wat de gebruiker heeft, bijvoorbeeld een token zoals een bankpas.
-	Iets waar de gebruiker op een bepaalde tijd moet zijn, bijvoorbeeld alleen als de gebruiker op werk moet zijn volgens zijn agenda doet zijn keycard het.
-	Iets waar de gebruiker is, bijvoorbeeld alleen als de gps van je werktelefoon ziet dat je op je werk bent kan je het wachtwoord van je werktelefoon invullen.
Het authenticatie proces kan je opsplitsen in 2 delen: credential en authentication.
Het credential deel is het deel waarin het systeem vraagt om jouw inloggegevens en het authentication deel is het controleren van deze inloggegeven.

Bronnen: [techtarget](https://www.techtarget.com/searchsecurity/feature/5-common-authentication-factors-to-know)

## Soorten authenticatie
Er zijn 3 verschillende soorten authenticatie: Single-factor authentication, 2-factor authentication en multifactor authentication. 
Single factor authenticatie is een authenticatie waarin de gebruiker alleen zijn gebruikersnaam en wachtwoord hoeft in te vullen. Dit is genoeg voor het systeem om te weten welke data hij moet teruggeven. 
2-factor authenticatie is een authenticatie waarin ook de gebruikersnaam en wachtwoord wordt gevraagd, maar er wordt ook nog een bericht naar de gebruiker zijn mobile apparaat gestuurd.
Multifactor authenticatie is een authenticatie waarbij de gebruiker naast zijn gebruikersnaam en wachtwoord ook nog op een andere manier moet bewijzen dat hij geen hacker is. Een bekend voorbeeld hiervan is pinnen. Je moet je bankpas laten zien (Iets wat de gebruiker heeft) en je moet je pincode invullen (Iets wat de gebruiker weet). De laatste is hierdoor veiliger.

Bronnen: [delinea](https://delinea.com/blog/sfa-mfa-difference), [studiocdn](https://studiocdn.com/faq/what-is-two-factor-authentication/?gclid=Cj0KCQiA99ybBhD9ARIsALvZavVxycugjDb0dBqchP3yF4AOxEHdkS29I-0IGOrTqq1gKIzGSwC3Q6caAhZPEALw_wcB)

## Services
Het beveiligen van een app kan op veel verschillende manieren, zo worden er bijvoorbeeld verschillende services aangeboden zoals [Auth0](https://auth0.com/). Auth0 is een service die naast het inloggen ook het maken van SSO (Single Sign On) gemakkelijk maakt. Single Sign On is ook een manier van inloggen. Bij SSO kan je op verschillende platformen met hetzelfde account inloggen. SSO is zo gemakkelijk in Auth0 omdat Auth0 gebruik maakt van het [OpenID connect protocol](https://auth0.com/docs/authenticate/protocols/openid-connect-protocol).<br />
OpenID connect (OIDC) is een protocol wat het maken ven SSO gemakelijk maakt. Het Auth0 framework houdt zich vooral bezig met het inloggen van een gebruiker en OIDC met SSO. Omdat Auth0 OIDC gebruikt om SSO ook gemakkelijk te maken en is Auth0 een goede service om te gebruiken in uw applicatie.<br />
Naast Auth0 is ook [Amazon Cognito](https://aws.amazon.com/cognito/) een goede service. Ook Amazon Cognito maakt gebruik van het OIDC-protocol en dit maakt ook Amazon Cognitio goed voor SSO. Om te kiezen tussen Auth0 en Amazon Cognito is daarom ook lastig. Niet alleen voor SSO maar ook voor inlog services. Het grootste verschil is dat Amazon Cognito vaak duurder is als je de goede support wil voor OIDC.

Bronnen: [Auth0](https://auth0.com/), [OpenID Connect](https://auth0.com/docs/authenticate/protocols/openid-connect-protocol), [brocoders](https://brocoders.com/blog/auth0-vs-cognito/), [Amazon Cognito](https://aws.amazon.com/cognito/)

## Tokens
Het veilig maken van een authenticatie gebeurt meestal met tokens. De meest bekende tokens zijn: 
- JWT (JSON Web Token)
- Branca
- Fernet
- PASETO<br />

Hieronder ziet u de specificaties van alle bovenstaande tokens.
![image](https://user-images.githubusercontent.com/113592556/203552268-e82caf83-6ff4-43ce-ba7a-2ebcccc1e00f.png)<br />
<sub>Bron: [scottbrady91](https://www.scottbrady91.com/jose/alternatives-to-jwts#alternatives)</sub>

Bronnen: [scottbrady91](https://www.scottbrady91.com/jose/alternatives-to-jwts#alternatives)

## JWT
Ikzelf heb gekozen voor JWT-tokens. Een JWT-token is opgedeeld in 3 stukken: een header, een payload en een signature. Deze stukken worden opgesplitst doormiddel van punten. 

### Onderdelen van een JWT
De header bestaat meestal uit 2 delen. Dit is het type token en het signing algoritme. Het signing algoritme is het algoritme dat gebruikt gaat worden in het laatste deel van het token. Bekende voorbeelden van signing algoritmes zijn: HMAC SHA256 en RSA. Een header ziet er meestal zo uit:<br />
![image](https://user-images.githubusercontent.com/113592556/203557071-bee7e9d5-cc27-4291-ae52-5943c4b82c7b.png)<br />
<sub>Bron: [jwt.io](https://jwt.io/introduction)</sub>

De payload bestaat uit de verschillende claims. Deze claims kunnen worden opgesplitst in 3 types: registered, public, and private claims.
Registered claims zijn claims die niet verplicht zijn maar wel worden aangeraden. Dit zijn de claims zoals de issuer of de expiration time. Hieronder staat een foto van mijn eigen code met deze registered claims. <br />
![image](https://user-images.githubusercontent.com/113592556/203789125-26274f7a-ca8b-448e-bcf9-9f40858a0a40.png)<br />
<sub>Code snippet.</sub><br />

Het is ook mogelijk om public claims te gebruiken. Dit zijn claims die je zelf public kan maken. Om ervoor te zorgen dat alles goed verloopt zullen deze claims ergens opgeslagen moeten staan. De meest gebruikte lijst hiervoor is de [IANA JSON Web Token Claims Registry](https://www.iana.org/assignments/jwt/jwt.xhtml#claims). Deze lijst is gevuld met alle claims die je kan doen in een JWT-token.<br />
De laatste claim die je kunt uitvoeren zijn de private claims. Dit zijn claims die niet registered of public claims zijn. Het grootste verschil tussen een private en een public claim is dat er bij een private claim wel iets mis kan gaan. Daarom moeten deze altijd met beleid worden gebruikt.<br />

### Access token
Een access token is een JWT-token die gebruikt wordt om overal binnen te komen. Dit token wordt samen met een refresh token meegeleverd als de gebruiker zichzelf succesvol inlogt. Een access token wordt als een header in een request meegeleverd. Deze header is de AUTHENTICAION-header. Deze header wordt niet zomaar als '*authorized*' gezien. Dit houdt in dat deze header niet zomaar gebruikt kan worden. Dit komt omdat er voordat het echte request gedaan wordt, een preflight request gedaan wordt. Hierin wordt gekeken of alle headers authorized meegeleverd kunnen worden. Je moet dus in de backend handmatig zeggen dat de AUTHORIZATION header wel meegeleverd mag worden. Dit maakt deze header authorized Zodra de 
AUTHORIZATION-header als '*authorized*' wordt gezien kan een access token in deze header gezet worden. Dit gebeurt meestal door "Bearer " voor het token te zetten. Een access token ziet er als volgt uit: 
<br />
|![image](https://user-images.githubusercontent.com/113592556/203945493-06f92fae-2045-486c-8cf5-9aee9da51b34.png)|
|:--:|
<sub>Access token</sub>

Zoals je hierboven kunt zien wordt het token opgesplitst door punten. Het eerst deel is de header, het tweede deel is de payload en het derde deel is het signing algoritme. Zie <strong>[onderdelen van JWT](https://github.com/TijndeRooij/Portfolio/edit/main/Onderzoeken.md#onderdelen-van-een-jwt)</strong>.
Het doel van een access token is om de gebruiker zijn requests te laten doen. Zonder access token kan de gebruiker deze requests dus niet doen. Je krijgt een access token alleen als je bent ingelogd. Dit maakt je applicatie dus heel veilig.

### Refresh token
Een refresh token wordt samen met een access token meegeleverd als de gebruiker succesvol inlogt. Het doel van een refresh token is dat de gebruiker zonder opnieuw in te hoeven loggen een nieuwe access token kan krijgen. Om de applicatie nog veiliger te maken heeft een access token namelijk maar een bepaade tijd dat deze gebruikt kan worden. Als deze tijd afloopt kan een access token niet meer gebruikt worden. Zonder dat de gebruiker dit door heeft wordt er dan een refresh token naar de backend gestuurd. Deze refresh token laat de applicatie een nieuwe access token maken en deze wordt vervolgens weer gebruikt als normaal. Een refresh token kan ook aflopen na een bepaalde tijd. Als dit gebeurt moet de gebruiker wel opnieuw inloggen.

Bronnen: [jwt.io](https://jwt.io/introduction), [rfc-editor](https://www.rfc-editor.org/rfc/rfc7519#section-4.2), [iana](https://www.iana.org/assignments/jwt/jwt.xhtml#claims), [Amigoscode](https://youtu.be/VVn9OG9nfH0)

## Conclusie
In conclusie is het maken van een goede beveiliging voor uw applicatie geen gemakkelijke opgaven. Er zijn heel veel verschillende keuzes die de uitkomst drastisch kunnen veranderen. Ikzelf heb een authenticatie handmatig gemaakt met gebruik van JWT-tokens. Dit is heel leerzaam maar dit heeft mij wel heel veel werk gekost. Als je wat minder tijd hebt zou ik daarom kiezen om een service te gebruiken. Welke service ligt aan de applicatie die u maakt. Ikzelf zou voor Auth0 kiezen.<br />
Als u wel wat meer tijd hebt zou ik zelf een authenticatie proberen te maken. Dit zal uiteraard minder veilig zijn dan een service maar dit is wel heel leerzaam. Als token zou ik dan kiezen voor JWT-tokens.




# Hoe maak ik een goede UI/UX?
Een goede UI/UX zorgt zonder twijfel voor een betere applicatie. Als een gebruiker de app makkelijk kan gebruiken en hier maar weinig tot niks voor hoeft te leren zal de gebruiker vaker terug komen. Maar wat is nou een UI/UX? Wat is precies het verschil? En hoe maak je een goede UI/UX?

## Wat is UI/UX
UI en UX zijn 2 verschillende dingen die beiden te maken hebben met hoe een gebruiker om kan gaan met een applicatie. UI staat voor User interface 
