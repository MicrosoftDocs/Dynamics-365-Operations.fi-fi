---
title: "Sähköisen raportoinnin konfiguraatioiden elinkaaren hallinta"
description: "Tässä ohjeaiheessa käsitellään sähköisen raportoinnin konfiguraatioiden elinkaaren hallintaa Dynamics 365 for Finance and Operations -ratkaisussa."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: eecd53d181a086a5cf295f54f9fa72aa2960c272
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Sähköisen raportoinnin konfiguraatioiden elinkaaren hallinta

[!INCLUDE [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään sähköisen raportoinnin konfiguraatioiden elinkaaren hallintaa Dynamics 365 for Finance and Operations -ratkaisussa.

<a name="overview"></a>Yleiskuvaus
--------

Sähköinen raportointi on moduuli, joka tukee lakisääteisiä ja maakohtaisia sähköisten asiakirjojen vaatimuksia Microsoft Dynamics 365 for Finance and Operationsissa. Sähköisessä raportoinnissa oletuksena on se, että yksittäisille sähköisille asiakirjoille voidaan suorittaa seuraavat tehtävät. Lisätietoja on ohjeaiheessa [sähköisen raportoinnin yleiskuvaus](general-electronic-reporting.md).

-   Sähköisen asiakirjan malli suunnitteleminen:
    -   Tunnista vaaditut tietolähteet, jotka voidaan esittää asiakirjassa:
        -   Finance and Operationsin taustatiedot, kuten tietotaulukot, tietoyksiköt ja luokat.
        -   Prosessikohtaiset ominaisuudet (suorituspäivämäärä ja -aika sekä aikavyöhyke).
        -   Käyttäjän syöttöparametrit (loppukäyttäjä määrittää suorituksen aikana).
    -   Määrittele asiakirjassa tarvittavat osat ja niiden topologia, jotta voit määrittää asiakirjalle lopullisen muodon.
    -   Määritä haluamasi valituista tietolähteistä tuleva tietovirta määriteltyihin asiakirjan elementteihin (sitomalla tietolähteet asiakirjan muotokomponentteihin) ja määritä prosessinhallintalogiikka.
-   Julkaise malli käyttöön niin, että sitä voidaan käyttää muissa Finance and Operations -esiintymissä:
    -   Muunna Finance and Operationsissa luotu asiakirjamalli sähköisen raportoinnin konfiguraatioon ja vie se nykyisestä Finance and Operations -esiintymästä XML-pakettina, joka voidaan tallentaa joko paikallisesti tai LCS:ään.
    -   Muunna sähköisen raportoinnin konfiguraatio Finance and Operations -asiakirjamalliksi.
    -   Tuo XML-paketti, joka tallennetaan paikallisesti tai LCS:ään nykyiseen Finance and Operations -esiintymään.
-   Mukauta sähköisen asiakirjan mallia:
    -   Tuo malli sähköisen raportoinnin konfiguraationa LCS:stä nykyiseen Finance and Operations -esiintymään.
    -   Suunnittele sähköisen raportoinnin konfiguraatiosta mukautettu versio, mutta säilytä viittaus perusversioon.
-   Integroi malli tiettyyn liiketoimintaprosessiin niin, että se on käytettävissä Finance and Operationsissa:
    -   Määritä asetukset siten, että Finance and Operations alkaa käyttää sähköisen raportoinnin konfiguraatiota, viittaamalla kyseiseen konfiguraatioon prosessiin liittyvällä parametrilla. Voit esimerkiksi viitata sähköisen raportoinnin konfiguraatioon tietyssä ostoreskontran maksumenetelmässä, jos haluat luoda sähköisen maksuviestin laskujen käsittelyä varten.
-   Käytä mallia määrätyssä liiketoimintaprosessissa:
    -   Suorita sähköisen raportoinnin konfiguraatio määrätyssä liiketoimintaprosessissa. Voit esimerkiksi viitata sähköisen raportoinnin konfiguraatioon tietyssä ostoreskontran maksumenetelmässä, jos haluat luoda sähköisen maksuviestin laskujen käsittelyä varten.

## <a name="concepts"></a>Käsitteet
Sähköisen raportoinnin konfiguraatioiden elinkaareen liittyvät seuraavat roolit ja tehtävät.

| Rooli                                       | Tehtävät                                                      | kuvaus                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sähköisen raportoinnin toiminnallinen konsultti | Sähköisen raportoinnin komponenttien (mallien ja muotojen) luonti ja hallinta.           | Yrityksessä työskentelevä henkilö, joka suunnittelee sähköisen raportoinnin toimialuekohtaisia tietomalleja, suunnittelee sähköisissä asiakirjoissa tarvittavat mallit ja liittää ne vastaavasti.                                                                           |
| Sähköisen raportoinnin kehittäjä             | Tietomallien yhdistämismääritysten luonti ja hallinta.                          | Finance and Operations -asiantuntija, joka valitsee tarvittavat Finance and Operations -tietolähteet ja sitoo ne sähköisen raportoinnin toimialuekohtaisiin tietomalleihin.                                                                 |
| Taloushallintopäällikkö                      | Sähköisen raportoinnin artefakteihin viittaavien prosessiin liittyvien asetusten määrittäminen. | Esimerkiksi **Taloushallintopäällikkö**-rooli, joka sallii sähköisen raportoinnin konfiguraation asetusten käyttämisen tietyssä ostoreskontran maksumenetelmässä sähköisen maksuviestin luomiseksi laskujen käsittelyä varten. |
| Ostoreskontran maksuliikenneassistentti            | Sähköisen raportoinnin artefaktien käyttäminen määrätyssä liiketoimintaprosessissa.                | Esimerkiksi **Ostoreskontran maksuliikenneassistentti** -rooli, joka sallii sähköisten maksuviestien luomisen laskujen käsittelyä varten tietylle maksutavalle määritetyn sähköisen raportoinnin muodon perusteella.           |

## <a name="er-configuration-development-lifecycle"></a>Sähköisen raportoinnin konfiguraation kehityksen elinkaari
On suositeltavaa, että sähköisen raportoinnin konfiguraatiot suunnitellaan kehitysympäristössä erillisenä Finance and Operations -esiintymänä seuraavista sähköiseen raportointiin liittyvistä syistä:

-   Käyttäjät, joilla on joko **Sähköisen raportoinnin kehittäjä**- tai **Sähköisen raportoinnin toiminnallinen konsultti** -rooli, voivat muokata konfiguraatioita ja suorittaa ne sitten testitarkoituksissa. Tämä skenaario saattaa aiheuttaa kutsuja luokkien tai taulujen menetelmistä, jotka voivat olla vahingollisia liiketoimintatiedoille ja Finance and Operations -esiintymän suorituskyvylle.
-   Finance and Operations -aloituskohdat ja kirjattu yrityksen sisältö eivät rajoita luokkien ja taulujen menetelmien kutsuja sähköisen raportoinnin tietolähteinä tai konfiguraatioina. Niinpä käyttäjät, joilla on joko **Sähköisen raportoinnin kehittäjä**- tai **Sähköisen raportoinnin toiminnallinen konsultti** -rooli, voivat päästä käsiksi salassa pidettäviin tietoihin.

Kehitysympäristössä suunnitellut sähköisen raportoinnin konfiguraatiot voidaan ladata testiympäristöön konfiguraation arviointia (oikea prosessi-integraatio, tulosten oikeellisuus, suorituskyky) ja laadunvarmistusta (roolipohjaisten käyttöoikeuksien oikeellisuus, tehtävien eriyttäminen jne.) varten. Tähän tarkoitukseen voidaan käyttää toimintoja, jotka sallivat sähköisen raportoinnin konfiguraatioiden vaihdon. Lopuksi testatut sähköisen raportoinnin konfiguraatiot voidaan ladata joko LCS:ään, jossa ne voidaan jakaa palvelun tilaajille, tai tuotantoympäristöön sisäiseen käyttöön, kuten seuraavassa kaaviossa. ![ER-konfiguraation elinkaari](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Lisätietoja
--------

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)




