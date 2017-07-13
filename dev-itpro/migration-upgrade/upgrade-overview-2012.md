---
title: "Päivitä Dynamics AX 2012 Dynamics 365 for Finance and Operations Enterprise edition -versioon"
description: "Tässä ohjeaiheessa käsitellään prosessia, jolla Microsoft Dynamics AX 2012:a käyttävät asiakkaat voivat siirtää tietoja ja koodia Microsoft Dynamics 365 for Finance and Operations Enterprise Editioniin."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 13507fcf9c0d626709aeb4e00a8632411204c20f
ms.contentlocale: fi-fi
ms.lasthandoff: 06/15/2017

---

# Päivitä Microsoft Dynamics AX 2012 Microsoft Dynamics 365 for Finance and Operations Enterprise edition -versioon
<a id="upgrade-microsoft-dynamics-ax-2012-to-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations, Enterprise edition -ympäristön päivitys 8 sisältää päivityspolun jonka avulla asiakkaat, jotka nykyisin käyttävät Microsoft Dynamics AX 2012:a, voivat siirtää tietoja ja koodia Finance and Operations -palveluun. Päivitysprosessi perustuu seuraaviin elementteihin:

- Työkalut, joilla avulla voit siirtää nykyisen mukautetun sovelluksen koodin AX 2012:sta.
- Tietojen päivitysprosessi, jonka avulla voit siirtää tietokantasi. Tämän vuoksi voit päivittää täydellisen tapahtumahistorian.

## Yleiskuvaus
<a id="overview" class="xliff"></a>

Koko päivitysprosessi voidaan visualisoida kolmessa ylätason vaiheessa: analyysi, suoritus ja vahvistus.

Seuraavassa kaaviossa esitetään koko päivitysprosessi ja tehtävät, joita pidetään kunkin vaiheen osana. 

![Päivitysprosessi](./media/upgrade-process.png)

## Analysoi
<a id="analyze" class="xliff"></a>

Analyysivaiheen tehtävien avulla voidaan arvioida työ, jota päivitystä edellyttää. Niiden avulla voit myös laatia projektisuunnitelman. Nämä toimet voidaan tehdä ennen Finance and Operations -palvelun ostamista. Niiden avulla voit tehdä asiantuntevan ostopäätöksen, antamalla arvopisteet tarvittavista työstä ja resursseista.

### Rekisteröityminen julkiseen esikatseluun LCS:ssä
<a id="sign-up-for-a-public-preview-in-lcs" class="xliff"></a>

Jotta voit analysoida toiminnot ennen Finance and Operations -palvelun ostamista, voit rekisteröityä julkista esikatselua varten. Julkisen esikatselun avulla voit ottaa käyttöön oman Finance and Operations -ympäristön. Saat myös käyttöoikeudet Microsoft Dynamics Lifecycle Services (LCS) -työkaluihin, joiden avulla arvioidaan AX 2012-ympäristöäsi ja nykyistä mukautettua koodia.

Jos sinulla on valmis LCS-projekti AX 2012:ssa, sinun on kuitenkin kirjauduttava uuteen lisäprojektiin Finance and Operations -arviointia varten.

