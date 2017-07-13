---
title: "Järjestelmävaatimukset"
description: "Tässä aiheessa on luettelo Microsoft Dynamics 365 for Finance and Operations Enterprise edition -ohjelman nykyisen version järjestelmävaatimuksista."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 724ee7ec29f8a9c4e8cc0b244193cd6c83c37f03
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Järjestelmävaatimukset
<a id="system-requirements" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tässä aiheessa on luettelo Microsoft Dynamics 365 for Finance and Operations Enterprise edition -ohjelman nykyisen version järjestelmävaatimuksista.

Tuetut selaimet
<a id="supported-web-browsers" class="xliff"></a>
----------------------

Verkkosovellus voidaan suorittaa seuraavissa selaimissa, joita käytetään määritetyissä käyttöjärjestelmissä:

-   Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
-   Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
-   Google Chrome (uusin saatavana oleva versio) Windows 10-, Windows 8.1-, Windows 8-, Windows 7- tai Google Nexus 10 -taulutietokoneen käyttöjärjestelmässä
-   Apple Safari (uusin saatavana oleva versio) Mac OS X 10.10 (Yosemite)-, 10.11 (El Capitan)-, 10.12 (Sierra)- tai Apple iPadin käyttöjärjestelmässä.

Ohjelmistovalmistajien sivustot sisältävät tietoja kunkin selaimen uusimmasta versiosta. 

**Huomautuksia:**

-   Chrome-laajennuksen ennakkojulkaisuversio pitää olla asennettuna, jotta voit tallentaa tehtävän tallennustoiminnon luomat kuvat ja sisällyttää ne Microsoft Word -asiakirjoihin. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
-   Työnkulkueditori käynnistetään ClickOnce-sovelluksena. Ainoastaan Microsoft Edge ja Internet Explorer (tuetussa Microsoft Windows -versiossa) tukevat ClickOnce-sovelluksia. Työnkulkueditorin ClickOnce-sovellus vaatii 64-bittisen käyttöjärjestelmän.
-   Taloushallinnon raportoinnin raportin suunnittelusovellus käynnistetään ClickOnce-sovelluksena. Siihen vaatii 64-bittisen käyttöjärjestelmän. Jos käytössäsi on Chrome, sinun on asennettava ClickOnce-laajennus ladataksesi raportin suunnittelun asiakasohjelman. Jos käytät Chromea incognito-tilassa, varmista, että ClickOnce-laajennus on käytössä incognito-tilassa.
-   PDF-tiedostojen esikatseluun suosittelemme modernia verkkoselainta, kuten Microsoft Edge (uusin julkinen versio) Windows 10 -käyttöjärjestelmässä tai Google Chrome (uusin julkinen versio) Windows 10, Windows 8.1, Windows 8 tai Windows 7 -käyttöjärjestelmässä tai Google Nexus 10 -taulutietokoneessa.


### Retail Cloud POS -sovelluksen tuetut selaimet
<a id="supported-web-browsers-for-retail-cloud-pos" class="xliff"></a>

Vähittäismyynnin pilvimyyntipiste voidaan suorittaa seuraavissa selaimissa, joita käytetään määritetyissä käyttöjärjestelmissä:

-   Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
-   Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
-   Chrome (uusin julkaistu versio) Windows 10, Windows 8.1 tai Windows 7 -käyttöjärjestelmässä

## Verkon vaatimukset
<a id="network-requirements" class="xliff"></a>
-   Dynamics 365 for Finance and Operations, Enterprise edition on suunniteltu verkkoja varten, joiden viive on 250–300 millisekuntia (ms) tai vähemmän. Tämä on viive selainasiakkaan ja Microsoftin Azure-datakeskuksen välillä, joka isännöi Finance and Operations -sovellusta. On suositeltavaa testata verkon viive osoitteessa <http://www.azurespeed.com>.
-   Kaistanleveyden vaatimukset riippuvat skenaariostasi. Yleisimmät tilanteet vaativat yli 50 kilotavua sekunnissa (KBps) kaistanleveyttä. Suosittelemme kuitenkin suurempaa kaistanleveyttä tilanteissa, joissa hyötykuorman vaatimus on korkea, kuten työtiloissa, tai tilanteissa, joissa vaaditaan laajaa mukauttamista.

Finance and Operations on yleisesti optimoitu Internet-käyttöön. Kyselyiden määrä selainasiakasohjelmasta Azure-datakeskukseen on hyvin pieni, ja koko paketti on pakattu. 

**Varoitus:** älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella. Tietyn sijainnin samanaikainen käyttö on vaikea laskea. Asiakkaat, jotka ovat huolissaan kaistanleveyden vaatimuksista voivat käyttää Finance and Operationsin ennakkoversiota.

