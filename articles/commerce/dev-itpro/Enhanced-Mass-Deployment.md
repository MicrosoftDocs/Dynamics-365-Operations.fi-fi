---
title: Sinetöityjen Commerce-itsepalvelukomponenttien joukkokäyttöönotto
description: Tässä artikkelissa kerrotaan, kuinka itsepalvelukomponentin asennusohjelman kehystä käytetään käyttöönottojen valvomattomaan asennukseen ja huoltoon.
author: jashanno
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: 66a711aff90221e594f4b2a0df3735eac93d0c9b
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387016"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>Sinetöityjen Commerce-itsepalvelukomponenttien joukkokäyttöönotto

[!include [banner](../includes/banner.md)]

Tämä artikkeli koskee suljettua kehystä, komponenttien asennusohjelmia, jotka julkaistaan kuukausittain versiosta 10.0.18 alkaen ja jotka ovat saatavilla jaetun omaisuuden kirjastossa, Microsoft Dynamics Lifecycle Servicesissä (LCS). Huomaa, että näiden uusien asennusohjelmien ensimmäiset useat julkaisuversiot on määritetty **(esiversiona)**. Tämän määrityksen ainoa tarkoitus on kuitenkin eritellä uudet asennusohjelmat, kun taas Microsoft määrittää, onko niitä varten käytössä muita toimintavaatimuksia. Se ei tarkoita, että asennusohjelmat eivät kelpaa tuotantoon. Näiden uusien asennusohjelmien julkaisun perusteella Microsoft aikoo poistaa vanhat asennusohjelmat lokakuussa 2023 tai sen jälkeen. 

Tässä artikkelissa kerrotaan, miten uusia asennusohjelmia käytetään valvomattomien asennus- ja huoltopäivitysten suorittamiseen komentoriviargumenttien kautta. Näiden argumenttien avulla voit käyttää joukkokäyttöönottoja useilla eri tavoilla.

> [!NOTE]
> Uusia itsepalvelumallin suljettuja asennusohjelmia ei voi käyttää pääkonttoreissa, ja niitä voi ladata vain LCS:n kautta.

## <a name="delimiters-for-mass-deployment"></a>Erottimet joukkokäyttöönottoa varten

Seuraavassa taulukossa näkyvät erottimet, joita voidaan käyttää komentorivin suorittamisessa.


