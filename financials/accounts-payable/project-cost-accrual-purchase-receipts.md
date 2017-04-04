---
title: "Projektin Kustannuskertymä-ostovastaanottojen"
description: "Tässä aiheessa kuvataan, kuinka jaksotettu projektikustannuksia Ostojen vastaanotot voidaan seurata Microsoft Dynamics-365 operaatioille."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 27a0a71095dce46c0119b32a92f8c4dce0f42e43
ms.lasthandoff: 03/31/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Projektin Kustannuskertymä-ostovastaanottojen

Tässä aiheessa kuvataan, kuinka jaksotettu projektikustannuksia Ostojen vastaanotot voidaan seurata Microsoft Dynamics-365 operaatioille. 

Projektin laskujen usein saapuvat myöhemmin kuin tavarat ja palvelut on toimitettu, joilla voisi olla merkittävä vaikutus projektin suorituskyvyn mittarit (KPI: T). Sen tärkeää voivat seurata näitä tapahtumia sekä taloudellisia ja projektin raportteja.

Esimerkiksi seuraavassa tilanteessa havainnollistaa tätä. 

Contoso-konsultointi on aloittanut uuden cloud käyttöönottoprojektin. Ostaa tietokoneen projektille luodaan ostotilaus. Tietokone kustannusten $1500 ja asennuspalvelut kustannusten $150. Toimittaja on toimitettu ja asennettu tietokoneeseen, mutta laskua ei ole vielä saavuttanut Contoso kuultuaan. Projektipäällikkö haluaa tarkastella projektin Kustannuskertymä $1650, ennen kuin lasku on toimitettu. Tämä kustannus olisi otettava huomioon myös yhtiön kuukauden lopussa tilinpäätöksen. 

Jaksotettu kustannus on merkittävä taloudellinen taso ja tason projektin raportointia varten. Taloudellista päivityksen tuotteen vastaanoton voi seurata Dynamics 365 toimintoja varten, kohteen ja hankintojen luokissa. 

Nimikkeille- **Ostoreskontran parametrit** -sivulla **Kirjataanko tuotteiden vastaanotot kirjanpitoon** vaihtoehto.
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Hankintojen luokkien- **luokan käytäntösääntö** -sivulla **ostaminen** käytäntöjä ja valitse sitten **Jaksota ostokulut vastaanoton** kunkin Hankintaluokalle.
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

**Ostaa laskuttamattomien menojen** ja **osto kertymä** asiakkuuksia **kirjausasetukset** käytetään, kun kirjataan tositteet, jotka liittyvät tuotteen vastaanoton.
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Käyttämällä tätä samaa skenaariota, Katsotaanpas miten tuotteen vastaanoton kirjaus vaikuttaa Kirjanpito- ja projektitietoja. 

**Vaihe 1:** Luo ja vahvista uusi ostotilaus project tallentaa tietokoneen $1500 ja asennuksen Services for $150.
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Ostotilauksen vahvistuksen jälkeen tapahtumat sidottu kustannus luodaan projekti. 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Sidottujen kustannusten tapahtumat on **tapahtuman alkuperä** -kentän arvoksi **ostotilauksen**. Luomalla ja vahvistamalla ostotilaus ei luo projektille tapahtumia. 

**Vaihe 2:** tavaroiden ja palvelujen perille ja tuotteen vastaanotto rekisteröidään. 

Tuotteen vastaanoton kirjaus luo ja kirjaa kirjanpidon tosite. Tosite osto menot, laskuttamattomien tilin debet- ja kredit-ostojen kertymätilin. 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Tuotteen vastaanoton kirjaus käyttää kirjausmääritysten hankintaluokat tuotteita ja ei ole projektiluokkien kirjausasetukset. Ostojen jaksotukset taloudellisista vaikutuksista ekologisia oikein, tämä asennus voidaan tasata. 

On mahdollista yhdistää hankintaluokat projektin luokkiin **hankintaluokka** sivulla.
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Vaihe 3:** luonnos toimittajalasku luodaan. 

Työvaiheiden Dynamics 365,-tuotteen vastaanoton kirjaus ei vaikuta projektitiedot. Kiertää luonnos toimittajalaskun voi luoda suoraan tavaran vastaanoton kirjauksen jälkeen. Siirry **ostotilauksen** sivulla &gt;**Lasku-välilehteen**&gt;**Luo**&gt;**laskun**. Tämä luo asiakirjan odottava lasku, joka päivittää projektitietoja. 

Luonnos toimittajalaskun luominen luo odottavat projektitapahtumat. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

- **Sidotut kustannukset** -sivulla vaiheessa 1 luotu tietueet voidaan sulkea ja muuttuvat kustannukset sitoumuksen lähtöisin odottava toimittajalasku luodaan uusia tietueita. **Tapahtuman alkuperä** kenttään sidotun kustannuksen arvoksi varten **toimittajalaskun**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Toimittajalaskun pysyy odottavassa tilassa, kunnes todellinen toimittajalasku saapuu.


