---
title: "Paikallisten käyttöönottojen järjestelmävaatimukset"
description: "Tässä ohjeaiheessa on luettelo Microsoft Dynamics 365 for Finance and Operations Enterprise editionin nykyisen version järjestelmävaatimuksista paikallisissa käyttöönotoissa."
author: kfend
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 73fefd43c9de917dc6c98b2a6893b36a5c0ccdc5
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>Paikallisten käyttöönottojen järjestelmävaatimukset

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa on luettelo Microsoft Dynamics 365 for Finance and Operations Enterprise editionin nykyisen version järjestelmävaatimuksista paikallisissa käyttöönotoissa. Tarkista tarvittaessa tämä vaihe ennen Finance and Operationsin asennusta, että käyttämäsi järjestelmän verkkoa, laitteistoa ja ohjelmistoa koskevat vähimmäisvaatimukset täyttyvät.

## <a name="network-requirements"></a>Verkon vaatimukset
Microsoft Dynamics 365 for Finance and Operations, Enterprise editionia (paikallinen) voi käyttää IPv4 (Internet Protocol Version 4)- tai IPv6 (Internet Protocol Version 6) -verkoissa. Pohdi verkkoympäristöä, kun suunnittelet järjestelmää, ja käytä seuraavia ohjeita.

### <a name="network-response-time"></a>Verkkoyhteyden vasteaika
Seuraava taulukko sisältää verkon vähimmäisvaatimukset selaimen ja AOS (Application Object Server) -palvelimen väliselle yhteydelle sekä AOS-palvelimen ja paikallisen järjestelmän tietokannan väliselle yhteydelle.

| Arvo     | Selain AOS-palvelimeen                      | AOS tietokantaan |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| Kaistanleveys | 50 kb/s käyttäjää kohden | 100 Mb/s |
| Viive   | Alle 250–300 millisekuntia (ms)     | Alle 1 ms (vain lähiverkko [LAN]). AOS-palvelimen ja tietokannan on oltava samassa sijainnissa. |

- Finance and Operations (paikallinen) on suunniteltu verkkoihin, joiden viive on enintään 250–300 millisekuntia (ms). Tämä viive on selaimen asiakasohjelman ja Finance and Operationsia isännöivän palvelinkeskuksen välillä.
- Finance and Operationsin (paikallinen) kaistanleveysvaatimus määräytyy tilanteen mukaan. Tyypillisissä skenaarioissa selaimen ja Finance and Operationsin välisen kaistanleveyden on oltava yli 50 kb/s. Suosittelemme kuitenkin suurempaa kaistanleveyttä tilanteissa, joissa hyötykuorman vaatimus on korkea, kuten työtiloissa, tai tilanteissa, joissa vaaditaan laajaa mukauttamista. Kaistanleveyden määrä määräytyy käytön mukaan.

Käyttöönottoja, joissa AOS ja Microsoft SQL Server -tietokanta ovat eri palvelinkeskuksissa, ei tueta. AOS-palvelimen ja SQL Server -tietokannan on oltava samassa sijainnissa. 

Finance and Operations optimoidaan yleensä vähentämään selaimen ja palvelimen välisiä kyselyjä. Kyselyiden määrä selainasiakasohjelmasta palvelinkeskukseen on joko nolla tai yksi kummassakin vuorovaikutuksessa, ja koko paketti on pakattu.

> [!WARNING]
> Älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella. Tietyn sijainnin samanaikainen käyttö on hyvin vaikea laskea. Paras tapa arvioida suorituskykyä on käyttää realistista simulaatiota muussa kuin Finance and Operationsin tuotantoympäristössä. 

### <a name="lan-environments"></a>LAN-ympäristöt
Lähiverkkoympäristöissä Microsoft Windows Serverin Microsoftin etätyöpöytää ei tarvita muodostamaan yhteyttä Finance and Operationsiin. Etätyöpöytää voidaan kuitenkin tarvita palvelinkäyttöönottojen virtuaali- eli VM-koneiden palvelutoiminnoissa.

### <a name="wan-environments"></a>WAN-ympäristöt
Suuralueverkko- eli WAN-ympäristöissä Windows Serverin etätyöpöytää ei tarvita muodostamaan yhteyttä Finance and Operationsiin.

### <a name="internet-connectivity-requirements"></a>Internet-yhteysvaatimukset
Finance and Operations (paikallinen) ei edellytä, että loppukäyttäjien työasemissa on internet-yhteys. Joitakin toimintoja ei kuitenkaan voi käyttää ilman internet-yhteyttä.