| Erotin                 | Kuvaus |
|---------------------------|-------------|
| -AadTokenIssuerPrefix | Microsoft Azure Active Directory (Azure AD) -tunnuksen myöntäjän etuliite. |
| -AsyncClientAadClientId | Asiakastunnus Azure AD, jota Async-asiakasohjelma käyttää viestinnässä Pääkonttorin kanssa. |
| -AsyncClientAppInsightsInstrumentationKey | Asyncin AppInsights-instrumentointiavain. |
| -AsyncClientCertFullPath | Kokonaan muotoiltu URN-polku, joka käyttää allekirjoitusta Async Client Identity -sertifikaatin sijainnin hakumittarina ja jota tulee käyttää Azure AD -ohjelman kanssa todennukseen pääkonttorin viestintää varten. Esimerkiksi `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` on oikein muotoiltu URN. Arvo **\<MyThumbprint\>** korvataan varmenteen allekirjoituksen, jota pitäisi käyttää. Älä käytä tätä parametria yhdessä **-AsyncClientCertThumbprint**-parametrin kanssa. |
| -AsyncClientCertThumbprint | Async-asiakastunnussertifikaatin allekirjoitus, jota tulee käyttää Azure AD -ohjelman kanssa todennukseen pääkonttorin viestintää varten. Tämän allekirjoituksen avulla voit etsiä **LocalMachine/My store** -sijainnista ja nimestä oikean varmenteen. Älä käytä tätä parametria yhdessä **-AsyncClientCertFullPath**-parametrin kanssa. |
| -ClientAppInsightsInstrumentationKey | Asiakasohjelman AppInsights-instrumentointiavain. |
| -CloudPosAppInsightsInstrumentationKey | Pilvimyyntipisteen AppInsights-instrumentointiavain. |
| -Config | Konfigurointitiedosto, jota tulee käyttää asennuksen aikana. Tiedostonimi voi olla esimerkiksi **Contoso.CommerceScaleUnit.xml**. |
| -CposAadClientId | Asiakastunnus Azure AD, jota pilvimyyntipiste käyttää laitteen aktivoinnin aikana. Tätä parametria ei tarvita paikallisissa käyttöönotoissa. |
| -Device | Laitetunnus pääkonttorin **Laitteet**-sivulla näkyvällä tavalla. |
| -EnvironmentId | Ympäristön tunnus. |
| -HardwareStationAppInsightsInstrumentationKey | Hardware Stationin AppInsights-instrumentointiavain. |
| Asenna | Parametri, joka määrittää, tuleeko tämän asennusohjelman komponenttia asentaa. Tämä parametri on pakollinen asennusta varten, eikä sillä ole väliviivamerkkiä. |
| -InstallOffline | Jos käytössä on Modern POS, tämä parametri määrittää, että offline-tietokanta tulee myös asentaa ja konfiguroida. Käytä myös **-SQLServerName**-parametria. Muutoin asennusohjelma yrittää etsiä edellytykset täyttävän oletusesiintymän. |
| -Port | Portti, johon Retail Serverin virtuaalihakemisto liitetään ja jota se käyttää. Oletusporttia 443 käytetään, jos porttia ei ole määritetty. |
| -Register | Rekisteritunnus pääkonttorin **Rekisterit**-sivulla näkyvällä tavalla. |
| -RetailServerAadClientId | Asiakastunnus Azure AD, jota Retail Server käyttää viestinnässä Pääkonttorin kanssa. |
| -RetailServerAadResourceId | Retail Server Azure AD -sovelluksen resurssitunnus, jota on käytettävä laitteen aktivoinnin aikana. Tätä parametria ei tarvita paikallisissa käyttöönotoissa. |
| -RetailServerCertFullPath | Kokonaan muotoiltu URN-polku, joka käyttää allekirjoitusta Retail Server Identity -sertifikaatin hakumittarina ja jota tulee käyttää Azure AD -ohjelman kanssa todennukseen pääkonttorin viestintää varten. Esimerkiksi `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` on oikein muotoiltu URN, jossa arvo **\<MyThumbprint\>** korvataan käytettävällä varmenteen allekirjoituksella. Älä käytä tätä parametria yhdessä **-RetailServerCertThumbprint**-parametrin kanssa. |
| -RetailServerCertThumbprint | Retail Server Identity -sertifikaatin allekirjoitus, jota tulee käyttää Azure AD -ohjelman kanssa todennukseen pääkonttorin viestintää varten. Tämän allekirjoituksen avulla voit etsiä **LocalMachine/My store** -sijainnista ja nimestä oikean varmenteen. Älä käytä tätä parametria yhdessä **-RetailServerCertFullPath**-parametrin kanssa. |
| -RetailServerURL | Retail Serverin URL-osoite, jota asennusohjelman on käytettävä. (Tätä URL-osoitetta kutsutaan myös nimellä Commerce Scale Unit \[CSU\] URL.) Tätä arvoa käytetään laiteaktivoinnin aikana modernissa myyntipisteessä. |
| -SkipAadCredentialsCheck| Kytkin, joka ilmaisee, ohitetaanko Azure AD tunnistetietojen edellytysten tarkistukset. Oletusarvo on **epätosi**. |
| -SkipCertCheck | Kytkin, joka ilmaisee, ohitetaanko sertifikaattien edellytysten tarkistukset. Oletusarvo on **epätosi**. |
| -SkipIisCheck | Kytkin, joka ilmaisee, ohitetaanko Internet Information Servicesin (IIS) edellytysten tarkistukset. Oletusarvo on **epätosi**. |
| -SkipNetFrameworkCheck | Kytkin, joka ilmaisee, ohitetaanko .NET Frameworkin edellytysten tarkistukset. Oletusarvo on **epätosi**. |
| -SkipScaleUnitHealthcheck | Kytkin, joka ilmaisee, ohitetaanko asennettujen komponenttien kuntotarkistus. Oletusarvo on **epätosi**. |
| -SkipSChannelCheck | Kytkin, joka ilmaisee, ohitetaanko turvallisen kanavan edellytysten tarkistukset. Oletusarvo on **epätosi**. |
| -SkipSqlFullTextCheck | Kytkin, joka ilmaisee, ohitetaanko täyttä tekstihakua edellyttävä SQL Server -edellytysten vahvistus. Oletusarvo on **epätosi**. |
| -SkipSqlServerCheck | Kytkin, joka ilmaisee, ohitetaanko SQL Serverin edellytysten tarkistukset. Oletusarvo on **epätosi**. |
| -SqlServerName | SQL Server -palvelimen nimi. Jos nimeä ei määritetä, asennusohjelma yrittää etsiä oletusesiintymän. |
| -SslcertFullPath | Kokonaan muotoiltu URN-polku, joka käyttää sertifikaattisijainnin hakumittarina allekirjoitusta, jonka avulla HTTP-liikenne salataan skaalausyksikölle. Esimerkiksi `store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` on oikein muotoiltu URN, jossa arvo **\<MyThumbprint\>** korvataan käytettävällä varmenteen allekirjoituksella. Älä käytä tätä parametria yhdessä **-SslCertThumbprint**-parametrin kanssa. |
| -SslCertThumbprint | Sen sertifikaatin allekirjoitus, jota käytetään HTTP-liikenteen salaamiseen skaalausyksikköön. Tämän allekirjoituksen avulla voit etsiä **LocalMachine/My store** -sijainnista ja nimestä oikean varmenteen. Älä käytä tätä parametria yhdessä **-SslCertFullPath**-parametrin kanssa. |
| -StoreSystemAosUrl | Pääkonttorin (AOS) URL-osoite. |
| -StoreSystemChannelDatabaseId | Kanavatietokannan tunnus (nimi). |
| -TenantId | Azure AD-vuokraajan tunnus. |
| -TransactionServiceAzureAuthority | Transaction Service Azure AD -viranomainen. |
| -TransactionServiceAzureResource | Transaction Service Azure AD -resurssi. |
| -TrustSqlServerCertificate | Kytkin, joka ilmaisee, luotetaanko palvelinsertifikaattiin SQL-palvelimen yhteyden muodostamisen aikana. Jotta turvallisuusriskejä voidaan välttää, tässä ei tuotantokäyttöönottojen tulisi koskaan antaa arvoa **tosi**. Oletusarvo on **epätosi**. |
| -Verbosity | Asennuksen aikana pyydetty lokiinkirjaustaso. Yleensä tätä arvoa ei tulisi käyttää. |
| -WindowsPhoneAppInsightsInstrumentationKey | Hardware Stationin AppInsights-instrumentointiavain. |

