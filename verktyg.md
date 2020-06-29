---
layout: default
---
# Var ingår?
Nedan försöker vi övergripande ge en bild över vad som ingår för de som avropar tjänsten eKlient från Inera.  

## Våra verktyg

### Sysman
​SysMan är en webbaserad portal för alla som arbetar med Klienthantering, syftet med SysMan är att erbjuda ett snabbt och lätt använt webgränsnitt samt lösa en del av de saker i Configuration Manger som kräver mycket jobb för att uppnå som exempelvis schemaläggning av en applikationsinsstallation eller ominstallation av en dator. SysMan består av ett webbgränssnitt och service som utför det som man gör/beställer i webportalen.​

<img src="/eklient/sysman1.png" width="500">

### ePaket
ePaket används för att hantera processen från beställning av paketering tills dess att paketet är i produktion. ePaket hanterar alla steg i processen:

* Beställning
* Paketering
* QA (kvalitetssäkring)
* Acceptanstest
* Distribution
* Drift
* Verktyget hanterar all information om paketet och hanterar även en applikations väg från beställning till distribution.

### Overview
Problemställningen att Windows 7 behöver bytas ut, eller att vi nu ser nya releaser av Windows 10 var 6:e månad är det som vi ämnar lösa med Overview och livscykelprocessen för Operativsystem.
Kortfattat så det huvudsakliga syftet med Overview:
* Förse IT med information så att byte till Windows 10 kan genomföras i ordinarie drift
* Automatisera och delegera införandet av Windows 10 till användare genom att förse dessa med information inför OS byte

Overview är ett verktyg som stödjer processen för att införa och förvalta Windows as a Service (Windows 10). Overview bygger på livscykelprocessen för operativsystem. Med hjälp av Overview kan alla faser i förvaltningen och release av nya versioner av Windows 10 hanteras. Verktyget hanterar:

* Infrastrukturverifiering
* Systemverifiering
* Verksamhetsverifiering
* Införande
* Städning

<img src="/eklient/overview1.png" width="300">
<img src="/eklient/overview2.png" width="300">
<img src="/eklient/overview3.png" width="300">
<img src="/eklient/overview4.png" width="300">

### DriftInformation
Driftinformation togs ursprungligen fram för att ersätta Active Desktop i Windows 7. Driftinformation kan visa ett RSS flöde med information, telefonnummer till ServiceDesk men även mer tekniska detaljer som inloggad användare, IP-Adress, Mac-Adress, upptid med mera. 

Den integrerar med skrivbordet och lägger sig längst upp. Driftinformation kan sedan version 4 även visa medelande samt "enkäter" som syns på bilden bredvid. Det går att utöka vad den visar under "Information" genom att skapa nycklar i registret på datorerna det står beskrivet i dokumentationen nedan.

<img src="/eklient/driftinfo1.png" width="300">
<img src="/eklient/driftinfo2.png" width="300">

### WrapperKing
Wrapperking är ett verktyg för att skapa en .xml film som kan användas av Installking.exe som är den fil som faktiskt gör installationen på en klient. Syftet med wrapperking är att fylla de hål i funktionailiet som finns i Configuration Manager

<img src="/eklient/wrapperking1.png" width="300">

### DriverKing
Driverking är ett verktyg som underlättar hanteringen av drivrutinspaket samt deras applikationer i Configuration Manager. Driverking möljliggör öven delning av drivrutinspaket samt tillhörande program mellan medlemmarna i eKlient

<img src="/eklient/driverking1.png" width="300">

### DeployKing
Deployking används för att importera applikationer till SysMan, Configuration Manager och skapa alla de objekt som behövs. Deployking kan läsa in information ifrån App-v, MSI samt Wrapperking applikationer. Det går även att lägga till andra installationer exempelvis .exe filer då måste dock detection metod skapas manuellt med registrernycklar det kan vi inte läsa in. Genom att använda Deployking kan vi säkerställa att namnstandard efterföljs och minimera risken för misstag.

När applikationen skapas skapar Deployking följande:

* ​Applikation i Configuration Manager
* AD Grupper
* Collectioner med Queries till AD Grupperna.
* Deployments
* Distribuerar innehållet till DP
* Skapar en Applikation/System i SysMan

<img src="/eklient/deployking1.png" width="300">

### TSLaunch
TSlaunch är ett av flera verktyg som vi tagit fram för att förenkla och förbättra uppgraderingen av Windows 7 - Windows 10 samt Windows 10 - Windows 10. Med TSLaunch kan vi göra tester innan användaren störs, kontrollera att nät finns, VPN samt att en Testuppgradering av datorn genomförs med lyckat resultat och mycket mer än så. 

Eftersom vi gör testuppgraderingen innan vi stör användaren kan vi rapportera tillbaka eventuella problem som skulle stoppat uppgraderingen och stört användaren innan detta sker. 

En annan liten binär som används är UPGBackground som gör det möjligt att visa en bild för användaren under uppgraderingen samt blockera inloggning efter omstart av datorn under uppgraderingen, även detta för att hjälpa användarna och minimera påverkan och missnöje.

<img src="/eklient/tslaunch1.png" width="300">

### Automation
Syftet med området beställningsautomation är att förse eKlients medlemmar med ett automation från vilken användaren i ett beställningsgränssnitt kan beställa IT resurser och att dessa kan levereras automatiskt. I de processer som levereras finns exempelvis hantering av godkännande och integration mot eKlients och medlemmens system. Området kan leverera på två nivåer, dels som en ren automationslösning som tar emot beställningar från ett externt system (exempelvis en tjänstekatalog), dels i samverkan med medlemmens leverantör som en komplett portal som inkluderar ett användargränssnitt. Exempel på beställningar som automatiserats är:

* Beställning/avbeställning applikationer
* Beställning/avbeställning av datorer
* Beställning och hantering av resurser (mappar, distributionslistor, sharepointsiter, grupper)
* Beställning av övriga resurser som konton, SSO, 802.1x, Pushmail, VPN, VDI m.m.

### Självbetjäning
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean consequat hendrerit metus feugiat faucibus. Phasellus varius augue at mauris sollicitudin, eu maximus nunc convallis. Praesent imperdiet urna vitae nisi dapibus, non dictum purus elementum. Vivamus elementum dolor magna, at tincidunt nulla malesuada vitae. Praesent pellentesque pellentesque est. Aenean eget accumsan magna, ac blandit ligula. Vivamus bibendum rutrum mauris eget aliquam. Duis imperdiet nibh eu tristique auctor. Pellentesque dapibus consequat risus, et iaculis eros fermentum eget. Curabitur odio diam, imperdiet vel augue sed, efficitur dapibus nunc. Ut lacus mauris, rutrum non consequat eget, sollicitudin a tellus. Fusce sit amet ante nulla. Praesent condimentum nec arcu at eleifend. Nulla consequat tristique ipsum eget aliquam. Quisque sed purus posuere, feugiat diam in, pulvinar est. Ut mi nunc, fringilla sit amet blandit id, tempus ac massa.

## Guider
Utöver alla våra verkyg så tillhandahåller vi även guider och instruktioner för våra medlemmar för hur man konfigurerar och underhåller viktiga delar av den infrastruktur som krävs för att tillhandahålla en säker och effektiv IT-arbetsplats.

Nedan följer några exempel på dokument vi tillhandahåller:

* xxxxx
* xxxxx
* xxxxx
* xxxxx
