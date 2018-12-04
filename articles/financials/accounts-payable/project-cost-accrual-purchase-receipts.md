---
title: Projektikustannusten jaksottaminen ostojen vastaanotoissa
description: "Tässä ohjeaiheessa kerrotaan, miten ostojen vastaanottojen jaksotetut projektikustannuksia voidaan seurata Microsoft Dynamics 365 for Finance and Operationsissa."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 9a74b684e955376b9c3036954f4a6e6628c468f0
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Projektikustannusten jaksottaminen ostojen vastaanotoissa

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten ostojen vastaanottojen jaksotetut projektikustannuksia voidaan seurata Microsoft Dynamics 365 for Finance and Operationsissa. 

Projektin laskut saapuvat usein tavaroiden ja palveluiden toimituksen jälkeen. Tällä saattaa olla merkittävä vaikutus projektin suorituskykyilmaisimiin. On tärkeää, että näitä tapahtumia pystytään seuraamaan sekä tilinpäätöksissä että projektiraporteissa.

Seuraava esimerkki havainnollistaa tätä. 

Contoso Consulting on aloittanut uuden pilvikehitysprojektin. Luodaan ostotilaus tietokoneen ostamiseksi projektia varten. Tietokone maksaa 1 500 euroa ja asennuspalvelut 150 euroa. Toimittaja on toimittanut ja asentanut tietokoneen, mutta Contoso Consulting ei ole vielä saanut laskua. Projektipäällikkö haluaa tarkastella projektikustannusten 1 650 euron jaksottamista ennen laskun toimitusta. Kustannusten tulee vastata yrityksen kuukauden lopun tilinpäätöksiä. 

Jaksotettu kustannus on tallennettava raportoinnissa sekä taloushallinnon tasolla että projektitasolla. Finance and Operationsin tuotteen vastaanoton nimike- ja hankintaluokkien maksupäivitystä voidaan seurata. 

Valitse nimikkeille **Ostoreskontran parametrit** -sivulla **Kirjaa tuotteen vastaanotot kirjanpitoon** -vaihtoehto.
[![jaksotukset1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Valitse hankintaluokille **Luokan käytäntösääntö** -sivulla **ostokäytännöt** ja valitse sitten jokaiselle hankintaluokalle **Jaksota ostokulut vastaanoton yhteydessä** -kohta.
[![jaksotukset2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

**Kirjausasetukset**-kohdassa olevia **Ostomeno, laskuttamaton**- ja **Osto, jaksotus** -tilejä käytetään, kun tuotteen vastaanottoon liittyvät tositteen kirjataan.
[![jaksotukset3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Käytetään samaa skenaariota ja tarkastellaan, miten tuotteen vastaanotto vaikuttaa kirjanpitoon ja projektin tietoihin. 

**Vaihe 1:** Luodaan ja vahvistetaan projektille uusi ostotilaus 1 500 euroa maksaneen tietokoneen ja 150 euroa maksaneiden asennuspalveluiden oston tallentamista varten.
[![jaksotukset4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Kun ostotilaus vahvistetaan, projektille luodaan sidotun kustannuksen tapahtumat. 
[![jaksotukset5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Sidotun kustannuksen tapahtumien **Tapahtuman alkuperä** -kentän arvoksi on määritetty **Ostotilaus**. Projektille ei luoda tapahtumia ostotilauksen luomisen ja vahvistamisen yhteydessä. 

**Vaihe 2:** Tavarat ja palvelut toimitetaan ja tuotteen vastaanotto rekisteröidään. 

Tuotteen vastaanoton kirjaamisen yhteydessä luodaan tosite ja kirjataan se kirjanpitoon. Tosite veloittaa ostomenoa, laskuttamatonta tiliä, ja hyvittää jaksotusmenetelmän tiliä. 
[![jaksotukset6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Tuotteen vastaanoton kirjaamisessa käytetään hankintaluokkien ja tuotteiden kirjausasetuksia projektiluokkien kirjausasetusten sijaan. Nämä asetukset on kohdistettava, jotta taloudellinen vaikutus ostojen jaksotukseen on oikea. 

Hankintaluokat on mahdollista yhdistää projektiluokkiin **Hankintaluokka**-sivulla.
[![jaksotukset7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Vaihe 3:** Luo toimittajan laskuluonnos. 

Tuotteen kirjaaminen Finance and Operationsiin ei vaikuta projektin tietoihin. Voit välttää ongelman luomalla toimittajan luonnoslaskun myös heti oston vastaanoton kirjaamisen jälkeen. Siirry kohtaan **Ostolasku**-sivu &gt; **Lasku-välilehti** &gt; **Luo** &gt; **Lasku**. Tämä luo odottavan laskuasiakirjan, joka päivittää projektin tiedot. 

Toimittajan laskuluonnoksen luominen luo odottavia projektitapahtumia. 
[![jaksotukset8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

**Sidottu kustannus** -sivulla vaiheessa 1 luodut tietueet suljetaan. Tämän jälkeen luodaan uudet tietueet, jotka vastaavat odottavista toimittajan laskuista saatavia kustannussitoumuksia. Sidotun kustannuksen **Tapahtuman alkuperä** -kentän arvoksi määritetään **Toimittajan lasku**.
[![jaksotukset9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Toimittajan laskun tila on Odottaa niin kauan, kunnes todellinen toimittajan lasku saapuu.




