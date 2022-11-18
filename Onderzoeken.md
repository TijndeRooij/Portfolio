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

Er zijn 2 verschillende soorten authenticatie: Single-factor authentication en multifactor authentication. 
Single factor authenticatie is een authenticatie waarin de gebruiker alleen zijn gebruikersnaam en wachtwoord hoeft in te vullen. Dit is genoeg voor het systeem om te weten welke data hij moet teruggeven. Multifactor authenticatie is een authenticatie waarbij de gebruiker naast zijn gebruikersnaam en wachtwoord ook nog op een andere manier moet bewijzen dat hij geen hacker is. Een bekend voorbeeld hiervan is pinnen. Je moet je bankpas laten zien (Iets wat de gebruiker heeft) en je moet je pincode invullen (Iets wat de gebruiker weet). De laatste is hierdoor veiliger.  

## Authenticatie server
Een authenticatie server is een applicatie die ervoor zorgt dat de authenticatie van een gebruiker goed verloopt. Er zijn verschillende authenticatie protocollen. Bijvoorbeeld RADIUS, TACACS+, Active Directory, Lightweight Directory Access protocol, Secure Sockets Layer en Transport Layer Security. RADIUS is een van de meest gebruikte authenticatie methodes. TACACS+ lijkt heel erg op RADIUS maar gebruikt TCP en RADIUS gebruikt UDP. 
TCP en UDP zijn beide een set regels die aangeven hoe data wordt doorgegeven over het internet.
Alle verschillen staan in de afbeelding hieronder.

![image](https://user-images.githubusercontent.com/113592556/202681773-9750fe11-b383-46d3-8081-ddd9f5a97d4a.png)

Zoals je hierlangs ziet is het gebruik van UDP niet handig voor een authenticatie. Die komt omdat UDP niet betrouwbaar genoeg is. Het kan namelijk zijn dat UDP data verliest en dat kan natuurlijk niet als het gaat om inloggegevens. TCP gebuikt SSL en TLS als beveiliging. UDP kan TLS niet gebruiken omdat TLS niet kan werken als er een verlies is in data.