|                    |   |
|--------------------|---|
| **Selainasiakas** | Paikallinen käyttöönottovaihtoehto on suunniteltu toimimaan intranet-skenaariona ilman internet-yhteyttä. Jotkin pilvipalveluja edellyttävät ominaisuudet eivät ole käytettävissä, kuten Ohje ja Microsoft Dynamics Lifecycle Servicesin (LCS) tehtäväopaskirjastot. |
| **Palvelin**         | AOS- tai Microsoft Azure Service Fabric -tason on voitava olla yhteydessä LCS:ään. Paikallinen selainpohjainen asiakasohjelma ei tarvitse internet-yhteyttä. |
| **Telemetria**      | Telemetriatiedot voidaan menettää, jos yhteys on pitkään katkenneena. LCS-yhteyden katkeaminen ei vaikuta paikallisen sovelluksen toimintaan. |
| **LCS**            | LCS-yhteys tarvitaan käyttöönottoa, koodin käyttöönottoa ja ylläpidon työvaiheita varten. |

## <a name="telemetry-data-transfer-to-the-cloud"></a>Telemetriatietojen siirto pilveen
Useimmat telemetriatiedot tallennetaan paikallisesti ja niitä voidaan käyttää Microsoft Windowsin tapahtumienvalvonnassa. Pieni osa telemetriatietoja siirretään pilvessä Microsoftin telemetriaputkeen diagnostiikkaa varten. Asiakastiedot ja loppukäyttäjän tunnistettavat tiedot eivät kuulu Microsoftille lähetettäviin telemetriatietoihin. VM-nimet lähetetään Microsoftille avustamaan ympäristön hallintaa ja diagnostiikka LCS-portaalista.

## <a name="domain-requirements"></a>Toimialuevaatimukset
Ota huomioon seuraavat toimialuevaatimukset, kun asennat Finance and Operationsin (paikallinen):

- Finance and Operationsin (paikallinen) komponentteja isännöivien VM-koneiden on kuuluttava Active Directory -toimialueeseen. Active Directory -toimialuepalvelut (AD DS) on määritettävä alkuperäisessä tilassa.
- Finance and Operationsin (paikallinen) komponentteja käyttävillä VM-koneilla on oltava toistensa käyttöoikeus. Tämä käyttöoikeus määritetään AD DS -palvelussa. 
- Toimialueen ohjaimen on oltava vähintään Microsoft Windows Server 2012 R2, ja sen toimialueen toimintatason on oltava vähintään 2012 R2

## <a name="hardware-requirements"></a>Laitevaatimukset
Tässä osassa käsitellään laitteita, joita tarvitaan Finance and Operationsin (paikallinen) käyttämiseen.

Laitteistovaatimukset voivat vaihdella järjestelmän määritysten, tietojen kokoonpanon sekä käytettävien sovellusten ja ominaisuuksien mukaan. Esimerkiksi seuraavat tekijät voivat vaikuttaa Finance and Operationsin (paikallinen) laitevaatimuksiin:

- Tapahtumien määrä tunnissa
- Yhtäaikaisten käyttäjien määrä

## <a name="minimum-infrastructure-requirements"></a>Infrastruktuurin vähimmäisvaatimukset
Finance and Operations (paikallinen) käyttää Service Fabricia AOS-palvelimen, erän, tietojen hallinnan, Management reporterin ja ympäristön Orchestrator-palvelujen isännöintiin. 

SQL Serverissä on oltava suuren käytettävyyden HADRON-asennus, jossa on vähintään kaksi solmua tuotantokäytössä.

Seuraavassa kuvassa on Service Fabric -klusterin solmujen vähimmäismääräsuositus.

