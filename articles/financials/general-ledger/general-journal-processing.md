---
title: Kirjanpidon kirjauskansion käsittely
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Finance and Operationsin ominaisuuksista, joiden avulla yleisen kirjauskansion käsittely on helpompaa ja jonka avulla voidaan myös varmistaa, että kerättävät tiedot ovat oikeita eikä sisäisessä tarkistuksessa ole ongelmia.
author: ShylaThompson
manager: AnnBe
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7efd250428f7675b96674dd02e3aeccefe653fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839228"
---
# <a name="general-journal-processing"></a>Kirjanpidon kirjauskansion käsittely

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Finance and Operationsin ominaisuuksista, joiden avulla yleisen kirjauskansion käsittely on helpompaa ja jonka avulla voidaan myös varmistaa, että kerättävät tiedot ovat oikeita eikä sisäisessä tarkistuksessa ole ongelmia.  

## <a name="journal-names"></a>Kirjauskansioiden nimet

Kirjauskansioiden nimet on yksi tärkeimmistä määritettävistä alueista. On hyvä ajatus määrittää määrätyt kirjauskansionimet kullekin tarkoitukselle, kuten konsernin sisäinen, jaksotusoikaisut ja virheiden korjaus. Voit räätälöidä kunkin kirjauskansion nimen niin, että tietojen lisäys kullekin tarkoitukselle on helppoa ja turvallista. 

**Kirjauskansioiden nimet**-sivulla voit määrittää seuraavat elementit:

-   **Työnkulun hyväksyntä** – Sisäisen valvonnan parantamiseksi määritä kirjauskansion työnkulkuja, jotka muodostavat oleelliset rajat tarkastus- ja hyväksyntävaiheille perustuen ehtoihin, kuten veloituksen kokonaissummaan. Voit määrittää työnkulkuja yleisille kirjauskansioille **Kirjanpidon työnkulut** -sivulla.
-   **Oletusarvot** – Valitse oletusarvo vastatileille, valuutoille ja taloushallinnon dimensioille.
-   **Kirjauskansion hallinta** – Voit määrittää yritystä, tilityyppiä ja segmenttiarvoja koskevia rajoituksia. 

**Esimerkkejä**

Kirjauskansion nimeä voidaan käyttää vain oikaisuihin. Tässä tapauksessa voit määrittää, että vain **Kirjanpito**-tilityyppi on kelvollinen kaikissa yhtiöissä. 

