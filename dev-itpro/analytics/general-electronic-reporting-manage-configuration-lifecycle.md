---
title: "Sähköisen raportoinnin konfiguraatioiden elinkaaren hallinta"
description: "Tässä aiheessa kuvataan, miten sähköiset raportointi (ER) kokoonpanojen toimintoja ratkaisun Microsoft Dynamics-365 elinkaaren hallintaan."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: f4d8994f6548119789715a4879b6bc02d25598e9
ms.lasthandoff: 03/31/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Sähköisen raportoinnin konfiguraatioiden elinkaaren hallinta

Tässä aiheessa kuvataan, miten sähköiset raportointi (ER) kokoonpanojen toimintoja ratkaisun Microsoft Dynamics-365 elinkaaren hallintaan.

<a name="overview"></a>Yleiskuvaus
--------

Sähköinen raportointi on moduuli, joka tukee lakisääteisiä ja maakohtaisia sähköisten asiakirjojen vaatimuksia Microsoft Dynamics 365 for Operations -järjestelmässä. Sähköisessä raportoinnissa oletuksena on se, että yksittäisille sähköisille asiakirjoille voidaan suorittaa seuraavat tehtävät. Lisätietoja on ohjeaiheessa [sähköisen raportoinnin yleiskuvaus](general-electronic-reporting.md).

-   Sähköisen asiakirjan malli suunnitteleminen:
    -   Tunnista vaaditut tietolähteet, jotka voidaan esittää asiakirjassa:
        -   Työvaiheiden tietoja, kuten arvotaulukot ja tietojen kohteiden luokkien pohjana Dynamics-365.
        -   Prosessi-kohtaisia ominaisuuksia, kuten suorituksen päivämäärä ja aika ja aikavyöhyke.
        -   Käyttäjän määrittämä suorituksen aikana käyttäjän syöteparametreja.
    -   Määrittele asiakirjassa tarvittavat osat ja niiden topologia, jotta voit määrittää asiakirjalle lopullisen muodon.
    -   Määritä haluamasi valituista tietolähteistä tuleva tietovirta määriteltyihin asiakirjan elementteihin (sitomalla tietolähteet asiakirjan muotokomponentteihin) ja määritä prosessinhallintalogiikka.
-   Julkaise malli käyttöön niin, että sitä voidaan käyttää muissa Dynamics 365 for Operations -esiintymissä:
    -   Muunna Dynamics 365 for Operations -järjestelmässä luotu asiakirjamalli sähköisen raportoinnin konfiguraatioon ja vie se nykyisestä Dynamics 365 for Operations -esiintymästä XML-pakettina, joka voidaan tallentaa joko paikallisesti tai LCS:ään.
    -   Muunna sähköisen raportoinnin konfiguraatio Dynamics 365 for Operations -asiakirjamalliksi.
    -   Tuo XML-paketti, joka tallennetaan paikallisesti tai LCS:ään nykyiseen Dynamics 365 for Operations -esiintymään.
-   Mukauta sähköisen asiakirjan mallia:
    -   Tuo malli sähköisen raportoinnin konfiguraationa LCS:stä nykyiseen Dynamics 365 for Operations -esiintymään.
    -   Suunnittele sähköisen raportoinnin konfiguraatiosta mukautettu versio, mutta säilytä viittaus perusversioon.
-   Integroi malli tiettyyn liiketoimintaprosessiin niin, että se on käytettävissä Dynamics 365 for Operations -järjestelmässä:
    -   Määritä Dynamics AX:n asetukset, jotta Dynamics 365 for Operations alkaa käyttää sähköisen raportoinnin konfiguraatiota, viittaamalla kyseiseen konfiguraatioon prosessiin liittyvällä parametrilla. Esimerkiksi viitata tiettyjen tilien ostoreskontran maksutapa, tuoda käsittelyyn laskujen sähköinen maksu virhesanoman ER-määrityksiä.
-   Käytä mallia määrätyssä liiketoimintaprosessissa:
    -   Suorittaa tietyn liiketoimintaprosessin ER-kokoonpano. Esimerkiksi voit tuoda virhesanoman sähköisen maksun käsittelyssä laskut kun maksutapa, joka viittaa ER-kokoonpano on valittuna.

