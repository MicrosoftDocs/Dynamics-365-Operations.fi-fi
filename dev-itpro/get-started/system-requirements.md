---
title: "Järjestelmävaatimukset"
description: "Tässä aiheessa luetellaan Microsoft Dynamics-365 toimintojen nykyisen version järjestelmävaatimukset."
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

Tässä aiheessa luetellaan Microsoft Dynamics-365 toimintojen nykyisen version järjestelmävaatimukset.

<a name="supported-web-browsers"></a>Tuetut selaimet
----------------------

Microsoft Dynamics-365 WWW-sovelluksen toimintoja voidaan suorittaa seuraavia web-selaimia, jotka suoritetaan määritetyn käyttöjärjestelmissä:

-   Microsoft-Edge (uusin yleisesti saatavilla olevan version) Windows-10
-   Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
-   Google Chrome (uusin versio yleisesti saatavilla) Windows-10, Windows 8.1, Windows 8, Windows 7 tai Google Nexus 10 Tablet-PC: n
-   Apple Safari (uusin versio yleisesti saatavilla) Mac OS X (Yosemite) 10.10, 10.11 (El Capitan) tai 10.12 (Sierra) tai Apple iPad

Ohjelmistovalmistajien sivustot sisältävät tietoja kunkin selaimen uusimmasta versiosta. **Huomautuksia:**

-   Jos haluat siepata kuvia, jotka on luotu tehtävän tallennus ja sisällyttää Microsoft Word-asiakirjoja, asennettu Chrome tunnisteen on oltava. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   ClickOnce-sovellus käynnistetään työnkulkueditori. Tue ClickOnce-sovellukset Microsoft Edge ja Internet Explorer (tuettu Microsoft Windowsin versio). 64-bittinen yhteensopiva käyttöjärjestelmä vaatii työnkulkueditori ClickOnce-sovelluksen.
-   ClickOnce-sovellus käynnistetään Report Designer taloudelliseen raportointiin. Siihen tarvitaan 64-bittinen yhteensopiva käyttöjärjestelmä. Jos käytät Chrome, jotta voit ladata raportin suunnittelun asiakasohjelma on asennettava ClickOnce-tunniste. Jos käytät Chrome incognito-tilassa, varmista, että ClickOnce-laajennus on käytössä myös incognito-tilassa.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS -sovelluksen tuetut selaimet

Cloud Vähittäismyyntipisteen Dynamics 365 toimintoihin voidaan suorittaa seuraavia web-selaimia, jotka suoritetaan määritetyn käyttöjärjestelmissä:

-   Microsoft-Edge (uusin yleisesti saatavilla olevan version) Windows-10
-   Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
-   Chrome (uusin versio yleisesti saatavilla) Windows 10, Windows 7 tai Windows 8.1

## <a name="network-requirements"></a>Verkkovaatimukset
-   Dynamics 365 toimintoja varten on suunniteltu verkkojen viive (ms) alle 150 millisekuntia. Tämä on Microsoftin Azure data center, joka isännöi Dynamics 365 operaatioille, selaimen asiakasohjelmassa viive. On suositeltavaa testata verkon viiveestä, <http://www.azurespeed.com>.
-   Työvaiheiden 365 Dynamics kaistanleveysvaatimukset riippuu tilannetta. Yleisimmät skenaariot vaativat kaistanleveyttä yli 50 kilotavua sekunnissa (KBps). Kuitenkin tilanteissa, joissa on suuri hyötykuorma vaatimukset, esimerkiksi työtiloja tai skenaarioita, joihin liittyy laajoja customization suositellaan enemmän kaistanleveyttä.

Dynamics 365 toiminnoissa on yleensä optimoitu Internet. Edestakaiset matkat selaimen asiakasohjelmassa Azure, data center määrä on hyvin pieni, ja koko paketti on pakattu. **Varoitus:** ei laske kaistanleveyden vaatimukset asiakkaan sijainnista käyttäjien määrä kertomalla pienin kaistanleveyden vaatimukset. Samanaikainen käyttö tietyssä paikassa, on hyvin vaikea laskea. Asiakkaat, jotka ovat huolissaan kaistanleveyden vaatimukset käyttää Dynamics 365 preview-version toimintoja.

