---
title: "Pilvikäyttöönottojen järjestelmävaatimukset"
description: "Tässä ohjeaiheessa on luettelo Microsoft Dynamics 365 for Finance and Operations Enterprise editionin nykyisen version järjestelmävaatimuksista pilvikäyttöönotoissa."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 5230911e1febc66b294f1331846373a472789adf
ms.openlocfilehash: 46eacb2a01c3bfcc7144c7d8c39ee0189fd72e16
ms.contentlocale: fi-fi
ms.lasthandoff: 08/04/2017

---

# <a name="system-requirements-for-cloud-deployments"></a>Pilvikäyttöönottojen järjestelmävaatimukset

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa on luettelo Microsoft Dynamics 365 for Finance and Operations Enterprise editionin nykyisen version järjestelmävaatimuksista pilvikäyttöönotoissa. Tarkista tarvittaessa tämä vaihe ennen Finance and Operationsin asennusta, että käyttämäsi järjestelmän verkkoa, laitteistoa ja ohjelmistoa koskevat vähimmäisvaatimukset täyttyvät.

## <a name="supported-web-browsers"></a>Tuetut selaimet
Verkkosovellus voidaan suorittaa seuraavissa selaimissa, joita käytetään määritetyissä käyttöjärjestelmissä:

-   Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
-   Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
-   Google Chrome (uusin saatavana oleva versio) Windows 10-, Windows 8.1-, Windows 8-, Windows 7- tai Google Nexus 10 -taulutietokoneen käyttöjärjestelmässä
-   Apple Safari (uusin saatavana oleva versio) Mac OS X 10.10 (Yosemite)-, 10.11 (El Capitan)-, 10.12 (Sierra)- tai Apple iPadin käyttöjärjestelmässä.

Ohjelmistovalmistajien sivustot sisältävät tietoja kunkin selaimen uusimmasta versiosta. 

> [!NOTE]
> -   Chrome-laajennuksen ennakkojulkaisuversio on asennettava, jotta voit tallentaa tehtävien tallennustoiminnon luomat kuvat ja sisällyttää ne Word-asiakirjoihin. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Työnkulkueditori käynnistetään ClickOnce-sovelluksena. Ainoastaan Microsoft Edge ja Internet Explorer (tuetussa Microsoft Windows -versiossa) tukevat ClickOnce-sovelluksia. Työnkulkueditorin ClickOnce-sovellus edellyttää 64-bittisen käyttöjärjestelmää.
> -   Taloushallinnon raportoinnin raportin suunnittelusovellus käynnistetään ClickOnce-sovelluksena. Se edellyttää 64-bittisen käyttöjärjestelmän kanssa yhteensopivaa järjestelmää. Jos käytössäsi on Chrome, sinun on asennettava ClickOnce-laajennus ladataksesi Report Designer -asiakasohjelman. Jos käytät Chromea Incognito-tilassa, varmista, että ClickOnce-laajennus on käytössä Incognito-tilassa.
> -   PDF-tiedostojen esikatseluun suosittelemme modernia verkkoselainta, kuten Microsoft Edgeä (uusin julkinen versio) Windows 10 -käyttöjärjestelmässä tai Google Chromea (uusin julkinen versio) Windows 10-, Windows 8.1-, Windows 8- tai Windows 7 -käyttöjärjestelmässä tai Google Nexus 10 -tabletissa.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS -sovelluksen tuetut selaimet

Vähittäismyynnin pilvimyyntipiste voidaan suorittaa seuraavissa selaimissa, joita käytetään määritetyissä käyttöjärjestelmissä:

-   Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
-   Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
-   Chrome (uusin julkaistu versio) Windows 10, Windows 8.1 tai Windows 7 -käyttöjärjestelmässä

## <a name="network-requirements"></a>Verkon vaatimukset
-   Finance and Operations on suunniteltu verkkoihin, joiden viive on enintään 250–300 millisekuntia (ms). Tämä viive on selainasiakasohjelman ja sen Microsoft Azure -palvelinkeskuksen välinen viive, joka isännöi Finance and Operationsia. On suositeltavaa testata verkon viive osoitteessa <http://www.azurespeed.com>.
-   Finance and Operationsin kaistanleveysvaatimus määräytyy tilanteen mukaan. Yleisimmät tilanteet vaativat yli 50 kilotavua sekunnissa (KBps) kaistanleveyttä. Suosittelemme kuitenkin suurempaa kaistanleveyttä tilanteissa, joissa hyötykuorman vaatimus on korkea, kuten työtiloissa, tai tilanteissa, joissa vaaditaan laajaa mukauttamista.