[![Service fabric -klusterin solmujen vähimmäismääräsuositus](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Suoritin- ja RAM-vaatimukset
Seuraavissa taulukoissa on suorittimien ja RAM-muistin määrä, jota kukin rooli tarvitsee tämän käyttöönottovaihtoehdon suorittamiseen. Lisätietoja erillisen Service Fabric -klusterin vähimmäisvaatimussuosituksesta on ohjeaiheessa [Service Fabric -klusterin suunnittelu ja valmistelu](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Jos samaan tietokoneeseen on asennettu toinen Microsoft-ohjelmisto, järjestelmän on vastattava myös kyseisen ohjelmiston laitevaatimuksia. Muiden palvelinsovellusten koko kannattaa rajoittaa 1 gigatavuun RAM-muistista siinä tietokoneessa, johon AOS on asennettu.

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

**Tuotannon ja eristysympäristön käyttöönottojen vähimmäiskokoarviot\***

| Topologia                                        | Rooli                          | Esiintymien määrä |
|-------------------------------------------------|-------------------------------|---------------------|
| Tuotanto                                      | AOS (tietojen hallinta, erä)  | 3                   |
|                                                 | Management Reporter           | 2                   |
|                                                 | SQL Server -raportointipalvelut. | 1                   |
|                                                 | Orchestrator\*\*              | 3                   |
| Eristysympäristö                                         | AOS, tietojen hallinta, erä   | 2                   |
|                                                 | Management Reporter           | 1                   |
|                                                 | SQL Server -raportointipalvelut. | 1                   |
|                                                 | Orchestrator                  | 3                   |
| *Tuotanto- ja eristysympäristötopologioiden yhteenveto* |                               | *16*                |

\* Esikatseluversion asiakkaat tarkistavat tämän taulukon luvut, ja niitä voidaan säätää kyseisten asiakkaiden palautteen perusteella.

\*\* Orchestrator-toiminto on määritetty ensisijaiseksi solmutyypiksi ja sillä suoritetaan myös Service Fabric -palveluja.

**SQL Server -taustapalvelimen ja AD DS -palvelun ensimmäiset arviot**

<table>
<thead>
<tr>
<th></th>
<th>Rooli</th>
<th>VM-koneet/instanssit</th>
<th>Ytimet</th>
<th>Ytimet yhteensä</th>
<th>Muistia /instanssi (Gt)</th>
<th>Muistin kokonaismäärän (Gt)</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Jaettu infrastruktuuri</strong></td>
<td>SQL Server*</td>
<td>2</td>
<td>8</td>
<td>16</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>Tiedostopalvelin / tallennusalueverkko / erittäin käytettävissä oleva tallennustila</td>
<td colspan="5"><p>Taustatallennustilan on perustuttava SSD-asemiin suorituksenaikaisessa tallennusalueverkossa (SAN).</p>
<p>Koko ja IOPS-kapasiteetti perustuu kuormituksen kokoon.</p></td>
</tr>
<tr>
<td>Active Directorysta</td>
<td>3</td>
<td>4</td>
<td>12</td>
<td>16</td>
<td>48</td>
</tr>
<tr>
<td><em>Jaetun infrastruktuurin yhteenveto</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\*SQL Server -koot määräytyvät kuormitusten mukaan. Lisätietoja on kohdassa [Laitteiston koon määrittäminen paikallisissa ympäristöissä](hardware-sizing-on-premises-environments.md).

## <a name="storage"></a>Tallennus

- **AOS** – Finance and Operations (paikallinen) jakaa jäsentämättömän tiedon Server Message Block (SMB) 3.0:n avulla. Lisätietoja on ohjeaiheessa [Tallennustilat suoraan Windows Server 2016:ssa](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – Valittavissa ovat seuraavat vaihtoehdot:

    - Erittäin käytettävissä oleva SSD-määritys
    - OLTP (online transaction processing) -siirtomäärille optimoitu SAN-verkko
    - Erittäin suorituskykyinen suoraan yhdistetty tallennustila (DAS) 

- **SQL Server ja tietojen hallinnan IOPS** – Sekä tietojen hallinnan että SQL Serverin tallennustilan IOPS:n on oltava vähintään 2 000. Monet tekijät vaikuttavat tuotannon IOPS:ään. Lisätietoja on kohdassa [Laitteiston koon määrittäminen paikallisissa ympäristöissä](hardware-sizing-on-premises-environments.md).
- **VM IOPS** – Kunkin VM-koneen kirjoitus-IOPS:n oltava vähintään 100.

## <a name="virtual-host-requirements"></a>Virtuaali-isännän vaatimukset
Kun määrität Finance and Operations (paikallinen) -ympäristön virtuaali-isännät, lisätietoja on seuraavissa ohjeaiheissa: [Service Fabric -klusterin suunnittelu ja valmistelu](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) ja [Service Fabric -klusterin kuvaus](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Kullakin virtuaali-isännällä on oltava riittävästi ytimiä infrastruktuuriin, jonka kokoa mietitään. Useita lisämääritykset ovat mahdollisia, kun SQL Server sijaitsee fyysisessä laitteessa mutta kaikki muu on virtuaalista. Jos SQL Server on virtualisoitu, levyn alijärjestelmän on oltava nopea SAN tai vastaava. Varmista kaikissa tapauksissa, että virtuaali-isännän perusasetus on erittäin käytettävissä ja vikasietoinen. VM-tilannevedoksia ei saa koskaan ottaa, kun virtualisointia käytetään.

## <a name="software-requirements-for-all-server-computers"></a>Kaikkien palvelintietokoneiden ohjelmistovaatimukset
Seuraava ohjelmisto on oltava tietokoneessa, ennen kuin Finance and Operationsia (paikallinen) osia voidaan asentaa:

- Microsoft .NET Framework 4.5.1 tai uudempi
- Service Fabric

Lisätietoja on ohjeaiheessa [Service Fabric -klusterin suunnittelu ja valmistelu](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Tuetut palvelinkäyttöjärjestelmät
Seuraavassa taulukossa on Finance and Operationsin osissa tuetut palvelinkäyttöjärjestelmät.

| Käyttöjärjestelmä                                     | Muistiinpanot |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 Datacenter tai Standard | Nämä vaatimukset koskevat tietokantaa ja Service Fabric -klusteria, joka AOS-palvelimen isäntä. |

## <a name="software-requirements-for-database-servers"></a>Tietokantapalvelimen ohjelmistovaatimukset

- Vain SQL Server 2016:n 64-bittisiä versioita tuetaan.
- Tuotantoympäristöön on suositeltavaa asentaa käytettävän SQL Serverin version uusin kumulatiivinen päivitys.
- Finance and Operations (paikallinen) tukee Unicode-lajittelua, joissa otetaan huomioon kirjainkoko, aksentti, kana-merkistö ja leveys. Lajittelun on vastattava niiden tietokoneiden Windowsin aluekohtaisia asetuksia, joissa AOS-esiintymät ovat. Jos olet määrittämässä uutta asennusta, kannattaa valita Windows-lajittelu SQL Server -lajittelun sijaan. Lisätietoja SQL Server -tietokannan lajittelun valitsemista on [SQL Serverin dokumentaatiossa](/sql/sql-server/sql-server-technical-documentation).

Seuraavassa taulukossa on Finance and Operationsin tietokannoissa tuetut SQL Server -versiot. Lisätietoja on [SQL Serverin](https://www.microsoft.com/en-us/sql-server/sql-server-2016) vähimmäislaitevaatimuksissa.

| Tarve                                                      | Muistiinpanot |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server 2016 Standard Edition tai Enterprise Edition | Lisätietoja SQL Server 2016:n laitevaatimuksista on ohjeaiheessa [SQL Server 2016:n asennuksen laite- ja ohjelmistovaatimukset](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-application-object-server-aos"></a>Application Object Server (AOS) -palvelimen ohjelmistovaatimukset 
- SQL Server Integration Services (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>Raportointipalvelimen (BI) ohjelmistovaatimukset
- SQL Server Reporting Services (SSRS)

## <a name="software-requirements-for-client-computers"></a>Kaikkien asiakastietokoneiden ohjelmistovaatimukset
Finance and Operations -verkkosovellus voidaan suorittaa missä tahansa laitteessa, jossa on HTML 5.0 -yhteensopiva selain. Microsoft on vahvistanut seuraavat laite- ja selainyhdistelmät:

- Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
- Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
- Google Chrome (uusin saatavana oleva versio) Windows 10-, Windows 8.1-, Windows 8-, Windows 7- tai Google Nexus 10 -taulutietokoneen käyttöjärjestelmässä
- Apple Safari (uusin saatavana oleva versio) Mac OS X 10.10 (Yosemite)-, 10.11 (El Capitan)-, 10.12 (Sierra)- tai Apple iPadin käyttöjärjestelmässä.

## <a name="software-requirements-for-active-directory-federation-services"></a>Active Directory -liittoutumispalvelujen ohjelmistovaatimukset 
Edellytyksenä Windows Server 2016:n Active Directory -liittoutumispalvelut (AD FS).

Toimialueen ohjaimen on oltava vähintään Windows Server 2012 R2, ja sen toimialueen toimintatason on oltava vähintään 2012 R2 Lisätietoja toimialueiden toimintatasosta on seuraavilla sivuilla:

- [Active Directoryn toimintatasojen selitys](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Active Directoryn -toimialueen palvelujen toimintatasot](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>Tuetut Microsoft Office -sovellukset
Seuraavia Microsoft Office -sovelluksia tuetaan Finance and Operationsin pilvikäyttöönotoissa ja paikallisissa käyttöönotoissa:

-   Microsoft Office 2016:n Windows- tai Mac-version on oltava asennettuna, jotta Microsoft Excel ja Microsoft Word -lisäosia voi käyttää. Lisätietoja versiovaatimuksista on ohjeaiheessa [Office-integroinnin vianmääritys](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Microsoft Office 2007 tai sitä uudempi on oltava asennettuna, jotta voit tarkastella Vie Exceliin tai Vie Wordiin -toimintojen luomia asiakirjoja.
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Retail-osien laite- ja ohjelmistovaatimukset
Finance and Operations (paikallinen) ei sisällä tällä hetkellä Retail-komponentteja.