## <a name="general-overview"></a>Yhteenveto

Uusi itsepalveluasennusohjelmien kehys sisältää useita ominaisuuksia ja parannuksia. Uusi kehys luo tällä hetkellä asennusohjelmat vain modernille myyntipisteelle, hardware stationille ja CSU:lle (paikallinen ympäristö). On tärkeää ymmärtää suljettujen asennusohjelmien peruskomentorivin käyttö. Tämän pitäisi näyttää samanlaiselta kuin seuraavassa esimerkissä. 
 
```Console
<Component Installer Name>.exe install -<Parameter Name> "<Parameter Information>"
```

Asennusohjelma edellyttää parametrin **install** (tai **uninstall** asennuksen poistamiseksi) sekä asennusta koskevat parametrit. **Parametrin nimessä** tulisi olla tarvittavat parametrit, kuten rekisteri, CSU URL tai sertifikaattitiedot. **Parametrin tietoihin** tulisi sisältyä parametreja koskevat lisätiedot.

Suljettu kehys on luotu sallimaan seuraavat muutokset:
- **Suljettu** – Uusi asennusohjelmakehys erottaa Microsoftin jakamat peruskomponentin asennusohjelmat kokonaan laajennettavuuspohjaisesta mukautuksesta. Mukautukset asennetaan jälkikäteen, mutta ne on sitten irrotettu päivitysten suhteen (joten päivitykset sallitaan vain Microsoftin peruskomponentille, vain mukautuksille tai molemmille).
- **GUI-less** – Käyttöliittymää ei enää ole. Sen sijaan jokaiselle komponentin asennusohjelmalle on täysin komentorivipohjainen suoritettava tiedosto. Tämä muutos on yksi useista avainmuutoksista tai ominaisuuksista, joita käytetään uuden asennusohjelmakehyksen keskittämiseksi joukkokäyttöönottoa varten.
- **Syvällisempi kirjaaminen** – Parannetut asennusohjelman lokit mahdollistavat paremman asennuksen valmistumisen tai epäonnistumisen, suoritettujen vaiheiden ja syntyneiden varoitusten tai virheiden tarkistamisen.
- **Puhdistus** – Uudessa kehyksessä komponenttien asennusohjelmat työskentelevät kovemmin säilyttääkseen asennushakemistojen puhtauden tyhjentämällä komponenttikansion koko sisällön ennen uusien komponenttien asentamista. Puhdistus varmistaa, ettei jäljellä ole tiedostoja, jotka voivat aiheuttaa ongelmia ja estää asennuksen onnistumisen.

