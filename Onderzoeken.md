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
2-factor authenticatie is een authenticatie waarin ook de gebruikersnaam en wachtwoord wordt gevraagt, maar er wordt ook nog een bericht naar de gebruiker zijn mobile apparaat gestuurd.
Multifactor authenticatie is een authenticatie waarbij de gebruiker naast zijn gebruikersnaam en wachtwoord ook nog op een andere manier moet bewijzen dat hij geen hacker is. Een bekend voorbeeld hiervan is pinnen. Je moet je bankpas laten zien (Iets wat de gebruiker heeft) en je moet je pincode invullen (Iets wat de gebruiker weet). De laatste is hierdoor veiliger.

Bronnen: [delinea](https://delinea.com/blog/sfa-mfa-difference), [studiocdn](https://studiocdn.com/faq/what-is-two-factor-authentication/?gclid=Cj0KCQiA99ybBhD9ARIsALvZavVxycugjDb0dBqchP3yF4AOxEHdkS29I-0IGOrTqq1gKIzGSwC3Q6caAhZPEALw_wcB)

## Hoe werkt het?
Het beveiligen van een app kan op veel verschillende manieren, zo worden er bijvoorbeeld verschillende services aangeboden zoals [Auth0](https://auth0.com/). Auth0 is een service die het maken van SSO (Single Sign On) gemakkelijk maakt. Single Sign On is ook een manier van inloggen. Bij SSO kan je op verschillende platformen met hetzelfde account inloggen, een voorbeeld hiervan is als je langs de inlogkeuzes ook nog de keuze hebt om met google in te loggen. Als je dit doet maak je gebruik van je google account en dus van SSO.

Bronnen: [Auth0](https://auth0.com/)

## Tokens
Het veilig maken van een authenticatie gebeurt meestal met tokens. De meest bekende tokens zijn: 
- JWT (JSON Web Token)
- Branca
- Fernet
- PASETO
Hieronder ziet u de specificaties van alle bovenstaande tokens.
![image](https://user-images.githubusercontent.com/113592556/203552268-e82caf83-6ff4-43ce-ba7a-2ebcccc1e00f.png)<br />
<sub>Source: [scottbrady91](https://www.scottbrady91.com/jose/alternatives-to-jwts#alternatives)</sub>

Bronnen: [scottbrady91](https://www.scottbrady91.com/jose/alternatives-to-jwts#alternatives)

## JWT
Ikzelf heb gekozen voor JWT tokens. 
