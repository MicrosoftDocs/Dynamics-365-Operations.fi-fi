---
title: "Järjestelmävaatimukset"
description: "Tässä ohjeaiheessa on luettelo Microsoft Dynamics 365 for Finance and Operations Enterprise editionin nykyisen version järjestelmävaatimuksista pilvikäyttöönotossa ja paikallisessa käyttöönotossa."
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: fi-fi
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>Järjestelmävaatimukset

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa on luettelo Microsoft Dynamics 365 for Finance and Operations Enterprise editionin nykyisen version järjestelmävaatimuksista pilvikäyttöönotossa ja paikallisessa käyttöönotossa. Tarkista tarvittaessa ennen Finance and Operationsin asennusta, että käyttämäsi järjestelmän verkkoa, laitteistoa ja ohjelmistoa koskevat vähimmäisvaatimukset täyttyvät.


## <a name="supported-microsoft-office-applications"></a>Tuetut Microsoft Office -sovellukset
Seuraavia Office-sovelluksia tuetaan Finance and Operationsin pilvikäyttöönotoissa ja paikallisissa käyttöönotoissa.
-   Microsoft Office 2016:n Windows- tai Mac-version on oltava asennettuna, jotta Microsoft Excel ja Word-lisäosia voi käyttää. Lisätietoja versiovaatimuksista löydät kohdasta [Office-integroinnin vianmääritys](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Microsoft Office 2007 tai sitä uudempi on oltava asennettuna, jotta voit tarkastella Vie Exceliin tai Vie Wordiin -toimintojen luomia asiakirjoja.

# <a name="system-requirements-specific-to-cloud-deployments"></a>Pilvikäyttöönottoja koskevat järjestelmävaatimukset
## <a name="network-requirements"></a>Verkon vaatimukset
-   Finance and Operations on suunniteltu verkkoihin, joiden viive on enintään 250–300 millisekuntia (ms). Tämä on viive selainasiakkaan ja Microsoftin Azure-datakeskuksen välillä, joka isännöi Finance and Operations -sovellusta. On suositeltavaa testata verkon viive osoitteessa <http://www.azurespeed.com>.
-   Finance and Operationsin kaistanleveysvaatimus määräytyy tilanteen mukaan. Yleisimmät tilanteet vaativat yli 50 kilotavua sekunnissa (KBps) kaistanleveyttä. Suosittelemme kuitenkin suurempaa kaistanleveyttä tilanteissa, joissa hyötykuorman vaatimus on korkea, kuten työtiloissa, tai tilanteissa, joissa vaaditaan laajaa mukauttamista.

Finance and Operations on yleisesti optimoitu Internet-käyttöön. Kyselyiden määrä selainasiakasohjelmasta Azure-datakeskukseen on hyvin pieni, ja koko paketti on pakattu. 

> [!WARNING]
> Älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella. Tietyn sijainnin samanaikainen käyttö on hyvin vaikea laskea. Asiakkaat, jotka ovat huolissaan kaistanleveyden vaatimuksista voivat käyttää Finance and Operationsin ennakkoversiota.

## <a name="net-framework-requirements"></a>.NET Framework -vaatimukset
Finance and Operations edellyttää .NET Framework -version 4.6.2 kaikille yhden napsautuksen sovelluksille, kuten asiakirjan reititysagentille. Asennusohjeet löydät kohdasta [.NET Frameworkin asentaminen](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-web-browsers"></a>Tuetut selaimet
Verkkosovellus voidaan suorittaa seuraavissa selaimissa, joita käytetään määritetyissä käyttöjärjestelmissä:


-   Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
-   Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
-   Google Chrome (uusin saatavana oleva versio) Windows 10-, Windows 8.1-, Windows 8-, Windows 7- tai Google Nexus 10 -taulutietokoneen käyttöjärjestelmässä
-   Apple Safari (uusin saatavana oleva versio) Mac OS X 10.10 (Yosemite)-, 10.11 (El Capitan)-, 10.12 (Sierra)- tai Apple iPadin käyttöjärjestelmässä.

Ohjelmistovalmistajien sivustot sisältävät tietoja kunkin selaimen uusimmasta versiosta. 

> [!NOTE]
> -   Chrome-laajennuksen ennakkojulkaisuversio pitää olla asennettuna, jotta voit tallentaa tehtävän tallennustoiminnon luomat kuvat ja sisällyttää ne Microsoft Word -asiakirjoihin. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Työnkulkueditori käynnistetään ClickOnce-sovelluksena. Ainoastaan Microsoft Edge ja Internet Explorer (tuetussa Microsoft Windows -versiossa) tukevat ClickOnce-sovelluksia. Työnkulkueditorin ClickOnce-sovellus vaatii 64-bittisen käyttöjärjestelmän.
> -   Taloushallinnon raportoinnin raportin suunnittelusovellus käynnistetään ClickOnce-sovelluksena. Siihen vaatii 64-bittisen käyttöjärjestelmän. Jos käytössäsi on Chrome, sinun on asennettava ClickOnce-laajennus ladataksesi raportin suunnittelun asiakasohjelman. Jos käytät Chromea incognito-tilassa, varmista, että ClickOnce-laajennus on käytössä incognito-tilassa.
> -   PDF-tiedostojen esikatseluun suosittelemme modernia verkkoselainta, kuten Microsoft Edge (uusin julkinen versio) Windows 10 -käyttöjärjestelmässä tai Google Chrome (uusin julkinen versio) Windows 10, Windows 8.1, Windows 8 tai Windows 7 -käyttöjärjestelmässä tai Google Nexus 10 -taulutietokoneessa.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS -sovelluksen tuetut selaimet

Vähittäismyynnin pilvimyyntipiste voidaan suorittaa seuraavissa selaimissa, joita käytetään määritetyissä käyttöjärjestelmissä:

-   Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
-   Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
-   Chrome (uusin julkaistu versio) Windows 10, Windows 8.1 tai Windows 7 -käyttöjärjestelmässä

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS -vaatimukset
### <a name="supported-operating-systems"></a>Tuetut käyttöjärjestelmät

-   Retail Modern POS on 32-bittinen sovellus, mutta sen voi suorittaa sekä x86- että x64-arkkitehtuureilla.
-   Retail Modern POS on tuettu vain Windows 10 Pro, Enterprise ja Enterprise LTSB -versioissa.

### <a name="minimum-system-requirements"></a>Järjestelmän vähimmäisvaatimukset

-   Pienin tuettu näyttötarkkuus on 1280 × 1024.
-   Tietokoneen, jolla Retail Modern POS -sovellusta käytetään on vastattava seuraavia vaatimuksia:
    -   Siinä on oltava vähintään kaksiytiminen suoritin, jonka nopeus on vähintään 2 gigahertsiä (GHz).
    -   Siinä on oltava vähintään 3 gigatavua (GB) keskusmuistia.
    -   Siinä on oltava Internet-yhteys.

## <a name="retail-hardware-station-requirements"></a>Retail hardware station -vaatimukset
### <a name="supported-operating-systems"></a>Tuetut käyttöjärjestelmät

-   Retail hardware station on 32-bittinen sovellus, mutta sen voi suorittaa sekä x86- että x64-arkkitehtuureilla.
-   Retail hardware station on tuettu seuraavissa käyttöjärjestelmissä:
    -   Windows 7 Professional, Enterprise ja Ultimate 
    
    > [!NOTE]
    > Windows 7:ää tuetaan vain, jos Internet Explorer 11 asennetaan manuaalisesti järjestelmään.

    -   Windows 8.1 Update 1 Professional, Enterprise ja Embedded
    -   Windows 10 Pro, Enterprise ja Enterprise LTSB

### <a name="minimum-system-requirements"></a>Järjestelmän vähimmäisvaatimukset

Tietokoneen on täytettävä kaikki järjestelmän vähimmäisvaatimukset, jotta seuraavien kohteiden asennus ja käyttö on mahdollista:

-   IIS (Internet Information Services)
-   Kolmannen osapuolen laitteisto

## <a name="retail-store-scale-unit-requirements"></a>Vähittäismyymälän vähittäismyyntilaitteen vaatimukset
### <a name="supported-operating-systems"></a>Tuetut käyttöjärjestelmät

-   Vähittäismyymälän vähittäismyyntilaite on 32-bittinen sovellus, mutta sen voi suorittaa sekä x86- että x64-arkkitehtuureilla.
-   Vähittäismyymälän vähittäismyyntilaite on tuettu seuraavissa käyttöjärjestelmissä:
    -   Windows 7 Professional, Enterprise ja Ultimate
    -   Windows 8.1 Update 1 Professional, Enterprise ja Embedded
    -   Windows 10 Pro, Enterprise ja Enterprise LTSB

### <a name="minimum-system-requirements"></a>Järjestelmän vähimmäisvaatimukset

-   4 Gt RAM-muistia
-   1,6 GHz korkein ytimen suoritinnopeus (vähintään kaksi ydintä)
-   Vähintään 10 gigatavua vapaata tallennustilaa (kanavatietokanta voi vaatia paljon tallennustilaa)

### <a name="recommended-system-requirements"></a>Suositeltavat järjestelmävaatimukset

-   6 Gt RAM-muistia
-   2,4 GHz i7 (tai vastaava) ydinkohtainen suoritinnopeus (suositus on neljä ydintä)
-   Vähintään 10 gigatavua vapaata tallennustilaa (kanavatietokanta voi vaatia paljon tallennustilaa)

## <a name="connector-requirements"></a>Connectorin vaatimukset
### <a name="supported-operating-systems"></a>Tuetut käyttöjärjestelmät

-   Connector for Microsoft Dynamics AX:ssä on kaksi erillistä asennusohjelmaa, **Async Server Connector service** ja **Real-time service for Dynamics AX 2012 R3**.
-   Molemmat komponentit ovat 32-bittinen sovelluksia, mutta ne voi suorittaa sekä x86- että x64-arkkitehtuureilla.
-   Seuraavat käyttöjärjestelmät tukevat molempia komponentteja:
    -   Windows 7 Professional, Enterprise ja Ultimate
    -   Windows 8.1 Update 1 Professional, Enterprise ja Embedded
    -   Windows 10 Pro, Enterprise ja Enterprise LTSB
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Järjestelmän vähimmäisvaatimukset

-   2 GT RAM-muistia, 4 GT RAM-muistia suositellaan
-   1,6 GHz korkein ytimen suoritinnopeus (vähintään kaksi ydintä)
-   Vähintään 10 gigatavua vapaata tallennustilaa (kanavatietokanta voi vaatia paljon tallennustilaa)

## <a name="requirements-for-development-on-local-vms"></a>Vaatimukset paikalliseen kehitykseen virtuaalikoneessa
Lisätietoja paikallisesta virtuaalikoneessa (VMs) kehittämistä koskevista vaatimuksista on kohdassa [Paikalliset virtuaalikoneet](../dev-tools/access-instances.md).

# <a name="system-requirements-for-on-premises-deployments"></a>Paikallisten käyttöönottojen järjestelmävaatimukset

## <a name="network-requirements"></a>Verkon vaatimukset
Finance and Operationsia (paikallinen) voi käyttää verkoissa, joissa on käytössä Internet Protocol Version 4 (IPv4) tai Internet Protocol Version 6 (IPv6). Pohdi verkkoympäristöä, kun suunnittelet järjestelmää, ja käytä seuraavia ohjeita.

### <a name="network-response-time"></a>Verkkoyhteyden vasteaika
Seuraava taulukko sisältää verkon vähimmäisvaatimukset selaimen ja AOS (Application Object Server) -palvelimen väliselle yhteydelle sekä AOS-palvelimen ja paikallisen järjestelmän tietokannan väliselle yhteydelle.

| Arvo     | Selain AOS-palvelimeen | AOS tietokantaan                                            |
|-----------|--------------------|------------------------------------------------------------|
| Kaistanleveys | 50 kbit/s käyttäjää kohti   | 100 MBit/s                                                   |
| Viive   | < 250–300 ms       | < 1 ms (vain LAN). AOS-palvelimen ja tietokannan on oltava samassa sijainnissa. |

- Finance and Operations (paikallinen) on suunniteltu verkkoihin, joiden viive on enintään 250–300 millisekuntia (ms). Tämä viive on selaimen asiakasohjelman ja Finance and Operationsia isännöivän palvelinkeskuksen välillä.
- Finance and Operationsin (paikallinen) kaistanleveysvaatimus määräytyy tilanteen mukaan. Tyypillisissä skenaarioissa selaimen ja Finance and Operationsin välisen kaistanleveyden on oltava yli 50 kbit/s. Suosittelemme kuitenkin suurempaa kaistanleveyttä käytön mukaan tilanteissa, joissa hyötykuorman vaatimus on korkea, kuten työtiloissa, tai tilanteissa, joissa vaaditaan laajaa mukauttamista.
Käyttöönottoja, joissa AOS ja SQL Server -tietokanta ovat eri palvelinkeskuksissa, ei tueta. AOS-palvelimen ja SQL Server -tietokannan on oltava samassa sijainnissa. Finance and Operations optimoidaan yleensä vähentämään selaimen ja palvelimen välisiä kyselyjä. Kyselyiden määrä selainasiakasohjelmasta datakeskukseen on joko nolla tai yksi kummassakin vuorovaikutuksessa ja koko paketti on pakattu.

> [!WARNING]
> Älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella. Tietyn sijainnin samanaikainen käyttö on hyvin vaikea laskea. Paras tapa arvioida suorituskykyä on käyttää realistista simulaatiota Finance and Operationsin muussa kuin tuotantoympäristössä. 

### <a name="lan-environments"></a>LAN-ympäristöt
Lähiverkko- eli LAN-ympäristöissä Microsoft Windows Serverin Microsoftin etätyöpöytää ei tarvita muodostamaan yhteyttä Finance and Operationsiin. Sitä voidaan kuitenkin tarvita palvelinkäyttöönottojen VM-koneiden palvelutoiminnoissa.

### <a name="wan-environments"></a>WAN-ympäristöt
Suuralueverkko- eli WAN-ympäristöissä Windows Serverin etätyöpöytää ei tarvita muodostamaan yhteyttä Finance and Operationsiin.

### <a name="internet-connectivity-requirements"></a>Internet-yhteysvaatimukset
Finance and Operations (paikallinen) ei edellytä, että loppukäyttäjien työasemissa on internet-yhteys. Joitakin toimintoja ei kuitenkaan voi käyttää ilman internet-yhteyttä.

| Selainasiakas | Paikallinen käyttöönottovaihtoehto on suunniteltu toimimaan intranet-skenaariona ilman internet-yhteyttä. Jotkin pilvipalveluja edellyttävät ominaisuudet eivät ole käytettävissä, kuten Ohje ja LCS:n tehtäväopaskirjastot. |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Palvelin         | AOS- tai Service Fabric -tason on voitava olla yhteydessä LCS:ään. Paikallinen selainpohjainen asiakasohjelma ei tarvitse internet-yhteyttä.                                                                                |
| Telemetria      | Telemetriatiedot voidaan menettää, jos yhteys on pitkään katkenneena. LCS-yhteyden katkeaminen ei vaikuta paikallisen sovelluksen toimintaan.                                                |
| LCS            | LCS-yhteys tarvitaan käyttöönottoa, koodin käyttöönottoa ja ylläpidon työvaiheita varten.                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>Telemetriatietojen siirto pilveen
Useimmat telemetriatiedot tallennetaan paikallisesti ja niitä voidaan käyttää Microsoft Windowsin tapahtumienvalvonnassa. Pieni osa telemetriatietoja siirretään pilvessä Microsoftin telemetriaputkeen diagnostiikkaa varten. Asiakastiedot ja loppukäyttäjän tunnistettavat tiedot eivät kuulu Microsoftille lähetettäviin telemetriatietoihin. VM-nimet lähetetään Microsoftille avustamaan ympäristön hallintaa ja diagnostiikka LCS-portaalista.

## <a name="domain-requirements"></a>Toimialuevaatimukset
Ota huomioon seuraavat toimialuevaatimukset, kun asennat Finance and Operationsin (paikallinen):

- Finance and Operationsin (paikallinen) komponentteja isännöivien virtuaalikoneiden on kuuluttava Active Directory -toimialueeseen. Active Directory -toimialuepalvelut (AD DS) on määritettävä alkuperäisessä tilassa.
- Virtuaalikoneilla, joissa Finance and Operationsin (paikallinen) komponentteja käytetään, on oltava toistensa käyttöoikeudet ja niiden on oltava määritetty Active Directory -toimialuepalveluissa. 
- Toimialueohjainta on käytettävä Microsoft Windows Server 2016:ssa.

## <a name="hardware-requirements"></a>Laitevaatimukset
Tässä osassa käsitellään laitteita, joita tarvitaan Finance and Operationsin (paikallinen) käyttämiseen.
Laitteistovaatimukset voivat vaihdella järjestelmän määritysten, tietojen kokoonpanon sekä käytettävien sovellusten ja ominaisuuksien mukaan. Esimerkiksi seuraavat tekijät voivat vaikuttaa Finance and Operationsin (paikallinen) laitevaatimuksiin:

- Tapahtumien määrä tunnissa.
- Yhtäaikaisten käyttäjien määrä.

## <a name="minimum-infrastructure-requirements"></a>Infrastruktuurin vähimmäisvaatimukset
Finance and Operations (paikallinen) käyttää Microsoft Azure Service Fabricia AOS-palvelimen, erän, tietojen hallinnan, Management reporterin ja ympäristön Orchestrator-palvelujen isännöintiin. Microsoft SQL Server Reporting Servicesiä (SSRS) ei isännöidä Service Fabric -klusterissa.
SQL Server on määritettävä suuren käytettävyyden HADRON-asennuksena, jossa on vähintään kaksi solmua tuotantokäytössä.
Seuraavassa kuvassa on Service Fabric -klusterin solmujen vähimmäismääräsuositus.

[![service fabric -klusterin solmujen vähimmäismääräsuositus](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Suoritin- ja RAM-vaatimukset
Seuraavassa taulukossa on suorittimien ja RAM-muistin määrä, jota kukin rooli tarvitsee tämän käyttöönottovaihtoehdon suorittamiseen. Lisätietoja erillisen Service Fabric -klusterin vähimmäisvaatimussuosituksesta on ohjeaiheessa [Service Fabric -klusterin suunnittelu ja valmistelu](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Jos samaan tietokoneeseen on asennettu toinen Microsoft-ohjelmisto, järjestelmän on vastattava myös kyseisen ohjelmiston laitevaatimuksia. Muiden palvelinsovellusten koko kannattaa rajoittaa 1 gigatavuun RAM-muistista siinä tietokoneessa, jossa AOS on.

**Koon muuttaminen roolin ja topologiatyypin mukaan**

| Topologia   | Rooli (solmutyyppi)              | Suorittimien ydinsuositukset | Muistisuositus (Gt) |
|------------|-------------------------------|-----------------------------|-------------------------|
| Tuotanto | AOS, tietojen hallinta, erä   | 8                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server -raportointipalvelut. | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |
| Eristysympäristö    | AOS, tietojen hallinta, erä   | 4                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server -raportointipalvelut. | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |

**Tuotannon ja eristysympäristön käyttöönottojen vähimmäiskokoarviot**\*

| Topologia                                  | Rooli                          | Esiintymien määrä |
|-------------------------------------------|-------------------------------|---------------------|
| Tuotanto                                | AOS (tietojen hallinta, erä)  | 3                   |
|                                           | Management Reporter           | 2                   |
|                                           | SQL Server -raportointipalvelut. | 1                   |
|                                           | Orchestrator\*\*                | 3                   |
| Eristysympäristö                                   | AOS, tietojen hallinta, erä   | 2                   |
|                                           | Management Reporter           | 1                   |
|                                           | SQL Server -raportointipalvelut. | 1                   |
|                                           | Orchestrator                  | 3                   |
| *Tuotanto- ja eristysympäristötopologioiden yhteenveto* |                               | 16                  |

\*Esiversion käyttäjät arvioivat näitä lukuja ja niitä voidaan säätää tämän palautteen perusteella.

\*\*Orchestrator-toiminto on määritetty ensisijaiseksi solmutyypiksi ja sillä suoritetaan myös Service Fabric -palveluja.

**SQL Server -taustapalvelin ja ensimmäiset AD-arviot**

[![SQL Server -taustapalvelin ja ensimmäiset AD-arviot](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*SQL Server -koot määräytyvät kuormitusten mukaan. Lisätietoja on kohdassa [Laitteiston koon määrittäminen paikallisissa ympäristöissä](#Hardware-sizing-for-on-premises-environments).

## <a name="storage"></a>Tallennus

- **AOS** – Finance and Operations (paikallinen) jakaa jäsentämättömän tiedon Server Message Block (SMB) 3.0:n avulla. Lisätietoja on ohjeaiheessa [Tallennustilat suoraan Windows Server 2016:ssa](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – mahdolliset vaihtoehdot:
    - Erittäin käytettävissä oleva SSD-aseman määritys.
    - OLTP-kierroksille optimoitu tallennusalueverkko (SAN).
    - Erittäin suorituskykyinen suoraan yhdistetty tallennustila (DAS) 
- **SQL ja tietojen hallinnan IOPS** – Sekä tietojen hallinnan että SQL Serverin tallennustilan IOPS:n on oltava vähintään 2 000. Monet tekijät vaikuttavat tuotannon IOPS:ään. Lisätietoja on kohdassa Laitteiston koon määrittäminen paikallisissa ympäristöissä. 
- **Virtuaalikoneen IOPS** – jokaisen virtuaalikoneen kirjoitus-IOPS:n oltava vähintään 100.

## <a name="virtual-host-requirements"></a>Virtuaali-isännän vaatimukset
Kun määrität Finance and Operations (paikallinen) -ympäristön virtuaali-isännät, käytä seuraavia ohjeita: [Service Fabric -klusterin suunnittelu ja valmistelu](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) ja [Service Fabric -klusterin kuvaus](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Kullakin virtuaali-isännällä on oltava riittävästi ytimiä infrastruktuuriin, jonka kokoa mietitään. Useita lisämääritykset ovat mahdollisia, kun SQL Server sijaitsee fyysisessä laitteessa mutta kaikki muu on virtuaalista. Jos SQL Server on virtualisoitu, levyn alijärjestelmän on oltava nopea SAN tai vastaava. Varmista kaikissa tapauksissa, että virtuaali-isännän perusasetus on erittäin käytettävissä ja vikasietoinen. VM-tilannevedoksia ei saa koskaan ottaa, kun virtualisointia käytetään.

## <a name="software-requirements-for-all-server-computers"></a>Kaikkien palvelintietokoneiden ohjelmistovaatimukset
Seuraava ohjelmisto on oltava tietokoneessa, ennen kuin Finance and Operationsia (paikallinen) osia voidaan asentaa:

- Microsoft .NET Framework 4.5.1. tai uudempi
- Service Fabric Lisätietoja on ohjeaiheessa [Service Fabric -klusterin suunnittelu ja valmistelu](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Tuetut palvelinkäyttöjärjestelmät
Seuraavassa taulukossa on Finance and Operationsin osissa tuetut palvelinkäyttöjärjestelmät.

| Käyttöjärjestelmä                                     | Muistiinpanot                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Datacenter tai Standard | Nämä vaatimukset koskevat tietokantaa ja Service Fabric -klusteria, joka AOS-palvelimen isäntä. |

## <a name="software-requirements-for-database-servers"></a>Tietokantapalvelimen ohjelmistovaatimukset

- Vain SQL Server 2016:n 64-bittisiä versioita tuetaan.
- Tuotantoympäristöön on suositeltavaa asentaa käytettävän SQL Serverin version uusin kumulatiivinen päivitys.
- Finance and Operations (paikallinen) tukee Unicode-lajittelua, joissa otetaan huomioon kirjainkoko, aksentti, kana-merkistö ja leveys. Lajittelun on vastattava niiden tietokoneiden Windowsin aluekohtaisia asetuksia, joissa AOS-esiintymät ovat. Jos olet määrittämässä uutta asennusta, kannattaa valita Windows-lajittelu SQL Server -lajittelun sijaan. Lisätietoja SQL Server -tietokannan lajittelun valitsemista on [SQL Serverin dokumentaatiossa](/sql/sql-server/sql-server-technical-documentation).
Seuraavassa taulukossa on Finance and Operationsin tietokannoissa tuetut SQL Server -versiot. Lisätietoja on [SQL Serverin](https://www.microsoft.com/en-us/sql-server/sql-server-2016) vähimmäislaitevaatimuksissa.

| Tarve                                                      | Muistiinpanot                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard Edition tai Enterprise Edition | Lisätietoja SQL Server 2016:n laitevaatimuksista on ohjeaiheessa [SQL Server 2016:n asennuksen laite- ja ohjelmistovaatimukset](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>Kaikkien asiakastietokoneiden ohjelmistovaatimukset
Finance and Operations -verkkosovellus voidaan suorittaa missä tahansa laitteessa, jossa on yhteensopiva HTML5.0 -selain. Microsoft on vahvistanut seuraavat laite- ja selainyhdistelmät:

- Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
- Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
- Google Chrome (uusin saatavana oleva versio) Windows 10-, Windows 8.1-, Windows 8-, Windows 7- tai Google Nexus 10 -taulutietokoneen käyttöjärjestelmässä
- Apple Safari (uusin saatavana oleva versio) Mac OS X 10.10 (Yosemite)-, 10.11 (El Capitan)-, 10.12 (Sierra)- tai Apple iPadin käyttöjärjestelmässä.

## <a name="software-requirements-for-active-directory-federation-services"></a>Active Directory -liittoutumispalvelujen ohjelmistovaatimukset 
Active Directory -liittoutumispalvelut (AD FS) Windows Server 2016:ssa

Toimialueen ohjaimen on oltava vähintään Windows Server 2012 R2, jossa toimialueen toimintataso on vähintään 2012 R2

Lisätietoja toimialueiden toimintatasosta: 
- [Active Directoryn toimintatasojen selitys](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Active Directoryn -toimialueen palvelujen toimintatasot](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Retail-osien laite- ja ohjelmistovaatimukset
Finance and Operations (paikallinen) ei sisällä tällä hetkellä Retail-osia.

<a name="see-also"></a>Lisätietoja
--------

[Dynamics 365 for Finance and Operations, Enterprise Editionin kokeiluversion hankkiminen](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

