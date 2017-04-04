---
title: "Kustannuslaskennan analyysi BI virran sisältö"
description: "Tässä aiheessa kuvataan, mitä sisällytetään kustannuslaskentaan analyysin sisältöä virtaa BI. Artikkelissa kerrotaan, miten voit käyttää virtaa BI-raportteja ja tietoja tietomallin ja yhteisöistä, joita käytettiin rakentaa sisältöä."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 50e7bd92ee693f59fd013226aee22bd1a54c81e2
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Kustannuslaskennan analyysi BI virran sisältö

Tässä aiheessa kuvataan, mitä sisällytetään kustannuslaskentaan analyysin sisältöä virtaa BI. Artikkelissa kerrotaan, miten voit käyttää virtaa BI-raportteja ja tietoja tietomallin ja yhteisöistä, joita käytettiin rakentaa sisältöä.

<a name="overview"></a>Yleiskuvaus
--------

**Kustannuslaskennan analyysi** Microsoft Power BI sisältö on tarkoitettu kustannukset ohjaimien tai kuka tahansa, joka on vastuussa organisaation kustannusseuranta suorittamista. Se sisältää tärkeitä mittareita, kuten kustannusten suuruus ja kustannushinta budjetin kustannukset, todelliset kustannukset ja joustavan budjetin kustannukset. Se käyttää tapahtumatietoja kustannuslaskennan toimintoja Microsoft Dynamics-365 ja tarjoaa koko organisaation kustannusten yhteenlaskettu tutkimuksen raportoinnin valuutassa. Esimiehet voit suodattaa tietoja objektien kustannukset suorittaa kustannusseuranta ja organisaatioyksiköille, vaikka organisaatio voi olla useita oikeussubjekteja. Koska **kustannuslaskennan analyysi** BI virran sisältöä korostaa toteutuneiden kustannusten ja suunniteltujen kustannusten eroja johtajat voivat saada ilmoituksen positiivisten ja negatiivisten suuntausten niiden toiminnallista yksikköä. Johtajat voi porautua kustannukset elementin hierarkioita tai yksittäisiä kustannuselementeistä Hanki yksityiskohtaisia tietoja miten kustannusvariansseja on tapahtunut, ja sitten toteuttaa tehokkaita toimia. **Kustannuslaskennan analyysi** virtaa BI sisällön oletetaan, että kustannukset kirjanpitäjät analysoida miten kustannukset kulkee koko organisaation kustannus-objekteja. Katso lisätietoja kustannuslaskennan [kustannuslaskennan kotisivu](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page.md). Määrittämällä Accessin käyttäjätason suojauksen kustannuslaskennan ja yhdistetään rivitason BI virran suojauksen, voit myöntää kaikki kustannukset objektin omistajat pääsy **kustannuslaskennan analyysi** virtaa BI-sisältöä. Kaikki tiedot visualisointi sitten suodatetaan perusteella-taso, joka ohjaa kustannuslaskennan. Saat lisätietoja Accessin käyttäjätason suojauksen ja tietoturvan rivitason [kustannuslaskennan sisällön suojauksen määrittäminen Power BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Power BI-sisällön käyttämistä
Löydät **kustannuslaskennan analyysi** virtaa BI sisältöä jaettujen varojen kirjaston Microsoft Dynamics Lifecycle Services (LCS). Saat lisätietoja siitä, miten ladata sisältöä ja muodostamaan yhteyttä Dynamics 365 toimintoja tietojen [virtaa BI sisältöä Microsoftin ja kumppanien LCS-](power-bi-content-microsoft-partners.md). **Huomautus:** KB4011327 ** ** on edellytys **kustannuslaskennan analyysi** virtaa BI-sisältöä.  Kun kirjaudut Lifecycle Services, voit käyttää tätä KB: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittareita, jotka sisältyvät Power BI-sisältö
Sisältö sisältää raportin sivuja. Jokainen sivu koostuu joukko mittareita, jotka ovat visualized laatat, kaavioiden ja taulukoiden muodossa. Seuraavassa taulukossa on yleiskatsaus visualisointi **kustannuslaskennan analyysi** virtaa BI-sisältöä.

| Raportti-sivu                      | Kaavio                                                                                                                         | Ruutu                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kustannusseuranta kirjanpitokauden mukaan    | Todelliset kustannukset- ja kustannukset elementin hierarkiatason mukaan budjetin kustannukset                                                                   | Vs: todelliset kustannukset budjetin kustannukset                    |
|                                  | Budjetin varianssin kustannukset elementin hierarkiatason mukaan                                                                               | Nopeus vs todelliset kustannukset budjetin kustannukset-kurssi          |
|                                  | Top 10 varianssi prosentteina kustannustekijä mukaan                                                                          | Todellinen suuruus vs budjetin suuruus          |
| Kustannusseurannan perusteella vuoden alusta     | Todelliset kustannukset ja kalenterivuoden ajanjakson mukaan budjetin kustannukset                                                                           | Vs: todelliset kustannukset budjetin kustannukset                    |
|                                  | Budjetin varianssin kalenterivuoden ajanjakson mukaan                                                                                       | Nopeus vs todelliset kustannukset budjetin kustannukset-kurssi          |
|                                  | Top 10 varianssi prosentteina kustannustekijä mukaan                                                                          | Todellinen suuruus vs budjetin suuruus          |
| Kustannushinta tilikauden mukaan         | Todellisen kustannushinnan mukaan toiminnan kustannukset                                                                                             | Nopeus vs todelliset kustannukset budjetin kustannukset-kurssi          |
|                                  | Toteutunut kustannushinta, budjetin kustannusten varianssi nopeus, budjetin kustannukset prosenttiluvulla ja budjetin kustannushinta kustannukset elementin hierarkiatason mukaan | Todellinen suuruus vs budjetin suuruus          |
|                                  | Budjetin varianssin kustannukset elementin hierarkiatason mukaan                                                                               |                                               |
|                                  | Top 10 varianssi prosentteina kustannustekijä mukaan                                                                          |                                               |
| Joustavan budjetin kirjanpitokauden mukaan | Todelliset kustannukset, budjetin kustannukset- ja kustannukset elementin hierarkiatason mukaan joustavan budjetin kustannukset                                             | Todellinen suuruus vs budjetin suuruus          |
|                                  | Budjetin varianssin ja joustavan budjetin kustannukset-elementin hierarkiatason mukaan varianssi                                                  | Toteutunut kustannus vs joustavan budjetin kustannukset           |
|                                  | Todelliset kustannukset, budjetin kustannukset ja joustavat kustannukset mukaan toiminnan kustannukset ja kustannusten elementin Hierarkiataso                                  | Todelliset kustannukset nopeus vs joustavan budjetin kustannushinta |
| Kustannusraportti kirjanpitokauden mukaan  | Todelliset kustannukset kustannukset osa Hierarkiataso ja kustannukset dimension jäsennimi                                             |                                               |
|                                  | Todelliset kustannukset kustannukset dimension jäsennimi ja kustannukset elementin dimension jäsennimi                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Täyttääksesi raportin sivuja käytetään työvaiheiden tietoja Dynamics 365 **kustannuslaskennan analyysi** virtaa BI-sisältöä. Nämä tiedot esitetään koostaa mitat, jotka lisätään yrityksen säilössä, joka on Microsoft SQL-tietokannan, joka on optimoitu analytics. Lisätietoja on ohjeaiheessa [yksikön Myymälän integrointi yleistä Power BI](power-bi-integration-entity-store.md). Avaimen koosta mittauksissa käytetään sisällön perusteella.

| Kokonaisuus                  | Avaimen koosta mittaus | Tietolähteen Dynamics 365 operaatioille | Kenttä     | kuvaus                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Kustannuslaskennan tapahtumia | SUM(Amount)               | CAMDATAAggregatedCostEntry                  | Summa    | Summa valuuttana kustannuslaskenta kirjanpitoon |
| Tilastomerkinnät     | SUM(MAGNITUDE)            | CAMDATAAggregatedStatisctialEntry           | Suuruus |                                               |

Seuraavassa taulukossa on esitetty, miten avaimen koostaa mitat voidaan luoda useita laskettuja mittoja sisällön dataset-ryhmän.

| Mitta                                       | Miten on laskettu mitta                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Toteutunut kustannus                                   | Laske ('kustannuslaskennan tapahtumia'\[mitta\], 'Tapahtuma versiot'\[ISSOURCEVERSIONBUDGET\_arvo\] = 0)            |
| Budjetoitu kustannus                                   | Laske ('kustannuslaskennan tapahtumia'\[mitta\], 'Tapahtuma versiot'\[ISSOURCEVERSIONBUDGET\_arvo\] = 1)            |
| Kustannusten varianssi                          | \[Budjetin kustannukset\] - \[todelliset kustannukset\]                                                                                      |
| Talousarvion prosentuaalinen varianssi                    | IF (\[budjetin kustannukset\] = 0, blank(), \[budjetin varianssin\] / \[budjetin kustannukset\])                                                |
| Todellinen suuruus                              | Laske ('Tilastollisen tapahtumat'\[FullMagnitude\], 'Tapahtuma versiot'\[ISSOURCEVERSIONBUDGET\_arvo\] = 0)          |
| Budjetin suuruus                              | Laske (\[FullMagnitude\], 'Tapahtuma versiot'\[ISSOURCEVERSIONBUDGET\_arvo\] = 1)                               |
| Tilastollinen varianssi                   | \[Talousarvion suuruus\] - \[todellinen suuruus\]                                                                            |
| Budjetin tilastollinen varianssi prosentteina        | IF (\[talousarvion suuruus\] = 0, blank(), \[tilastollinen varianssi\] / \[talousarvion suuruus\])                          |
| Toteutunut kustannushinta                              | IF (\[todellinen suuruus\] = 0, BLANK(), \[todelliset kustannukset\] / \[todellinen suuruus\])                                          |
| Budjetin kustannushinta                              | IF (\[talousarvion suuruus\] = 0, BLANK(), \[budjetin kustannukset\] / \[talousarvion suuruus\])                                          |
| Kustannusten korvaus varianssi                     | \[Budjetin kustannushinta\] - \[Toteutunut kustannushinta\]                                                                            |
| Budjetin kustannusten varianssi prosenttiluvulla          | IF (\[budjetin kustannukset\] = 0, blank(), \[budjetin kustannusten korvaus varianssi\] / \[budjetin kustannushinta\])                                 |
| Kiinteä budjettikustannus                             | Laske (\[budjetin kustannukset\], 'Kustannuslaskenta tapahtumat'\[COSTBEHAVIOR\] = 1)                                              |
| Muuttuva budjetin kustannukset                          | Laske (\[budjetin kustannukset\], 'Kustannuslaskenta tapahtumat'\[COSTBEHAVIOR\] = 2)                                              |
| Joustavan budjetin kiinteä kustannus                    | \[Kiinteä budjettikustannus\]                                                                                                  |
| Muuttuva joustavan budjetin kustannukset                 | IF (\[talousarvion suuruus\] = 0, BLANK(), (\[muuttujan budjetin kustannukset\] / \[talousarvion suuruus\]) \*\[todellinen suuruus\])       |
| Joustavan budjetin kustannukset                          | \[Kiinteät kustannukset joustavaan budjettiin\] + \[muuttujan joustavan budjetin kustannukset\]                                                     |
| Joustavan budjetin varianssin                      | \[Joustavan budjetin kustannukset\] - \[todelliset kustannukset\]                                                                             |
| Joustavan budjetin prosentuaalinen varianssi           | IF (\[joustavan budjetin kustannukset\] = 0, BLANK(), \[joustavan budjetin varianssin\] / \[joustavan budjetin kustannukset\])                     |
| Joustavan budjetin kustannusten korvaus                     | IF (\[todellinen suuruus\] = 0, BLANK(), \[joustavan budjetin kustannukset\] / \[todellinen suuruus\])                                 |
| Joustavan budjetin kustannusten korvaus varianssi            | \[Joustavan budjetin kustannushinta\] - \[Toteutunut kustannushinta\]                                                                   |
| Joustavan budjetin kustannusten varianssi prosenttiluvulla | IF (\[joustavan budjetin kustannushinta\] = 0, BLANK(), \[joustavan budjetin kustannusten korvaus varianssi\] / \[joustavan budjetin kustannushinta\]) |

Suodattimina käytetään seuraavat tärkeimmät mitat osittaa yhteenlaskettu mittausten saavuttaa suurempi rakeisuus ja syvemmälle analyyttinen asuun.

| Kokonaisuus                             | Esimerkkejä määritteet                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Kustannuslaskennan kirjanpidot            | Kustannuslaskennan kirjanpito                                                                                               |
| Kustannusseurantayksiköt                 | Kustannusseurannan nimi                                                                                               |
| Kustannustason dimensiot            | Kustannusten elementtejä dimension nimi, kustannukset elementin dimension jäsennimi, kustannukset elementin dimension jäsenen kuvaus          |
| Kustannusobjektin dimensiot             | Kustannuskohteen dimension nimi, kustannukset dimension jäsennimi, kustannukset objektin dimension jäsenen kuvaus              |
| Tilastodimensiot             | Tilastollinen dimension nimi, tilastollinen dimension jäsennimi, tilastollinen dimension jäsenen kuvaus              |
| Kustannuskohteen dimensiohierarkiat  | Kustannusluokkien dimension hierarkian nimi, kustannus-objekti dimension Hierarkiataso kustannukset dimension hierarkian hakemistopuu    |
| Kustannusten elementin dimensiohierarkiat | Kustannusten elementti-dimension hierarkian nimi, kustannukset elementin dimension Hierarkiataso kustannukset elementti-dimensio hierarkiapuussa |
| Tilastollinen dimensiohierarkiat  | Tilasto-dimension hierarkian nimi, tilastollinen dimension Hierarkiataso, tilastollinen dimension hierarkiapuussa    |
| Tapahtuman versiot               | Version nimi                                                                                                         |
| Kirjanpidon kalenterit                   | Kalenterin kalenterin kuvaus                                                                                       |
| Tilikaudet                       | Kalenterivuosi                                                                                                        |
| Tilikaudet                     | Kalenterivuoden aikana                                                                                                 |

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](..\data-entities\data-entities.md)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](configure-power-bi-integration.md)
-   [Power BI kustannuslaskennan sisällön suojauksen määrittäminen](setup-security-cost-accounting-content-pack.md)