Kolme komponenttia, joita ei ole siirretty uuteen kehykseen: Virtual Peripheral Simulator, Async Server Connector Service (käytetään Dynamics AX 2012 R3 -tuessa) ja Real-time Service Replacement (käytetään Dynamics AX 2012 R3 -tuessa).

> [!NOTE]
> Asennusohjelmat tallennetaan paikallisesti ja säilytetään.  Ajan mittaan on tärkeää hallita tai poistaa säilytettyjä asennuksia, jotta ei hukata levytilaa. On suositeltavaa säilyttää peruskomponentin nykyinen asennusohjelma ja uusimpien versioiden laajennusasentimet äärimmäisistä tilanteista toipumista varten.

## <a name="migration"></a>Siirto

Siirtyminen vanhasta itsepalvelukehyksen komponenttien asennusohjelmasta uusiin kehyskomponenttien asennusohjelmiin edellyttää vanhojen komponenttien asennuksen poistamista.

- **Modern POS** – Uusi asennusohjelmakehys aiheuttaa sovelluksen saamaan uuden allekirjoitustunnuksen. Sen vuoksi vanhojen komponenttien täydellinen asennuksen poisto on pakollinen, ennen kuin uuden kehyksen moderni myyntipistekomponentti asennetaan. Täydellisen asennuksen poistamisen vaatimuksen vuoksi laite on aktivoitava uudelleen. (Tämä laitteen uudelleenaktivointi on kertavaatimus, jos asennuksen poistoa ei tapahdu enää.)
- **Hardware station** – IIS-verkkosivustona uusi asennuskehys edellyttää peruskansiorakenteen muokkaamista. Sen vuoksi vanhojen komponenttien täydellinen asennuksen poisto on pakollinen, ennen kuin uuden kehyksen hardware station -komponentti asennetaan.
- **Commerce Scale Unit (CSU, paikallinen ympäristö)** – IIS-verkkosivustojen sarjana uusi asennuskehys edellyttää peruskansiorakenteen muokkaamista.  Sen vuoksi vanhojen komponenttien täydellinen asennuksen poisto on pakollinen, ennen kuin uuden kehyksen CSU (paikallinen ympäristö) asennetaan.

## <a name="modern-pos"></a>Moderni myyntipiste

### <a name="before-you-begin"></a>Ennen aloittamista

On tärkeää, että poistat vanhan, paikallisen ympäristön modernin myyntipisteen komponentin. Lisätietoja on siirtymisvaiheissa aiemmin tässä artikkelissa.