Lisätietoja julkisesta esikatselusta asiakkaille on sivulla https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Lisätietoja julkisesta esikatselusta partnereille on sivulla https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Huomaa, että yleinen esikatselu eroaa [30 päivän kokeiluversion](https://aka.ms/D365OperationTrials). Kolmenkymmenen päivän kokeiluversion avulla saat käyttöön Finance and Operations -esiintymän, jonka avulla voit tutkia ja arvioida sovellusta. Analysointitoiminto edellyttää kuitenkin täydellisiä LCS-sisältöä ja -työkaluja.

### Valitse päivitysmenetelmä
<a id="select-the-upgrade-methodology" class="xliff"></a>
Määritä uuden LCS-projektin menetelmäksi **AX 2012:n päivittäminen Dynamics 365 for Operationsiin**. Tämä menetelmä on tehty erityisesti AX 2012 -asiakkaille päivitystä varten. Siinä kuvataan yksityiskohtaisesti kolme vaihetta ja annetaan linkkejä prosessin tukidokumentaatioon.

![Päivitysmenetelmä(./media/methodology.png)
 
### Päivitysanalyysin suorittaminen
<a id="run-the-upgrade-analyzer" class="xliff"></a>
Päivitysanalyysityökalu suoritetaan AX 2012-ympäristössä ja se määrittää tehtäviä, jotka tulisi tehdä AX 2012-ympäristön valmistelemiseksi, jotta päivitys on mahdollisimman sujuva ja kustannukset mahdollisimman vähäiset:

- **Tietojen tyhjennys** – Prosessin avulla voit tunnistaa tiedot, jotka voi poistaa menettämättä toimintoja. Työkalu tunnistaa tietotyypit, joita voidaan vähentää puhdistusprosessin avulla. Jokaisen tietotyypin osalta annetaan selitys puhdistuksen vaikutuksista. Sen jälkeen päätät, suoritetaanko puhdistusprosessi. Osa Finance and Operations -tilauksen kustannuksista perustuu tietokannan kokoon. Pienentämällä kokoa voit pienentää tilauksen kustannuksia ja aikaa, joka vaaditaan päivityksen käyttöönotolta. Pienempi tietokanta takaa nopeamman päivityksen.
- **SQL-konfiguraatio** – Prosessi tarkistaa SQL-konfiguraation ja suosittelee optimointia. Varmistamalla, että SQL toimii optimaalisesti, tämä prosessi auttaa vähentämään aikaa, joka vaaditaan päivityksen käyttöönottoprosessilta.
- **Vanhentuneet ominaisuudet** – Prosessi tunnistaa toiminnot, joita parhaillaan käytät mutta jotka eivät ole käytettävissä Finance and Operations -palvelussa. Prosessi auttaa löytämään varhaisessa vaiheessa puutteet toiminnoissa. Se ehdottaa myös vaihtoehtoja.

Lisäksi tässä vaiheessa on asennettava KBXXXXXXX AX 2012 -ympäristössä. Tämä Hotfix-korjaus sisältää päivitystä edeltävän tarkistusluettelon. AX 2012 -ympäristössä voit antaa päivitysprosessin tarvitsemat tiedot tämän tarkistusluettelon avulla. Esimerkiksi yhdessä päivitystä edeltävän tarkistusluettelon tehtävässä annat kunkin AX 2012:n nykyisen käyttäjän Microsoft Azure Active Directory (Azure AD) -kirjautumistiedot, jotta kukin käyttäjä voi kirjautua Finance and Operations -palveluun.

Tämän vaiheen tuotoksesta tulee päivitysprojektisuunnitelman työnkulku AX 2012-järjestelmänvalvojille.

Lisätietoja on kohdassa [Analysointi – päivityksen suunnittelu päivitysanalyysin työkalulla](upgrade-analyzer-tool.md).

### Koodin päivityksen arviointityökalujen suorittaminen
<a id="run-the-code-upgrade-estimation-tools" class="xliff"></a>
Tämä vaihe muuntaa koodisi AX 2012:sta uuteen muotoon ja antaa palautetta ristiriidoista, jotka kehittäjän on ratkaistava myöhemmin. Tämä vaihe muodostaa perustan koodipäivityksen kustannusarviolle.

Tämän vaiheen suorittamiseksi sinun on vietävä koodisi AX 2012:sta mallisäiliönä ja ladattava se LCS-koodin päivitystyökaluun. Koodin päivitystyökalu tuottaa päivitetyn version koodistasi ja raportin ratkaistavista ristiriidoista. Järjestelmäkehittäjäsi voi tämän jälkeen tarkastaa päivitetyn koodin ja raportin ja määrittää, mitä koodikannan päivitys vielä edellyttää.

Tämän vaiheen tuotoksesta tulee päivitysprojektisuunnitelman työnkulku Microsoft Dynamics AX -kehittäjille.

Lisätietoja on kohdassa [Analysointi: koodin päivitykseen tarvittavan työmäärän arviointi](analyze-code-upgrade.md).

### Esittely-ympäristön käyttöönotto
<a id="deploy-a-demo-environment" class="xliff"></a>
Esittely-ympäristöt ovat oletusympäristöjä, jotka sisältävät esimerkkitietoja (ei yrityksesi tietoja) ja vakiokoodin (ei mukautuksia). Suosittelemme, että otat esittely-ympäristön käyttöön ja arvioit uudet ominaisuudet sekä suoritat soveltuvuuden perussopivuus- ja aukkoanalyysin AX 2012:ssa käytettäville vakioprosesseille, jotka ovat voineet muuttua Finance and Operations -palvelussa. Voit ottaa nämä esittely-ympäristöt käyttöön Azuressa tai ladata ne virtuaalikoneena (VM), joka suoritetaan omalla laitteellasi. Jos otat ne käyttöön Azuressa, sinun on annettava Azure tilauksen tiedot, koska julkinen esikatseluprojekti on yhä käytössäsi etkä vielä ei ole hankkinut Finance and Operations -tilausta.

Tämän vaiheen tuotoksesta tulee päivitysprojektisuunnitelman työnkulku toimintokäyttäjille tai yrityskäyttäjille.

Lisätietoja on kohdassa [Analysointi – eristysympäristön käyttöönotto](analysis-sandbox.md)

### Projektisuunnitelman luominen
<a id="create-a-project-plan" class="xliff"></a>
Päivitysmenetelmä sisältää projektisuunnitelman mallin. Tässä vaiheessa analyysivaiheen edellisten vaiheiden tuotosta käytetään täydentämään päivitysprojektin projektisuunnitelmaa. Projektisuunnitelma sisältää myös kaikki testaustiedot: tietopäivityksen testauksen, valmistelusiirron testauksen, toimintotestijakson toistojen ja kyseisten tehtävien resurssien määritykseen liittyviä tietoja.

Tässä vaiheessa projektisuunnitelma antaa arvopisteen, jonka avulla voit selvittää Finance and Operations -päivityksen edellyttämät kustannukset ja ajan.

## Suorita
<a id="execute" class="xliff"></a>
Suoritusvaiheessa käyt läpi tehtäviä, jotka suunnittelit analyysivaiheessa. Siirtyäksesi suoritusvaiheeseen sinun pitää ostaa Finance and Operations ja sinulla on oltava tarvittavat resurssit päivityksen suorittamiseksi.

### LCS-käyttöönottoprojektiin siirtyminen
<a id="switch-to-the-lcs-implementation-project" class="xliff"></a>
Analyysivaiheessa käytetty julkinen esikatseluprojekti on täyttänyt tarkoituksensa. Voit nyt poistaa sen. Jäljellä olevissa vaiheissa tarvitset vain projektisuunnitelman, jonka loit analyysivaiheen viimeisessä vaiheessa.

Kun ostat Finance and Operations -tilauksen, saat tarkat tiedot uuteen LCS-projektiin kirjautumista varten. Tätä projektia sanotaan käyttöönottoprojektiksi ja siitä tulee tilauksesi ajan kestävä uusi pysyvä LCS-projekti. Projekti poikkeaa julkisesta esikatseluprojektista siten, että se on Microsoftin ylläpitämä. Projektin ominaisuudet:

- Kaikkia projektin ympäristöjä isännöidään Azuressa.
- Microsoft hallinnoi projektiin liittyvää Azure-tilausta. Siksi Azure-kustannuksia ei laskuteta erikseen. Kustannukset sisältyvät Finance and Operations -tilaukseen.
- Microsoftin ylläpitää projektin tuotantoympäristöä. Siksi Microsoft suorittaa koodin käyttöönotot, päivitykset ja infrastruktuurin ylläpidon, eivätkä työntekijäsi. 

### AX 2012:n valmistelutoimien suorittaminen
<a id="perform-the-ax-2012-preparation-tasks" class="xliff"></a>
Suorita tehtävät, jotka päivityksen analysointityökalu havaitsi ja jotka on dokumentoitu päivitysprojektisuunnitelmaan. Microsoft Dynamics AX-järjestelmänvalvojan ja tietokannan järjestelmänvalvojan (DBA) on suoritettava nämä tehtävät.

[Tietojen päivitys AX 2012:sta Dynamics 365 for Operations -palveluun – AX 2012:n päivitystä edeltävä tarkistusluettelo](prepare-data-upgrade.md)

### Koodipäivityksen suorittaminen
<a id="perform-code-upgrade" class="xliff"></a>
Suorittaa tehtävät, jotka on suunniteltu koodin päivityksen arviointivaiheessa analysointivaiheen yhteydessä. Järjestelmäkehittäjiesi on suoritettava nämä tehtävät.

AX 2012:n koodimuutokset pitää lukita tästä alkaen. AX 2012:n kokodimuutokset on sallittu ainoastaan hätätapauksessa. Jos koodia muutetaan, se on siirrettävä manuaalisesti uuteen koodikantaan.

### Uuden koodin kehittäminen
<a id="develop-new-code" class="xliff"></a>
Tee analyysivaiheen "Esittely-ympäristön käyttöönotto”-vaiheessa tehdyn osaamisalueaukkojen analyysin tehtävät. Näihin tehtäviin kuuluu todennäköisesti sekä toimintatehtäviä, jotka määrittävät konfiguraation, ja mukautuksen kehitystehtäviä, jotka liittyvät uusiin toteutettaviin ominaisuuksiin.

### Tietojen päivittäminen (kehitysympäristö)
<a id="data-upgrade-development-environment" class="xliff"></a>
Jälkeen koodin päivitystehtävät on suoritettu, voit päivittää AX 2012:n tietokannat Finance and Operations -palveluun ensimmäistä kertaa. Ensimmäinen päivitys tapahtuu kehitysympäristössä, jotta voit helposti korjata tässä vaiheessa syntyneet ongelmat ja viat. Kehitysympäristössä virheet voidaan korjata heti, koodi voidaan oikaista ja päivitys voidaan suorittaa uudelleen muutaman minuutin kuluessa. Suuremmat eristysympäristöt ei tarjoa tätä joustavuutta ja tarvitaan vähintään useita tunteja virheenkorjausta, koodin päivitystä, päivitetyn koodin käyttöönottoa ja päivityksen uudelleen suorittamista varten.

Prosessi on esitetty seuraavassa kuvassa. Varmuuskopioi AX 2012:n tietokanta, lataa se Azureen, palauta se Finance and Operations ‑ympäristöön ja suorita tietojen päivitys.

![Tietojen päivitys kehitysympäristössä](./media/data-upgrade-dev.png)
 
Tietojen päivitys tapahtuu erityisen käyttöönottopaketin avulla. Samaa mekanismia käytetään uuden Finance and Operations -koodin käyttöönottoon yhdestä ympäristöstä toiseen.

Tämän prosessin aikana muunnettavien tietokannan tietojen kehikko on suurelta osin sama, mitä käytetään AX 2012:n päivityskehikkona, joka perustuu **ReleaseUpdatexxx**-luokat suorittaviin X++ -erätöihin.

Lisätietoja [Tietojen päivitys AX 2012:sta Dynamics 365 for Operationsiin kehitysympäristössä](data-upgrade-2012.md).

### Tietojen päivitys (eristysympäristö)
<a id="data-upgrade-sandbox-environments" class="xliff"></a>
Kun tietojen päivitys kehitysympäristössä on valmis, sama prosessi voidaan tehdä eristysympäristössä. Eristysympäristössä yrityskäyttäjät ja toimintotiimin jäsenet voivat testata liiketoimintaprosesseja käyttämällä päivitettyjä AX 2012 -tietoja ja -koodia.

Seuraavassa kuvassa on esitetty prosessi tietojen päivityksen suorittamiseksi eristetyssä ympäristössä. Erona on se, että bacpac-työkalua käytetään perinteisen SQL-varmuuskopion sijaan. Työkalua tarvitaan Microsoft SQL Serverin ja Azuren SQL-tietokannan väliseen muunnokseen. Tämä ei ole Finance and Operations -erityistyökalu vaan SQL-vakiotyökalu.

![Tietojen päivitys eristysympäristössä](./media/data-upgrade-sandbox.png)

Lisätietoja on kohdassa [Tietojen päivitys AX 2012:sta Dynamics 365 for Operationsiin kehitysympäristössä](upgrade-data-sandbox.md).
 
## Tarkista
<a id="validate" class="xliff"></a>
Kun siirryt Vahvista-vaiheeseen, käytettävissäsi olevat ympäristöt sisältävät päivitetyn mukautetun koodisi ja päivitetyt tietosi. Tässä vaiheessa kuvataan ympäristön toimivuuden tarkistus- ja testausprosessia. Siinä kuvataan myös käyttöönoton valmisteluprosessia.

### Valmistelusiirron testaus ja valmistelusiirtosuunnitelman laatiminen
<a id="perform-cutover-testing-and-create-a-cutover-plan" class="xliff"></a>
_Valmistelusiirto_-termi tarkoittaa tässä yhteydessä uuden järjestelmän käyttöönoton viimeistä prosessia. Tämä prosessi sisältää toiminnot, jotka tehdään AX 2012:n käytöstäpoiston jälkeen ja ennen Finance and Operations -käyttöönottoa. 

Testauksen tavoitteena on harjoitella valmistelusiirtoprosessia. Näin voit varmistaa, että todellinen valmistelusiirto sujuu kaikilta käyttäjiltä ongelmitta.

Pääasiallisia työnkulkuja on kaksi:

- **Tekninen työnkulku** – tämä on tietopäivityksen suorittamisprosessia vastaava työnkulku. Yrityksesi määrää sallitun käyttämättömyysajan. Käyttämättömyysaikana AX 2012 ja Finance and Operations eivät kumpikaan ole käytettävissä. Tekninen työnkulku saattaa hienosäätää päivitysprosessin suorituskykyä, jotta se täyttää yrityksen käyttämättömyysaikaa koskevat vaatimukset. 
- **Toiminnallinen työnkulku** – Tietopäivityksen jälkeen pitää suorittaa useita konfigurointitehtäviä Finance and Operations -ympäristössä. Nämä tehtävät pitää dokumentoida ja laskea ja niille pitää kohdistaa tarvittava resurssi, koska niiden on täsmättävä teknisten tehtävien kanssa yrityksen käyttämättömyysajan puitteissa.

Lisätietoja on kohdassa 
- [Tarkistus: valmistelusiirron testaus](upgrade-cutover-testing.md)
- [Tarkistus: sovelluksen tarkistusprosessi](app-validation-process.md)

### Toimintotestausjakso
<a id="functional-test-pass" class="xliff"></a>
Tee kaikkien liiketoimintaprosessien täydellinen toimintotestausjakso Tämä toimintatestausjakso on kaikkien Finance and Operations -palvelua käyttävien liiketoimintaprosessien laaja uudelleentestaus. Nämä liiketoimintaprosessit sisältävät vanhoja prosesseja, jotka tuotiin AX 2012:sta, sekä uusia prosesseja, joissa on uusia ja ensimmäisen kerran Finance and Operations -palvelussa käyttöönotettavia ominaisuuksia. 

Koodin laadun mukaan vian korjaaminen ja uudelleentestaus voivat edellyttää useita toimintotestausjakson toistoja. Kun vika on korjattu, testaa kaikki siihen liittyvät prosessit, jotta voit varmistaa ettei muutos vaikuta haitallisesti alempaan tai ylempään prosessiin.

Lisätietoja [Tarkistus – toiminnallinen testaus](upgrade-functional-validation.md).

### Käyttöönoton valmistelun tarkistusluettelo
<a id="pre-go-live-checklist" class="xliff"></a>
Käyttöönoton valmistelun tarkistusluettelo on suositeltava menettely, jonka avulla vähennät virhemahdollisuuksia käyttöönoton valmistelusiirron aikana. Lopeta konfigurointimuutokset AX 2012:ssa viikkoa ennen käyttöönottoa (\<moduuli\>\asennus -vaiheessa). Tämä konfigurointimuutosten rajoitus on pelkästään muodollinen. Microsoft Dynamics AX -järjestelmänvalvojat sopivat tällaisten muutosten asettamisesta pitoon tässä vaiheessa.

Suosittelemme, että lukitset koodimuutokset myös Finance and Operations -koodikannassa. Muita muutoksia ei saa tehdä, ellei niitä ole arvioitu ja osoitettu, etteivät ne estä käyttöönottoa.  

Kun konfigurointirajoitus ja koodilukitus ovat käytössä, tietojen päivitys suorittaa viimeisen kerran ennen siirtoa. Näin voit varmistaa, että kaikki toimii asianmukaisesti. 

Lisätietoja on kohdassa [Tarkistus: käyttöönoton valmistelu](upgrade-go-live-prep.md).



### Tuetut päivityspolut
<a id="supported-upgrade-paths" class="xliff"></a>
Kesäkuusta 2017 alkaen tuetaan Microsoft Dynamics AX 2012 R3:n päivittämistä Microsoft Dynamics 365 for Finance and Operations Enterprise edition -versioon 0617. Kaikki AX 2012 R3:n kumulatiiviset päivitykset ovat tuettuja.

Microsoft Dynamics AX 2012 R2 ja Microsoft Dynamics AX 2012 RTM eivät ole tuettuja. Tuki lisätään myöhemmin vuonna 2017.

Tuki koskee ainoastaan Finance and Operationsin verkossa käyttöönotettavaa versiota. Paikallisen version päivitystä ei tueta. Paikalliseen version päivityksen tuki lisätään myöhemmin vuonna 2017.