Finance and Operations on yleisesti optimoitu internet-käyttöön. Kyselyiden määrä selainasiakasohjelmasta Azure-palvelinkeskukseen on hyvin pieni, ja koko paketti on pakattu. 

> [!WARNING]
> Älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella. Tietyn sijainnin samanaikainen käyttö on hyvin vaikea laskea. Asiakkaat, jotka ovat huolissaan kaistanleveyden vaatimuksista, voivat käyttää Finance and Operationsin ennakkoversiota.

## <a name="net-framework-requirements"></a>.NET Framework -vaatimukset
Finance and Operations edellyttää Microsoft .NET Framework 4.6.2 -versiota kaikissa ClickOnce-sovelluksissa, kuten asiakirjan reititysagentissa. Asennusohjeet löydät kohdasta [.NET Frameworkin asentaminen](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Tuetut Microsoft Office -sovellukset
Seuraavia Microsoft Office -sovelluksia tuetaan Finance and Operationsin pilvikäyttöönotoissa ja paikallisissa käyttöönotoissa:

-   Microsoft Office 2016:n Windows- tai Mac-version on oltava asennettuna, jotta Microsoft Excel ja Word-lisäosia voi käyttää. Lisätietoja versiovaatimuksista on ohjeaiheessa [Office-integroinnin vianmääritys](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Microsoft Office 2007 tai sitä uudempi on oltava asennettuna, jotta voit tarkastella Vie Exceliin tai Vie Wordiin -toimintojen luomia asiakirjoja.

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS -vaatimukset

> [!NOTE]
> Jos Retail Modern POS käyttää offline-tietokantaa, tietokoneen on vastattava kaikkia Microsoft SQL Serverin järjestelmävaatimuksia. Retail Modern POS -offline-tietokantaa voi käyttää Microsoft SQL Server 2012 Service Pack 3:ssa tai uudemmassa, Microsoft SQL Server 2014 Service Pack 2:ssa tai uudemmassa ja Microsoft SQL Server 2016:ssa. Aina kannattaa käyttää uusinta käytettävissä olevaa versiota ja asentaa uusimmat Service Packit.

### <a name="supported-operating-systems"></a>Tuetut käyttöjärjestelmät

-   Retail Modern POS on 32-bittinen sovellus, mutta sen voi suorittaa sekä x86- että x64-arkkitehtuureilla.
-   Retail Modern POS on tuettu vain Windows 10 Pro, Enterprise ja Enterprise LTSB -versioissa.

### <a name="minimum-system-requirements"></a>Järjestelmän vähimmäisvaatimukset

-   Pienin tuettu näyttötarkkuus on 1280 × 1024.
-   Tietokoneen, jolla Retail Modern POS -sovellusta käytetään on vastattava seuraavia vaatimuksia:

    -   Siinä on oltava vähintään kaksiytiminen suoritin, jonka nopeus on vähintään 2 gigahertsiä (GHz).
    -   Siinä on oltava vähintään 3 gigatavua (Gt) keskusmuistia.
    -   Siinä on oltava internet-yhteys.

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

-   Connector for Microsoft Dynamics AX:ssä on kaksi erillistä asennusohjelmaa – toinen Async Server Connector -palvelua ja toinen Real-time Service for Dynamics AX 2012 R3 -palvelua varten.
-   Molemmat komponentit ovat 32-bittinen sovelluksia, mutta ne voi suorittaa sekä x86- että x64-arkkitehtuureilla.
-   Seuraavat käyttöjärjestelmät tukevat molempia komponentteja:

    -   Windows 7 Professional, Enterprise ja Ultimate
    -   Windows 8.1 Update 1 Professional, Enterprise ja Embedded
    -   Windows 10 Pro, Enterprise ja Enterprise LTSB
    -   Microsoft Windows Server 2012 R2 ja Microsoft Windows Server 2016

### <a name="minimum-system-requirements"></a>Järjestelmän vähimmäisvaatimukset
-   2 Gt RAM-muistia (suositus:, 4 Gt RAM-muistia)
-   1,6 GHz korkein ytimen suoritinnopeus (vähintään kaksi ydintä)
-   Vähintään 10 gigatavua vapaata tallennustilaa (kanavatietokanta voi vaatia paljon tallennustilaa)

## <a name="requirements-for-development-on-local-vms"></a>Vaatimukset paikalliseen kehitykseen virtuaalikoneessa
Lisätietoja paikallisesta virtuaalikoneessa (VMs) kehittämistä koskevista vaatimuksista on kohdassa [Paikalliset virtuaalikoneet](../dev-tools/access-instances.md).


## <a name="see-also"></a>Lisätietoja

[Dynamics 365 for Finance and Operations, Enterprise Editionin kokeiluversion hankkiminen](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