## <a name="concepts"></a>Käsitteet
ER-kokoonpanon elinkaarta liittyvät seuraavat roolit ja aktiviteetit.

| Rooli                                       | Tehtävät                                                      | kuvaus                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sähköisen raportoinnin toiminnallinen konsultti | Sähköisen raportoinnin komponenttien (mallien ja muotojen) luonti ja hallinta.           | Liiketoiminnan henkilö, joka suunnittelee ER toimialueen tiedot – mallit, mallien edellyttää sähköisten asiakirjojen mallit ja sitoo vastaavasti.                                                                           |
| Sähköisen raportoinnin kehittäjä             | Tietomallien yhdistämismääritysten luonti ja hallinta.                          | Dynamics-365-toimintojen asiantuntija, joka valitsee toimintoja tietojen pakollinen Dynamics-365 tietolähteitä ja sitoo ne ER toimialueen tiedot – mallit.                                                                 |
| Taloushallintopäällikkö                      | Sähköisen raportoinnin artefakteihin viittaavien prosessiin liittyvien asetusten määrittäminen. | Esimerkiksi **Taloushallintopäällikkö** rooli, jonka avulla asetukset ER-määritys, jota käytetään erityisesti tileihin maksettavaa maksutapa luoda sähköinen maksu virhesanoman laskujen käsittelyyn. |
| Ostoreskontran maksuliikenneassistentti            | Sähköisen raportoinnin artefaktien käyttäminen määrätyssä liiketoimintaprosessissa.                | Esimerkiksi **tileille maksettavien maksujen virkailija** rooli, joka mahdollistaa viestien sähköinen maksu luodaan laskujen käsittely perustuu ER muotoilun, joka on määritetty tietylle maksutavalle.           |

## <a name="er-configuration-development-lifecycle"></a>Sähköisen raportoinnin konfiguraation kehityksen elinkaari
On suositeltavaa, että sähköisen raportoinnin konfiguraatiot suunnitellaan kehitysympäristössä erillisenä Dynamics 365 for Operations -esiintymänä seuraavista sähköiseen raportointiin liittyvistä syistä:

-   Käyttäjät, joilla on joko **Sähköisen raportoinnin kehittäjä**- tai **Sähköisen raportoinnin toiminnallinen konsultti** -rooli, voivat muokata konfiguraatioita ja suorittaa ne sitten testitarkoituksissa. Tämä skenaario saattaa aiheuttaa kutsuja luokkien tai taulujen menetelmistä, jotka voivat olla vahingollisia liiketoimintatiedoille ja erillisenä Dynamics 365 for Operations -esiintymän suorituskyvylle.
-   Dynamics 365 for Operations -aloituskohdat ja kirjattu yrityksen sisältö eivät rajoita luokkien ja taulujen menetelmien kutsuja sähköisen raportoinnin tietolähteinä tai konfiguraatioina. Niinpä käyttäjät, joilla on joko **Sähköisen raportoinnin kehittäjä**- tai **Sähköisen raportoinnin toiminnallinen konsultti** -rooli, voivat päästä käsiksi salassa pidettäviin tietoihin.

ER-kokoonpanoja, jotka on suunniteltu kehitysympäristössä voi ladata (oikea prosessi-integrointi, tulokset ja suorituskykyä oikeellisuuden) kokoonpanon arviointi ja laadunvarmistus rooliin perustuvia käyttöoikeuksia oikeellisuuden ja eriyttämisen testiympäristöön. ER kokoonpano vaihdon mahdollistavien ominaisuuksien voidaan käyttää tähän tarkoitukseen. Lopuksi hyviksi ER-kokoonpanoissa voidaan ladata LCS, josta ne voi jakaa palvelun tilaajat, tai tuotantoympäristöön sisäiseen käyttöön, kuten seuraavassa kuvassa näytetään. ![ER kokoonpanon elinkaarta](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Lisätietoja
--------

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)


