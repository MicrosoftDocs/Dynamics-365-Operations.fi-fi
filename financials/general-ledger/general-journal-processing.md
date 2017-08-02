---
title: "Kirjanpidon kirjauskansion käsittely"
description: "Tässä artikkelissa kerrotaan Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin ominaisuuksista, joiden avulla yleisen kirjauskansion käsittely on helpompaa ja jonka avulla voidaan myös varmistaa, että kerättävät tiedot ovat oikeita eikä sisäisessä tarkistuksessa ole ongelmia."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 244eada4202106b65198e3d6e3d0dedaa5486632
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# <a name="general-journal-processing"></a>Kirjanpidon kirjauskansion käsittely

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin ominaisuuksista, joiden avulla yleisen kirjauskansion käsittely on helpompaa ja jonka avulla voidaan myös varmistaa, että kerättävät tiedot ovat oikeita eikä sisäisessä tarkistuksessa ole ongelmia.  

Kirjauskansioiden nimet

Kirjauskansioiden nimet on yksi tärkeimmistä määritettävistä alueista. On hyvä ajatus määrittää määrätyt kirjauskansionimet kullekin tarkoitukselle, kuten konsernin sisäinen, jaksotusoikaisut ja virheiden korjaus. Voit räätälöidä kunkin kirjauskansion nimen niin, että tietojen lisäys kullekin tarkoitukselle on helppoa ja turvallista. 

**Kirjauskansioiden nimet**-sivulla voit määrittää seuraavat elementit:

-   **Työnkulun hyväksyntä** – Sisäisen valvonnan parantamiseksi määritä kirjauskansion työnkulkuja, jotka muodostavat oleelliset rajat tarkastus- ja hyväksyntävaiheille perustuen ehtoihin, kuten veloituksen kokonaissummaan. Voit määrittää työnkulkuja yleisille kirjauskansioille **Kirjanpidon työnkulut** -sivulla.
-   **Oletusarvot** – Valitse oletusarvo vastatileille, valuutoille ja taloushallinnon dimensioille.
-   **Kirjauskansion hallinta** – Voit määrittää yritystä, tilityyppiä ja segmenttiarvoja koskevia rajoituksia. 

**Esimerkkejä**

Kirjauskansion nimeä voidaan käyttää vain oikaisuihin. Tässä tapauksessa voit määrittää, että vain **Kirjanpito**-tilityyppi on kelvollinen kaikissa yhtiöissä. [![Kirjauskansion hallinnan tilityypit](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Kirjauskansion nimeä voidaan käyttää vain määrätylle segmentille tai päätilien alueelle. [![Kirjauskansion hallintasegmentti](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Vaihtoehto **Automaattinen peruutus** on saatavilla yleisissä kirjauskansioissa. Sinulla voi esimerkiksi alla näkyvän esimerkin mukaisesti olla jaksotusoikaisu, jossa itse tiedostoa ei ole vielä käsitelty.
[![Kirjauskansion takaisinkirjaukset](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excelin lisäosa kirjauskansiovientejä varten tarjoaa lisäautomaatiota ja tekee tietojen syötöstä helpompaa. Toiminto **Avaa rivit Excelissä** on saatavilla **Yleinen kirjauskansio-** ja **Kirjaustosite** -sivuilla. 

Voit määrittää toistuvia kirjauskansioita **Kausikirjauskansiot**-sivulla ja siten automatisoida kirjauskansion käsittelyn. 

Voit käyttää tositemalleja milloin tahansa. **Yleiset kirjauskansiot** -sivulla löytyy **Tallenna-** ja **Valitse tositemalli** -toiminnot **Kirjaustosite**-sivulla tositerivien kohdassa **Toiminnot**.

## <a name="related-setup"></a>Liittyvät asetukset
Seuraavat asetukset eivät koske nimenomaan yleisiä kirjauskansioita, mutta ne auttavat takaamaan, että oikeat tiedot tulevat kirjatuiksi ja että kirjaaminen on helppoa.

### <a name="main-account"></a>Päätili

Päätilin asetukset tarjoaa useita vaihtoehtoja yleisen kirjauskansion käsittelyyn:

-   **Veloitus-/Hyvitystarve** – Käytä tätä vaihtoehtoa, jos päätili on rajoitettu debet- tai kredit-tapahtumiin. Asetukset tarkistetaan, kun kirjauskansio vahvistetaan tai kirjataan.
-   **Oletusvastatili**
-   **Keskeytetty** – Keskeytä päätilille tehtävä tietojen kirjaaminen kaikkien yhtiöiden osalta tai määrättyjen yritysten osalta.
-   **Älä salli manuaalista täyttämistä** – Estä käyttäjiä täyttämästä manuaalisesti tilin arvo kirjauskansioissa.
-   **Oletusvaluutta/valuutan vahvistaminen**
-   **Yrityksen ohitukset** – Nämä asetukset liittyvät kiinteästi määriteltyyn yritykseen:
    -   **Arvonlisäveron oletusarvo/vahvistaminen**
    -   **Oletusdimensio** – **Ei määritetty** tai **Kiinteä arvo**. **Kiinteä arvo** auttaa varmistamaan, että kaikki tälle päätilille tehtävät kirjaukset käyttävät aina dimensioarvoa, joka on määritetty **Kiinteäksi**.
-   **Kirjauksen oikeellisuustarkistus**
    -   **Käyttäjän oikeellisuustarkistus** – Tällä vaihtoehdolla valvotaan, millä käyttäjillä on oikeus tehdä kirjauksia päätilille.
    -   **Kirjaustyypin oikeellisuustarkistus** – Tällä vaihtoehdolla valvotaan, mitkä kirjaustyypit ovat sallittuja päätilillä.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Kirjanpitorakenteet ja lisäsääntöjen rakenteet

Kirjanpitorakenteet ja lisäsääntöjen rakenteet ovat erittäin tärkeitä sen varmistamisessa, että taloushallinnon raportoinnissa ja suorituskyvyn mittaamisessa tarvittavat tiedot ja asiakirjat kerätään kirjanpidon kirjauskansion käsittelyn yhteydessä. Kirjanpitorakenteiden ja lisäsääntöjen rakenteiden ansiosta voit räätälöidä tietojen syöttörutiinin. Voit sallia tietojen syötön vain kussakin tilanteessa asianmukaisille taloushallinnon dimensioille sekä toimeenpanna vaatimuksen, että pakolliset ja oikeat tiedot tulevat aina kerätyiksi.

Lisätietoja on ohjeaiheessa [Suunnittelu: tilikartta](plan-chart-of-accounts.md). 




