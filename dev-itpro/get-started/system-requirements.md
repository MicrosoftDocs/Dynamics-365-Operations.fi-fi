---
title: "Järjestelmävaatimukset"
description: "Tässä aiheessa on luettelo Microsoft Dynamics 365 for Operations -ohjelman nykyisen version järjestelmävaatimuksista."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>Järjestelmävaatimukset

Tässä aiheessa on luettelo Microsoft Dynamics 365 for Operations -ohjelman nykyisen version järjestelmävaatimuksista.

<a name="supported-web-browsers"></a>Tuetut selaimet
----------------------

Microsoft Dynamics 365 for Operations -verkkosovellus voidaan suorittaa seuraavissa selaimissa, joita käytetään määritetyissä käyttöjärjestelmissä:

-   Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
-   Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
-   Google Chrome (uusin saatavana oleva versio) Windows 10-, Windows 8.1-, Windows 8-, Windows 7- tai Google Nexus 10 -taulutietokoneen käyttöjärjestelmässä
-   Apple Safari (uusin saatavana oleva versio) Mac OS X 10.10 (Yosemite)-, 10.11 (El Capitan)-, 10.12 (Sierra)- tai Apple iPadin käyttöjärjestelmässä.

Ohjelmistovalmistajien sivustot sisältävät tietoja kunkin selaimen uusimmasta versiosta. **Huomautuksia:**

-   Voit tallentaa tehtävän tallennustoiminnon luomat kuvat ja sisällyttää ne Microsoft Word -asiakirjoihin, jos asennettuna on Chrome-laajennus. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Työnkulkueditori käynnistetään ClickOnce-sovelluksena. Ainoastaan Microsoft Edge ja Internet Explorer (tuetussa Microsoft Windows -versiossa) tukevat ClickOnce-sovelluksia. Työnkulkueditorin ClickOnce-sovellus vaatii 64-bittisen käyttöjärjestelmän.
-   Taloushallinnon raportoinnin raportin suunnittelusovellus käynnistetään ClickOnce-sovelluksena. Siihen vaatii 64-bittisen käyttöjärjestelmän. Jos käytössäsi on Chrome, sinun on asennettava ClickOnce-laajennus ladataksesi raportin suunnittelun asiakasohjelman. Jos käytät Chromea incognito-tilassa, varmista, että ClickOnce-laajennus on käytössä incognito-tilassa.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS -sovelluksen tuetut selaimet

Microsoft Dynamics 365 for Operationsin Retail Cloud POS -sovellus voidaan suorittaa seuraavissa selaimissa, joita käytetään määritetyissä käyttöjärjestelmissä:

-   Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
-   Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
-   Chrome (uusin julkaistu versio) Windows 10, Windows 8.1 tai Windows 7 -käyttöjärjestelmässä

## <a name="network-requirements"></a>Verkon vaatimukset
-   Dynamics 365 for Operations on suunniteltu verkkoja varten, joiden viive on alle 150 millisekuntia (ms). Tämä on viive selainasiakkaan ja Microsoftin Azure-datakeskuksen välillä, joka isännöi Dynamics 365 for Operations -sovellusta. On suositeltavaa testata verkon viive osoitteessa <http://www.azurespeed.com>.
-   Dynamics 365 for Operationsin kaistanleveysvaatimus riippuu tilanteesta. Yleisimmät tilanteet vaativat yli 50 kilotavua sekunnissa (KBps) kaistanleveyttä. Suosittelemme kuitenkin suurempaa kaistanleveyttä tilanteissa, joissa hyötykuorman vaatimus on korkea, kuten työtiloissa, tai tilanteissa, joissa vaaditaan laajaa mukauttamista.

Dynamics 365 fir Operations on yleisesti optimoitu Internet-käyttöön. Kyselyiden määrä selainasiakasohjelmasta Azure-datakeskukseen on hyvin pieni, ja koko paketti on pakattu. **Varoitus:** älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella. Tietyn sijainnin samanaikainen käyttö on hyvin vaikea laskea. Asiakkaat, jotka ovat huolissaan kaistanleveyden vaatimuksista voivat käyttää Dynamics 365 for Operationsin ennakkoversiota.

## <a name="net-framework-requirements"></a>.NET Framework -vaatimukset
Dynamics 365 for Operations vaatii .NET Framework -version 4.6.2 kaikille kerran klikattaville sovelluksille, kuten asiakirjan reititysagentille. Asennusohjeet löydät kohdasta [.NET Frameworkin asentaminen](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Tuetut Microsoft Office -sovellukset
-   Microsoft Office 2016:n Windows- tai Mac-version on oltava asennettuna, jotta Microsoft Excel ja Word-lisäosia voi käyttää. Lisätietoja versiovaatimuksista löydät kohdasta [Office-integroinnin vianmääritys](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Microsoft Office 2007 tai sitä uudempi on oltava asennettuna, jotta voit tarkastella Vie Exceliin tai Vie Wordiin -toimintojen luomia asiakirjoja.

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
    -   Windows 7 Professional, Enterprise ja Ultimate **Huomautus:** Windows 7 on tuettu vain, jos Internet Explorer 11 on asennettu järjestelmään manuaalisesti.
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

## <a name="requirements-for-development-on-local-vms"></a>Vaatimukset paikalliseen kehitykseen virtuaalikoneessa
Lisätietoja paikallisesta virtuaalikoneessa (VMs) kehittämistä koskevista vaatimuksista on kohdassa [Paikalliset virtuaalikoneet](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Lisätietoja
--------

[Hae Dynamics 365 for Operationsin kokeiluversio](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