## .NET Framework -vaatimukset
<a id="net-framework-requirements" class="xliff"></a>
.NET Framework -version 4.6.2 vaaditaan kaikille kerran klikattaville sovelluksille, kuten asiakirjan reititysagentille. Asennusohjeet löydät kohdasta [.NET Frameworkin asentaminen](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## Tuetut Microsoft Office -sovellukset
<a id="supported-microsoft-office-applications" class="xliff"></a>
-   Microsoft Office 2016:n Windows- tai Mac-version on oltava asennettuna, jotta Microsoft Excel ja Word-lisäosia voi käyttää. Lisätietoja versiovaatimuksista löydät kohdasta [Office-integroinnin vianmääritys](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Microsoft Office 2007 tai sitä uudempi on oltava asennettuna, jotta voit tarkastella Vie Exceliin tai Vie Wordiin -toimintojen luomia asiakirjoja.

## Retail Modern POS -vaatimukset
<a id="retail-modern-pos-requirements" class="xliff"></a>
### Tuetut käyttöjärjestelmät
<a id="supported-operating-systems" class="xliff"></a>

-   Retail Modern POS on 32-bittinen sovellus, mutta sen voi suorittaa sekä x86- että x64-arkkitehtuureilla.
-   Retail Modern POS on tuettu vain Windows 10 Pro, Enterprise ja Enterprise LTSB -versioissa.

### Järjestelmän vähimmäisvaatimukset
<a id="minimum-system-requirements" class="xliff"></a>

-   Pienin tuettu näyttötarkkuus on 1280 × 1024.
-   Tietokoneen, jolla Retail Modern POS -sovellusta käytetään on vastattava seuraavia vaatimuksia:
    -   Siinä on oltava vähintään kaksiytiminen suoritin, jonka nopeus on vähintään 2 gigahertsiä (GHz).
    -   Siinä on oltava vähintään 3 gigatavua (GB) keskusmuistia.
    -   Siinä on oltava Internet-yhteys.

## Retail hardware station -vaatimukset
<a id="retail-hardware-station-requirements" class="xliff"></a>
### Tuetut käyttöjärjestelmät
<a id="supported-operating-systems" class="xliff"></a>

-   Retail hardware station on 32-bittinen sovellus, mutta sen voi suorittaa sekä x86- että x64-arkkitehtuureilla.
-   Retail hardware station on tuettu seuraavissa käyttöjärjestelmissä:
    -   Windows 7 Professional, Enterprise ja Ultimate **Huomautus:** Windows 7 on tuettu vain, jos Internet Explorer 11 on asennettu järjestelmään manuaalisesti.
    -   Windows 8.1 Update 1 Professional, Enterprise ja Embedded
    -   Windows 10 Pro, Enterprise ja Enterprise LTSB

### Järjestelmän vähimmäisvaatimukset
<a id="minimum-system-requirements" class="xliff"></a>

Tietokoneen on täytettävä kaikki järjestelmän vähimmäisvaatimukset, jotta seuraavien kohteiden asennus ja käyttö on mahdollista:

-   IIS (Internet Information Services)
-   Kolmannen osapuolen laitteisto

## Vähittäismyymälän vähittäismyyntilaitteen vaatimukset
<a id="retail-store-scale-unit-requirements" class="xliff"></a>
### Tuetut käyttöjärjestelmät
<a id="supported-operating-systems" class="xliff"></a>

-   Vähittäismyymälän vähittäismyyntilaite on 32-bittinen sovellus, mutta sen voi suorittaa sekä x86- että x64-arkkitehtuureilla.
-   Vähittäismyymälän vähittäismyyntilaite on tuettu seuraavissa käyttöjärjestelmissä:
    -   Windows 7 Professional, Enterprise ja Ultimate
    -   Windows 8.1 Update 1 Professional, Enterprise ja Embedded
    -   Windows 10 Pro, Enterprise ja Enterprise LTSB

### Järjestelmän vähimmäisvaatimukset
<a id="minimum-system-requirements" class="xliff"></a>

-   4 Gt RAM-muistia
-   1,6 GHz korkein ytimen suoritinnopeus (vähintään kaksi ydintä)
-   Vähintään 10 gigatavua vapaata tallennustilaa (kanavatietokanta voi vaatia paljon tallennustilaa)

### Suositeltavat järjestelmävaatimukset
<a id="recommended-system-requirements" class="xliff"></a>

-   6 Gt RAM-muistia
-   2,4 GHz i7 (tai vastaava) ydinkohtainen suoritinnopeus (suositus on neljä ydintä)
-   Vähintään 10 gigatavua vapaata tallennustilaa (kanavatietokanta voi vaatia paljon tallennustilaa)

## Connectorin vaatimukset
<a id="connector-requirements" class="xliff"></a>
### Tuetut käyttöjärjestelmät
<a id="supported-operating-systems" class="xliff"></a>

-   Connector for Microsoft Dynamics AX:ssä on kaksi erillistä asennusohjelmaa, **Async Server Connector service** ja **Real-time service for Dynamics AX 2012 R3**.
-   Molemmat komponentit ovat 32-bittinen sovelluksia, mutta ne voi suorittaa sekä x86- että x64-arkkitehtuureilla.
-   Seuraavat käyttöjärjestelmät tukevat molempia komponentteja:
    -   Windows 7 Professional, Enterprise ja Ultimate
    -   Windows 8.1 Update 1 Professional, Enterprise ja Embedded
    -   Windows 10 Pro, Enterprise ja Enterprise LTSB
    -   Windows Server 2012 R2, Windows Server 2016

### Järjestelmän vähimmäisvaatimukset
<a id="minimum-system-requirements" class="xliff"></a>

-   2 GT RAM-muistia, 4 GT RAM-muistia suositellaan
-   1,6 GHz korkein ytimen suoritinnopeus (vähintään kaksi ydintä)
-   Vähintään 10 gigatavua vapaata tallennustilaa (kanavatietokanta voi vaatia paljon tallennustilaa)

## Vaatimukset paikalliseen kehitykseen virtuaalikoneessa
<a id="requirements-for-development-on-local-vms" class="xliff"></a>
Lisätietoja paikallisesta virtuaalikoneessa (VMs) kehittämistä koskevista vaatimuksista on kohdassa [Paikalliset virtuaalikoneet](../dev-tools/access-instances.md).

Lisätietoja
<a id="see-also" class="xliff"></a>
--------

[Dynamics 365 for Finance and Operations, Enterprise Editionin kokeiluversion hankkiminen](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)