> [!NOTE]
> Store Commerce ei voi suorittaa laitteen aktivointia yksittäisessä tietokoneessa, kuten kehittäjän topologiassa tai esittely-ympäristössä tai Commerce Scale Unitin ja Modern POS:in ollessa asennettuna samaan tietokoneeseen. Tämä ongelma ilmenee, koska Store Commerce ei voi suorittaa verkkokutsuja samaan tietokoneeseen (kutsua itseään). Vaikka tätä ei tule koskaan käyttää tuotantoasetuksen skenaariona, ongelmaa voi pienentää ottamalla Käyttöön AppContainer-silmukan poikkeus, jotta samaa tietokonetta voidaan käyttää viestinnässä. Tämän silmukan käyttöönottoa varten on olemassa useita julkisesti saatavilla olevia sovelulksia. For more information about palautussilmukan käyttöönotosta on kohdassa [Palautussilmukan käyttöönotto ja verkon eristyksen vianmääritys](/previous-versions/windows/apps/hh780593(v=win.10)). On tärkeää ymmärtää, että silmukka voi olla suojausriski, joten ei ole suositeltavaa käyttää palautesilmukkaa, ellei se ole välttämätöntä.

### <a name="examples-of-silent-deployment"></a>Esimerkkejä valvomattomasta käyttöönotosta

Tässä osassa on esimerkkejä komennoista, joita käytetään modernin myyntipisteen asentamiseen.

#### <a name="silently-install-modern-pos"></a>Asenna Modern POS valvomattomasti

Seuraava komento asentaa (tai päivittää) Modern POS:n valvomattomasti. Siinä on vakiokomentorakenne, jota käytetään parhaillaan asennettujen komponenttien valvomattomaan huoltoon. Rakenteessa käytetään **&lt;InstallerName&gt;.exen perusarvoja**.

Seuraava peruskomento sisältää käytettävissä olevat vaihtoehdot, jos asennusta pyydetään. On erittäin suositeltavaa käyttää tätä komentoa ensimmäistä kertaa testattaessa tai käytettäessä asennusohjelmaa.

```Console
CommerceModernPOS.exe -help install
```

> [!NOTE]
> Moderni POS ei vaadi määritystiedostoa. Asennusohjelmalla on nyt parametrit (jotka näkyvät aiemmin tässä artikkelissa) niiden arvojen yhteydessä, joita käytetään laitteen aktivoinnin aikana.

Seuraava komento määrittää kaikki parametrit, joita on käytettävä laiteaktivoinnin aikana sen jälkeen, kun Moderni POS -sovellus on asennettu. Tässä esimerkissä käytetään **Houston-3**-rekisteriä, joka on yleisesti käytetty arvo Dynamics 365 Commerce -demotiedoissa.

```Console
CommerceModernPOS.exe install -Register "Houston-3" -Device "Houston-3" -RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

Seuraava komento määrittää parametrit, joita käytetään offline-tietokannan asentamisessa ja konfiguroinnissa. SQL Server määritetään yhdessä käytettävän konfigurointitiedoston kanssa.

```Console
CommerceModernPOS.exe install -InstallOffline -SQLServerName "SQLExpress" -Config "ModernPOS.Houston-3.xml"
```

Voit yhdistellä näitä käsitteitä haluamasi asennustuloksen saamiseksi.

## <a name="hardware-station"></a>Laiteasema

### <a name="before-you-begin"></a>Ennen aloittamista

On tärkeää, että poistat vanhan, paikallisen ympäristön hardware station -komponentin. Lisätietoja on siirtymisvaiheissa aiemmin tässä artikkelissa. Ei ole enää Merchant Account Information Tool -työkalua. Sen sijaan myyjätilin tiedot asennetaan kassapäätteen asennuksen yhteydessä. On erittäin suositeltavaa suorittaa tämä komento ensimmäistä kertaa testattaessa asennusohjelmaa:

```Console
CommerceHardwareStation.exe -help install
```

### <a name="examples-of-silent-deployment"></a>Esimerkkejä valvomattomasta käyttöönotosta

Tässä osassa on esimerkkejä komennoista, joita käytetään hardware stationin asentamiseen.

#### <a name="silently-install-hardware-station"></a>Asenna Hardware station valvomattomasti

Seuraava komento asentaa (tai päivittää) hardware stationin valvomattomasti. Siinä on vakiokomentorakenne, jota käytetään parhaillaan asennettujen komponenttien huoltoon. Rakenteessa käytetään **&lt;InstallerName&gt;.exen perusarvoja**.

Seuraava peruskomento suorittaa suoritettavien tiedostojen asennusohjelman.

```Console
HardwareStation.exe install -Port 443 -StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" -StoreSystemChannelDatabaseID "Houston" -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> Hardware station ei vaadi määritystiedostoa. Asennusohjelmalla on nyt parametrit (jotka näkyvät aiemmin tässä artikkelissa) tarvittaville arvoille.