## <a name="net-framework-requirements"></a>.NET framework-vaatimukset
Työvaiheiden 365 Dynamics edellyttää .NET Framework 4.6.2 kaikki napsauttamalla-kerran sovellukset, kuten asiakirjan reitityksen agentti. Asennus ohjeet [.NET Frameworkin asentaminen](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Tuetut Microsoft Office-sovellukset
-   Microsoft Excel- ja Word-apuohjelmien suorittamiseen on oltava asennettuna Microsoft Officen 2016 Windows tai Mac. Saat lisätietoja versiovaatimukset [Office-integroinnin vianmääritys](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Vienti Exceliin tai Word-toimintojen avulla luodut asiakirjojen näyttämiseen tarvitaan Microsoft Office 2007 tai uudempi.

## <a name="retail-modern-pos-requirements"></a>Retail POS nykyaikaiset vaatimukset
### <a name="supported-operating-systems"></a>Tuetut käyttöjärjestelmät

-   Retail POS-Sovelluksen Moderni on 32-bittinen sovellus, mutta se suoritetaan palvelimella sekä x86 että x64.
-   Retail POS-Sovelluksen Moderni tuetaan vain Windows 10 Pro, yrityksen ja yrityksen pitkän aikavälin ylläpidon haara (LTSB) versiot.

### <a name="minimum-system-requirements"></a>Järjestelmän vähimmäisvaatimukset

-   Pienin tuettu tarkkuus on 1280 × 1024.
-   Tietokone, joka toimii Retail POS-Sovelluksen Moderni on vastattava seuraavia vaatimuksia:
    -   Sillä on oltava, ainakin kaksiytiminen suoritin, joka suoritetaan aikaisintaan 2 gigahertsin (GHz).
    -   Sillä on oltava, ainakin 3 gigatavua (gt) RAM-muistia.
    -   Sillä on oltava Internet-yhteys.

## <a name="retail-hardware-station-requirements"></a>Vähittäismyynnin aseman laitteistovaatimukset
### <a name="supported-operating-systems"></a>Tuetut käyttöjärjestelmät

-   Vähittäismyynnin laitteiston station on 32-bittinen sovellus, mutta se suoritetaan palvelimella sekä x86 että x64.
-   Vähittäismyynnin laitteiston station tuetaan seuraavissa käyttöjärjestelmissä:
    -   Windows 7 Professional-, Enterprise- ja Ultimate-versiot **Huomautus:** Windows 7 tukee vain, jos järjestelmään asennetaan manuaalisesti Internet Explorerin 11.
    -   Windows 8.1 Update 1 Professional, Enterprise ja upotettu versiot
    -   Windows 10 Pro-, yritys- ja yrityksen LTSB versiot

### <a name="minimum-system-requirements"></a>Järjestelmän vähimmäisvaatimukset

Tietokoneen on täytettävä kaikki järjestelmän vähimmäisvaatimukset asentamisen ja käyttämisen seuraavat kohteet:

-   IIS (Internet Information Services)
-   Kolmannen osapuolen laitteisto

## <a name="retail-store-scale-unit-requirements"></a>Retail Store-asteikon aikayksikön vaatimukset
### <a name="supported-operating-systems"></a>Tuetut käyttöjärjestelmät

-   Retail Store asteikon yksikkö on 32-bittinen sovellus, mutta se suoritetaan palvelimella sekä x86 että x64.
-   Retail Store-asteikon aikayksikön tuetaan seuraavissa käyttöjärjestelmissä:
    -   Windows 7 Professional-, Enterprise- ja Ultimate-versiot
    -   Windows 8.1 Update 1 Professional, Enterprise ja upotettu versiot
    -   Windows 10 Pro-, yritys- ja yrityksen LTSB versiot

### <a name="minimum-system-requirements"></a>Järjestelmän vähimmäisvaatimukset

-   4 gt RAM-muistia
-   Per core 1,6 GHz: N huippu suorittimen nopeus (kaksi porausnäytettä on pienin).
-   On vähintään 10 Gigatavua vapaata tilaa (kanava-tietokantaan, voit vaatia paljon tilaa.)

### <a name="recommended-system-requirements"></a>Suositeltavat järjestelmävaatimukset

-   6 gt RAM-Muistia
-   2.4 GHz i7 (tai vastaava) huippu suorittimen nopeus per core (neljän porausnäytteet suositellaan.)
-   On vähintään 10 Gigatavua vapaata tilaa (kanava-tietokantaan, voit vaatia paljon tilaa.)

## <a name="requirements-for-development-on-local-vms"></a>VMs paikallista kehittämistä koskevat vaatimukset
Lisätietoja paikallisen virtuaalikoneet (VMs)-kehittämistä koskevat vaatimukset on [VM käynnissä paikallisen](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Lisätietoja
--------

[Saat toiminnot Dynamics 365 arviointiversio](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