[![Kirjauskansion hallinnan tilityypit](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Kirjauskansion nimeä voidaan käyttää vain määrätylle segmentille tai päätilien alueelle. 

[![Kirjauskansion hallintasegmentti](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Vaihtoehto **Automaattinen peruutus** on saatavilla yleisissä kirjauskansioissa. Sinulla voi esimerkiksi alla näkyvän esimerkin mukaisesti olla jaksotusoikaisu, jossa itse tiedostoa ei ole vielä käsitelty.
[![Kirjauskansion takaisinkirjaukset](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excelin lisäosa kirjauskansiovientejä varten tarjoaa lisäautomaatiota ja tekee tietojen syötöstä helpompaa. Toiminto **Avaa rivit Excelissä** on saatavilla **Yleinen kirjauskansio-** ja **Kirjaustosite** -sivuilla. 

Voit määrittää toistuvia kirjauskansioita **Kausikirjauskansiot**-sivulla ja siten automatisoida kirjauskansion käsittelyn. 

Voit käyttää tositemalleja milloin tahansa. **Yleiset kirjauskansiot** -sivulla löytyy **Tallenna-** ja **Valitse tositemalli** -toiminnot **Kirjaustosite**-sivulla tositerivien kohdassa **Toiminnot**.

## <a name="related-setup"></a>Liittyvät asetukset
Seuraavat asetukset eivät koske pelkästään yleisiä kirjauskansioita vaan auttavat takaamaan, että oikeat tiedot tulevat kirjatuiksi ja että kirjaaminen on helppoa.

### <a name="main-account"></a>Päätili

Päätilin asetukset tarjoaa useita vaihtoehtoja yleisen kirjauskansion käsittelyyn:

-   **Veloitus-/Hyvitystarve** – Käytä tätä vaihtoehtoa, jos päätili on rajoitettu debet- tai kredit-tapahtumiin. Asetukset tarkistetaan, kun kirjauskansio vahvistetaan tai kirjataan.

-   **Oletusvastatili**
-   **Keskeytetty** – Keskeytä päätilille tehtävä tietojen kirjaaminen kaikkien tai tiettyjen yhtiöiden osalta.
-   **Älä salli manuaalista täyttämistä** – Estä käyttäjiä täyttämästä manuaalisesti tilin arvo kirjauskansioissa.
-   **Oletusvaluutta/valuutan vahvistaminen**
-   **Yrityksen ohitukset** – Nämä asetukset liittyvät kiinteästi määriteltyyn yritykseen:
    -   **Arvonlisäveron oletusarvo/vahvistaminen**
    -   **Oletusdimensio** – **Ei määritetty** tai **Kiinteä arvo**. **Kiinteä arvo** auttaa varmistamaan, että kaikki tälle päätilille tehtävät kirjaukset käyttävät aina dimensioarvoa, jonka tilaksi on määritetty **Kiinteä**.
-   **Kirjauksen oikeellisuustarkistus**
    -   **Käyttäjän oikeellisuustarkistus** – Tällä vaihtoehdolla valvotaan, millä käyttäjillä on oikeus tehdä kirjauksia päätilille.
    -   **Kirjaustyypin oikeellisuustarkistus** – Tällä vaihtoehdolla valvotaan, mitkä kirjaustyypit ovat sallittuja päätilillä.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Kirjanpitorakenteet ja lisäsääntöjen rakenteet

Kirjanpitorakenteet ja lisäsääntöjen rakenteet ovat erittäin tärkeitä sen varmistamisessa, että taloushallinnon raportoinnissa ja suorituskyvyn mittaamisessa tarvittavat tiedot ja asiakirjat kerätään kirjauskansion käsittelyn ja muun dokumentaation yhteydessä. Kirjanpitorakenteiden ja lisäsääntöjen rakenteiden ansiosta voit räätälöidä tietojen syöttörutiinin. Voit sallia tietojen syötön vain kussakin tilanteessa asianmukaisille taloushallinnon dimensioille sekä määrätä vaatimuksen siitä, että kerätään aina vaadittuja ja oikeita tietoja.

Lisätietoja on seuraavissa aiheissa:
- [Suunnittelu: tilikartta](plan-chart-of-accounts.md). 
- [Luo kirjauskansioiden lisäsäännöt](tasks/create-advanced-rules-journals.md)
- [Kirjauskansioviennin luonti mallin avulla](tasks/create-journal-entry-template.md)
- [Luo ja vahvista kirjauskansiot](tasks/create-validate-journals.md)
- [Kausittaisten kirjauskansioiden kirjaaminen](tasks/post-periodic-journals.md)
- [Käsittele kirjanpidon kohdistuskirjauskansio](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>Kirjauksen simulointi
Löydät **Kirjauksen simulointi** -kohdan useimpien kirjauskansioiden **Vahvista**-valikosta. Kun vahvistat kirjauskansion **Vahvista**-toiminnon avulla, järjestelmä testaa kirjauskansiota tiettyjen virhetilanteiden varalta. Jos käytät **Kirjauksen simulointi** -toimintoa, järjestelmä suorittaa kaikki samat prosessit, jotka suoritetaan kirjauksen aikana kirjauskansiota kirjaamatta. Voit siten tarkastella näytettyjä kirjausviestejä, korjata mahdollisesti löytämäsi virheet ja kirjata sitten kirjauskansion napsauttamalla **Kirjaa**. 

**Kirjauksen simulointi** ei ole käytettävissä eräkäsittelyä varten. Käytettävissä on kuitenkin koodi, jonka avulla voidaan simuloida eräkirjausta, ja kehittäjät voivat ulottaa koodin lisäämään tämän toiminnon.  