Seuraava komento määrittää kaikki parametrit, joita tarvitaan edellytysten tarkistusten ohittamiseksi vakioasennuksen aikana. 

> [!NOTE]
> Tarkistusten ohittamista ei suositella ilman perusteellista testausta etukäteen tai kehitystilanteissa.

```Console
HardwareStation.exe install -SkipFirewallUpdate -SkipOPOSCheck -SkipVersionCheck -SkipURLCheck -Config "HardwareStation.Houston.xml"
```

Voit yhdistellä näitä käsitteitä haluamasi asennustuloksen saamiseksi.

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (paikallinen ympäristö)

On erittäin suositeltavaa suorittaa tämä komento ensimmäistä kertaa testattaessa asennusohjelmaa:

```Console
CommerceStoreScaleUnitSetup.exe -help install
```

### <a name="before-you-begin"></a>Ennen aloittamista

On tärkeää, että poistat vanhan, paikallisen ympäristön CSU-komponentin. Lisätietoja on siirtymisvaiheissa aiemmin tässä artikkelissa.

### <a name="examples-of-silent-deployment"></a>Esimerkkejä valvomattomasta käyttöönotosta

Tässä osassa on esimerkkejä komennoista, joita käytetään CSU:n (paikallinen ympäristö) asentamiseen.

#### <a name="silently-install-csu-self-hosted"></a>CSU:n asennus valvomattomasti (paikallinen ympäristö)

Seuraava komento asentaa (tai päivittää) CSU:n (paikallinen ympäristö) valvomattomasti. Siinä on vakiokomentorakenne, jota käytetään parhaillaan asennettujen komponenttien valvomattomaan huoltoon. Rakenteessa käytetään **&lt;InstallerName&gt;.exen perusarvoja**.

Commerce Scale Unit (CSU) on monimutkaisempi kuin muut itsepalvelun asennusohjelmat, ja se edellyttää melko paljon lisätietoja. Seuraava komento on vähimmäiskomento (ja parametrit), joka tarvitaan suoritettavan tiedoston asennusohjelman suorittamiseen, kun konfigurointitiedostoa ei ole.

```Console
CommerceScaleUnit.exe install -port 446 -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> Konfigurointitiedostoa tarvitaan edelleen CSU:ssa (paikallinen ympäristö).

Seuraava komento on perusteellisempi komento, joka suorittaa suoritettavan tiedoston asennusohjelman ja sisältää joitakin vaihtoehtoisia parametreja.

```Console
CommerceScaleUnit.exe install -Port 446 -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Verbosity 0 -Config "Contoso.StoreSystemSetup.xml"
```

Seuraava komento määrittää parametrit, joita tarvitaan edellytysten tarkistusten ohittamiseksi vakioasennuksen aikana. 

> [!NOTE]
> Tarkistusten ohittamista ei suositella ilman perusteellista testausta etukäteen tai kehitystilanteissa.


```Console
CommerceScaleUnit.exe installer -skipscaleunithealthcheck -skipcertcheck -skipaadcredentialscheck -skipschannelcheck -skipiischeck -skipnetcorebundlecheck -skipsqlservercheck -skipnetframeworkcheck -skipversioncheck -skipurlcheck -Config "Contoso.StoreSystemSetup.xml" -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate
```

Voit yhdistellä näitä käsitteitä haluamasi asennustuloksen saamiseksi.

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
