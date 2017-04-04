---
title: "Kirjanpidon kirjauskansion käsittely"
description: "Tässä artikkelissa kuvataan Microsoft Dynamics-365 saat toimintoihin, jotka auttavat Varmista yleisen päiväkirjan käsittelyn helpottamiseksi ja, jotka auttavat myös takaamaan, että oikeat tiedot on kerätty ja sisäinen valvonta ei vaarannu ominaisuuksista."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 50cd203025be8857de943e458fc32315e494fb7a
ms.lasthandoff: 03/31/2017


---

# <a name="general-journal-processing"></a>Kirjanpidon kirjauskansion käsittely

Tässä artikkelissa kerrotaan Microsoft Dynamics AX:n ominaisuuksista, joiden avulla yleisen kirjauskansion käsittely on helpompaa ja jonka avulla voidaan myös varmistaa, että kerättävät tiedot ovat oikeita eikä sisäisessä tarkistuksessa ole ongelmia.  

Kirjauskansioiden nimet

Kirjauskansioiden nimet on yksi tärkeimmistä alueiden määrittäminen. Se on hyvä tietyn kirjauskansion nimet kullekin tarkoitukseen, esimerkiksi yritysten kertymä muutos ja virheenkorjaus. Voit räätälöidä kullekin kirjauskansion nimelle helpottaa tiedonsyötön kunkin tarkoitukseen helposti ja turvallisesti. 

**Kirjauskansioiden nimet**-sivulla voit määrittää seuraavat elementit:

-   **Työnkulun hyväksyntä** – Sisäisen valvonnan parantamiseksi määritä kirjauskansion työnkulkuja, jotka muodostavat oleelliset rajat tarkastus- ja hyväksyntävaiheille perustuen ehtoihin, kuten veloituksen kokonaissummaan. Määritä yleiset kirjauskansiot työnkulut käyttöön ** kirjanpidon työnkulut ** sivu.
-   **Oletusarvot** – Valitse oletusarvo vastatileille, valuutoille ja taloushallinnon dimensioille.
-   **Kirjauskansion hallinta** – Voit määrittää yritystä, tilityyppiä ja segmenttiarvoja koskevia rajoituksia. 

**Esimerkkejä**

Kirjauskansion nimeä voidaan käyttää vain oikaisuihin. Tässä tapauksessa voit määrittää, että vain **Kirjanpito**-tilityyppi on kelvollinen kaikissa yhtiöissä. [![Ohjausobjektin Kirjauskansiotyypit](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Kirjauskansion nimeä voidaan käyttää vain määrätylle segmentille tai päätilien alueelle. [![Kirjauskansion hallinta-Segmentti](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Vaihtoehto **Automaattinen peruutus** on saatavilla yleisissä kirjauskansioissa. Sinulla voi esimerkiksi alla näkyvän esimerkin mukaisesti olla jaksotusoikaisu, jossa itse tiedostoa ei ole vielä käsitelty.
[![Yleisen päiväkirjan peruuttaminen](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excel-apuohjelman, päivyrimerkinnän, automaatio tarjoaa ja helpottaa tietojen kirjoittamista. Toiminto **Avaa rivit Excelissä **on saatavilla **Yleinen kirjauskansio-** ja **Kirjaustosite** -sivuilla. 

Voit määrittää toistuvia kirjauskansioita **Kausikirjauskansiot**-sivulla ja siten automatisoida kirjauskansion käsittelyn. 

Voit milloin tahansa Tositemallit. - **Yleisten päiväkirjojen** -sivulla **Tallenna** ja **Valitse tositemalli** toimintoja löytyy **tosite** sivun kohtaan **funktiot** tositteen rivien.

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

Lisätietoja on ohjeaiheessa [suunnittelu: tilikartan](plan-chart-of-accounts.md). 


